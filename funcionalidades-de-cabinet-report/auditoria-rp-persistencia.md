---
description: >-
  Auditoría RP: registros XML, identidad de producción, persistencia de revisiones,
  decisiones del usuario, recuperación y trazabilidad económica.
layout:
  width: wide
---

# Auditoría RP y persistencia

**CABINET REPORT · TRAZABILIDAD DE PRODUCCIÓN**

## Qué se registra y qué significa

La **Auditoría RP** reúne información sobre la apertura, transformación, revisión y preparación de una producción. Su función es **conservar evidencia técnica y decisiones**, no modificar el diseño ni certificar que una pieza física se fabricó correctamente.

Trabaja junto al [Reporte de Producción](reporte-de-produccion.md) y al [Revisor IA](revisor-inteligencia-artificial.md).

{% hint style="info" %}
**Distinción esencial:** el TXT contiene datos productivos; los metadatos técnicos describen la producción y sus módulos; el XML de Auditoría RP conserva registros de eventos, revisiones y decisiones. Son archivos con finalidades diferentes.
{% endhint %}

## 1. Componentes de la información

| Elemento | Función |
| --- | --- |
| **TXT del reporte** | Representar las piezas y atributos usados para preparar la fabricación. |
| **Metadatos XML de módulos** | Conservar atributos complementarios y fichas técnicas cuando estén disponibles. |
| **XML de Auditoría RP** | Registrar identidad, sesiones, aperturas, cambios, validaciones y evidencias del proceso. |
| **Revisiones del Revisor IA** | Guardar resultados, hallazgos, contexto y decisiones asociados a la auditoría. |
| **Registros económicos** | Conservar cálculos, referencias y estados de impactos cuando sean calculables y acreditables. |

El código contempla un nombre estable de **Auditoria RP** asociado con cliente, ambiente, referencia y, cuando existe un número de RP válido, ese identificador. Se conservan funciones auxiliares de compatibilidad e historial; **no presupongas que todo XML con un nombre parecido corresponde a la misma producción**.

## 2. Identidad y asociación de la revisión

Para que una revisión pueda reconocerse de manera confiable, el sistema utiliza distintos datos:

- **RevisionId y SolicitudRevisionIAId:** identifican el análisis y su solicitud.
- **IdCliente y usuario:** limitan el alcance de acceso y decisiones.
- **Cliente, ambiente y número de RP:** identifican la producción a la que se pretende asociar el resultado.
- **Fingerprint de producción:** contribuye a comprobar que los datos revisados corresponden al estado esperado.
- **Identificadores de módulos, piezas y hallazgos:** permiten localizar y relacionar la observación con la información original.

{% hint style="warning" %}
Un resultado que pertenece a otra producción, usuario o estado técnico no debe incorporarse como si fuera propio. Los controles de identidad pueden impedir su acreditación o modificación.
{% endhint %}

## 3. Cómo se conserva el XML

La implementación incorpora:

1. **Carga y validación** de documentos de auditoría existentes.
2. **Verificación de estructura** antes de registrar cambios.
3. **Guardado en archivo temporal** y validación del contenido preparado.
4. **Protección de escritura** con bloqueo y comparación del estado previo en disco.
5. **Reemplazo controlado**, verificación después del guardado y reintentos delimitados ante fallos transitorios.
6. **Preservación de saltos de línea** durante la serialización XML.

Estas salvaguardas reducen el riesgo de sobrescribir información concurrente, pero **no garantizan ausencia total de fallos** (permisos, archivos bloqueados, identidad incompatible, almacenamiento inaccesible o datos inválidos).

## 4. Revisión completada frente a revisión acreditada

Una revisión puede terminar su ejecución y mostrar **Completada**, incluso cuando se interpretaron **cero hallazgos**. Sin embargo, la acreditación en el XML exige comprobaciones adicionales.

El código incluye operaciones para:

