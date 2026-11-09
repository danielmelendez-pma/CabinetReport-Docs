---
description: >-
  Auditoría RP de Cabinet Report: seguimiento de revisiones, guardado de
  decisiones, recuperación de información y referencias económicas.
layout:
  width: wide
---

# Auditoría RP y persistencia

**CABINET REPORT · SEGUIMIENTO DE PRODUCCIÓN**

## ¿Para qué sirve la Auditoría RP?

La **Auditoría RP** ayuda a conservar el historial de una producción: qué información se revisó, qué observaciones surgieron y qué decisiones tomaste antes de continuar. Complementa el [Reporte de Producción](reporte-de-produccion.md) y el [Revisor de Inteligencia Artificial](revisor-inteligencia-artificial.md).

No certifica que las piezas ya se hayan fabricado ni sustituye la inspección del responsable técnico.

## Dos situaciones frecuentes

{% columns %}
{% column width="50%" %}
### ✅ La revisión sigue visible

Confirma el cliente, ambiente y RP, y comprueba que los hallazgos y decisiones mostrados son los esperados.
{% endcolumn %}
{% column width="50%" %}
### 🔎 No encuentras una revisión

Verifica la identidad de la producción y los avisos de guardado. No sustituyas archivos XML sin respaldo; sigue las comprobaciones de recuperación de esta guía.
{% endcolumn %}
{% endcolumns %}

## 1. Qué información acompaña al proyecto

| Archivo o información | ¿Para qué se utiliza? |
| --- | --- |
| **Reporte de producción (TXT)** | Contiene las piezas y los datos utilizados para preparar la fabricación. |
| **Metadatos técnicos (XML)** | Conservan información adicional sobre los módulos, cuando corresponde. |
| **Auditoría RP (XML)** | Registra eventos, revisiones y decisiones relacionadas con la producción. |
| **Datos económicos** | Permiten consultar estimaciones y referencias de costos cuando existe información suficiente. |

{% hint style="info" %}
**No son archivos intercambiables.** Trabaja siempre con la producción correcta y evita modificar manualmente sus archivos sin respaldo.
{% endhint %}

## 2. Cómo comprobar que una revisión quedó guardada

1. Abre el proyecto con el **cliente, ambiente y reporte de producción** correctos.
2. Ejecuta o consulta la revisión del [Revisor IA](revisor-inteligencia-artificial.md), si está disponible para tu licencia.
3. Lee los hallazgos y verifica las medidas, materiales y piezas afectadas.
4. Registra las decisiones que corresponda tomar: **Resuelto** o **Pasar por alto**.
5. Comprueba que no aparezcan advertencias de guardado o acreditación.
6. Cuando necesites retomar el trabajo, **vuelve a abrir la misma producción** y confirma que las revisiones y decisiones esperadas siguen visibles.

Una revisión puede mostrar **Completada**, incluso con **cero hallazgos**, sin que ese estado por sí solo garantice que todos sus datos se hayan guardado correctamente.

## 3. Comprender las decisiones

| Acción | Qué significa | Qué no significa |
| --- | --- | --- |
| **Resuelto** | Indicas que atendiste el hallazgo. | No prueba que la pieza física esté corregida. |
| **Pasar por alto** | Decides continuar sin efectuar esa corrección. | No elimina el riesgo ni confirma un ahorro. |
| **Nueva revisión** | Solicitas otra evaluación del estado de la producción. | No implica que una observación anterior se haya corregido. |
| **Continuar con pendientes** | Autorizas continuar cuando el sistema solicita una confirmación. | No garantiza que el documento final o la fabricación estén correctos. |

{% hint style="warning" %}
**La decisión es tuya.** Si un hallazgo es grave o no comprendes sus consecuencias, verifica la información antes de generar u optimizar la producción.
{% endhint %}

## 4. Recuperar información al abrir nuevamente

Cabinet Report dispone de mecanismos para recuperar y reconocer revisiones previamente registradas, siempre que su identidad corresponda con la producción actual.

Si no encuentras una revisión o el sistema informa un problema de persistencia:

1. Confirma que abriste el **mismo cliente, ambiente y RP**.
2. Comprueba que tienes acceso a la carpeta del proyecto y a los archivos de auditoría.
3. Lee cualquier aviso de guardado, acreditación o recuperación y conserva el mensaje.
4. Evita eliminar, renombrar o combinar archivos XML para intentar corregir el problema.
5. Conserva una copia del proyecto y contacta con soporte si el estado sigue sin recuperarse.

**No des por guardada una decisión si el sistema informa que no pudo acreditarla.** Comprueba el estado antes de continuar y no sustituyas un archivo anterior sin respaldo.

## 5. Interpretar costos y posibles pérdidas

Cuando hay datos suficientes, la auditoría puede acompañarse de estimaciones relacionadas con materiales, cantos y reposición. Para valorar una referencia comprueba, entre otros elementos, el **material, marca, espesor, formato comercial, medidas y unidad de precio**.

Una cantidad calculada **no equivale automáticamente** a dinero gastado, material perdido o ahorro confirmado. Si no existen precios utilizables, la revisión técnica puede seguir siendo relevante aunque la estimación económica esté pendiente.

Para preparar una cotización consulta [Costos y cotizaciones](costos-en-desarrollo.md) y para validar un material consulta [Stock de tableros](stock-de-tableros.md).

## 6. Comprobación final antes de fabricar

Antes de distribuir los documentos, revisa que corresponden a la producción actual, que el TXT contiene los cambios esperados y que las decisiones importantes siguen guardadas. Conserva una copia de seguridad y asegúrate de que el equipo de fabricación recibe la versión correcta.

## Ensayo reproducible: recuperación y aislamiento de Auditoría RP

Esta comprobación **manual** permite registrar si una revisión y sus decisiones siguen asociadas a la producción correcta después de cerrar y volver a abrir el trabajo. Es un **procedimiento documental para ejecutar en Windows**, no una prueba funcional realizada por esta página ni una garantía de que el guardado siempre funciona.

### Preparar dos producciones de prueba

1. Utiliza dos producciones de prueba autorizadas, **A** y **B**, con identidad distinguible (cliente, ambiente y número de RP, si existe). No cambies la identidad de una producción real para fabricar el caso.
2. Antes de intervenir, conserva una **copia independiente** de los TXT, XML de metadatos y XML de Auditoría RP que existan. Anota rutas, nombres, fecha y versión de Cabinet Report. No edites, renombres ni combines XML manualmente.
3. Abre cada producción y anota el usuario autorizado, el estado previo del Revisor IA, el proveedor/modelo mostrados cuando existan y la identificación de la revisión disponible. Si un dato no aparece, registra **«no disponible»** en lugar de inventarlo.
4. Toma evidencia de la pantalla y de los archivos **sin revelar credenciales ni datos confidenciales**. Usa la [guía del Revisor IA](revisor-inteligencia-artificial.md) para interpretar los estados y las decisiones.

### Casos que deben comprobarse por separado

| Caso | Ejecución manual | Evidencia a conservar |
| --- | --- | --- |
| **A · Revisión con cero hallazgos** | Si una revisión de prueba termina **Completada** sin hallazgos, cierra y vuelve a abrir **A**. Comprueba que la revisión siga identificable, sin convertir «Completada» en prueba automática de persistencia. | Identidad A; estado; cantidad **0**; proveedor/modelo si aparecen; aviso de guardado; revisión recuperada. |
| **B · Revisión con hallazgos** | En **B**, si existen hallazgos reales, registra sus identificadores y toma decisiones **Resuelto** o **Pasar por alto** solo cuando corresponda. Cierra y vuelve a abrir B para contrastar cada decisión. | Identidad B; hallazgos antes/después; decisiones por hallazgo; mensajes de acreditación; revisión recuperada. |
| **A ↔ B · Aislamiento** | Tras revisar B, abre nuevamente A y contrasta las identidades, los hallazgos y las decisiones de ambas. No debe considerarse conforme una revisión atribuida a la producción equivocada. | Comparación A/B y rutas de sus archivos de auditoría; cualquier mezcla, ausencia o duplicación observada. |
| **Incidencia de guardado** | Si aparece un aviso de falta de acreditación, recuperación pendiente o bloqueo para nueva revisión, **detén el ensayo**. No fuerces una nueva revisión ni sobrescribas el XML para lograr un resultado aparente. | Mensaje literal, paso que lo produjo, versión, producción afectada y respaldo conservado para soporte. |

Si la revisión no produce naturalmente cero hallazgos o hallazgos suficientes para un caso, márcalo **NO EJECUTADO**; no alteres respuestas IA, archivos o decisiones reales para simular que se completó.

### Criterio de cierre del ensayo

- **CONFORME:** en los casos efectivamente ejecutados, la revisión y las decisiones vuelven a verse en la **misma identidad** tras reabrir, sin avisos de acreditación pendientes ni mezcla entre A y B.
- **NO CONFORME:** desaparece una revisión o decisión que debía recuperarse, aparece asociada a otra producción, se observa duplicación conflictiva o la aplicación comunica que no pudo guardar/acreditar el estado.
- **NO EJECUTADO:** falta la condición necesaria para el caso, no se dispone de revisión o no se realizó la reapertura. No conviertas ese resultado en «CONFORME».

**Para cerrar la comprobación integral como CONFORME** deben haberse ejecutado y satisfecho **A, B y aislamiento A/B**. Documenta por separado cualquier caso no ejecutado. Si observas varios XML de auditoría con nombres distintos para la misma producción, conserva todos como evidencia y solicita diagnóstico: **la cantidad de archivos, por sí sola, no identifica cuál es el registro válido**.

{% hint style="warning" %}
**Criterio de fabricación:** un ensayo de persistencia satisfactorio no valida dimensiones, cantos, materiales ni decisiones técnicas. Si una revisión o decisión no puede acreditarse, conserva el respaldo y verifica el estado con soporte antes de liberar la producción.
{% endhint %}

## Navegación relacionada

[Reporte de Producción](reporte-de-produccion.md) · [Revisor IA](revisor-inteligencia-artificial.md) · [Manual de usuario](../manual-de-usuario.md) · [Índice de funcionalidades](README.md)

---

[**🏠 Volver al portal principal de Cabinet Report**](https://danielmelendez-pma.github.io/cabinet-report-partners/)