- Registrar una revisión con identidad canónica y evitar conflictos con identificadores repetidos.
- Recuperar la última revisión completada y el historial correspondiente.
- Reconocer revisiones técnicas pendientes de persistencia mediante mecanismos de custodia y conciliación.
- Impedir decisiones cuando la revisión no pertenece a la producción o el usuario esperado.
- Conservar ciertos datos técnicos aun cuando la etapa de precios no esté disponible.

**Completada no significa automáticamente guardada.** Si la aplicación informa un problema de acreditación, no debes tratarlo como éxito.

## 5. Resolver y pasar por alto: decisiones trazables

Una decisión sobre un hallazgo está vinculada a la **revisión**, al **HallazgoId** y a la **identidad productiva**.

| Acción | Qué registra | Qué no demuestra |
| --- | --- | --- |
| **Resuelto** | El usuario decidió cerrar técnicamente el hallazgo. | Que la pieza física está correctamente fabricada. |
| **Pasar por alto** | El usuario acepta continuar sin aplicar esa corrección. | Que no exista riesgo ni que se haya evitado una pérdida. |
| **Nueva revisión** | Un análisis posterior sujeto a condiciones de acreditación. | Que todos los hallazgos anteriores desaparecieron por una corrección real. |
| **Continuar con pendientes** | Consentimiento para intentar generar con asuntos abiertos, cuando se solicita. | Que la generación o la fabricación terminó correctamente. |

Las decisiones económicas y técnicas **no son equivalentes**: resolver técnicamente puede dejar pendiente una valoración económica, y pasar por alto no supone dinero ahorrado.

## 6. Recuperar revisiones al volver a abrir

El código contiene lectura de revisiones previas, recuperación de historial y mecanismos de conciliación de información que quedó pendiente. Su objetivo es permitir continuidad sin adjudicar revisiones de un cliente o producción a otra.

Si no aparece una revisión esperada:

1. Comprueba que abriste **el mismo cliente, ambiente y RP**.
2. Revisa la carpeta del proyecto y la disponibilidad del XML de auditoría.
3. Comprueba si existe una advertencia de guardado o recuperación.
4. Evita borrar, renombrar o combinar manualmente XML históricos sin respaldo.
5. Conserva los mensajes y el archivo de origen para soporte o una prueba de reproducción.

{% hint style="warning" %}
**Comprueba la recuperación en tu equipo.** Si el sistema informa que una revisión o decisión no pudo guardarse, no supongas que ya está registrada. Vuelve a abrir la producción, verifica su estado y conserva los archivos y mensajes necesarios para solicitar soporte.
{% endhint %}

## 7. Economía de errores y precios de referencia

La aplicación incorpora servicios para estimar consumos, canto, reposición y continuidad económica entre revisiones. Puede aprovechar **precios propios o referencias comerciales** según su disponibilidad y los filtros de coincidencia.

La valoración está condicionada por datos como dimensiones, cantidad, formato comercial, material, espesor, canto y evidencia de precio. Una cifra calculada no representa automáticamente:

- **Un gasto incurrido:** la pieza quizá aún no se ha fabricado.
- **Una pérdida irrecuperable:** es necesario conocer las condiciones físicas de recuperación.
- **Un ahorro confirmado:** requiere una decisión y evidencia distintas del hallazgo técnico.
- **Un precio vigente:** las referencias en Internet pueden estar incompletas o sin verificación.

Por eso el reporte técnico debe seguir siendo interpretable aun si **no existe una referencia económica utilizable**.

## 8. Qué comprobar antes de cerrar el RP

Confirma que los archivos corresponden a la producción actual, que los cambios en TXT están guardados, que la última revisión y sus decisiones se recuperan correctamente y que cualquier mensaje de persistencia pendiente se ha atendido. Haz una copia de seguridad antes de intervenir manualmente en los documentos.

## Navegación relacionada

[Reporte de Producción](reporte-de-produccion.md) · [Revisor de Inteligencia Artificial](revisor-inteligencia-artificial.md) · [Explorador de proyectos](explorador-de-proyectos.md) · [Índice de funcionalidades](README.md)

---

[← Volver al inicio de Cabinet Report](../README.md)
