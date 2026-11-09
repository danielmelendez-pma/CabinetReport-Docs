---
description: >-
  Punto de partida para aprender a utilizar Cabinet Report: acceso al curso,
  primeros pasos, funcionalidades y ayuda para usuarios.
layout:
  width: wide
---

# Manual de usuario

**CABINET REPORT · APRENDE A UTILIZAR EL SOFTWARE**

## Comienza con lo esencial

Esta sección te orienta para aprender a utilizar Cabinet Report en la **planificación y preparación de la fabricación de muebles**. Encontrarás el acceso al curso de uso y las páginas de referencia para consultar cada herramienta.

<figure><img src=".gitbook/assets/image.png" alt="Ilustración de aprendizaje y manual de Cabinet Report" width="188"><figcaption><p>Aprende a tu ritmo y consulta las herramientas cuando las necesites.</p></figcaption></figure>

{% hint style="info" %}
**El curso se encuentra en un sitio de aprendizaje independiente.** Puedes abrirlo desde el enlace siguiente y regresar a esta documentación para consultar las características y condiciones de cada función.
{% endhint %}

[**📘 Abrir el curso de Cabinet Report ↗**](https://cabinet-report.gitbook.io/curso-de-cabinet-report/)

## Ruta recomendada para empezar

{% columns %}
{% column width="50%" %}
### 1. Accede a tu cuenta

Comprueba que tienes tus credenciales y la licencia correspondiente. Familiarízate con la ventana principal.

[Inicio de sesión](funcionalidades-de-cabinet-report/inicio-de-sesion.md) · [Licencia de cliente](funcionalidades-de-cabinet-report/licencia-de-cliente.md)

### 2. Organiza tu proyecto

Conoce cómo localizar proyectos y utilizar los módulos disponibles como punto de partida.

[Explorador de proyectos](funcionalidades-de-cabinet-report/explorador-de-proyectos.md) · [Catálogo de módulos](funcionalidades-de-cabinet-report/catalogo-de-modulos.md)
{% endcolumn %}
{% column width="50%" %}
### 3. Prepara piezas y materiales

Revisa dimensiones, espesores, cantidades, vetas y cantos antes de generar los archivos.

[Creador de módulos](funcionalidades-de-cabinet-report/creador-de-modulos.md) · [Creador de piezas](funcionalidades-de-cabinet-report/creador-de-piezas.md)

### 4. Revisa y genera la producción

Consulta el reporte, las comprobaciones disponibles y las herramientas de optimización según tu licencia.

[Reporte de producción](funcionalidades-de-cabinet-report/reporte-de-produccion.md) · [Revisor IA](funcionalidades-de-cabinet-report/revisor-inteligencia-artificial.md) · [Optimizadores](funcionalidades-de-cabinet-report/optimizadores.md)
{% endcolumn %}
{% endcolumns %}

## Después del primer Reporte de Producción

Una vez revisado el despiece, elige la continuación que necesites. **No es obligatorio utilizar todas las herramientas en un mismo proyecto**:

- **Preparar el corte:** consulta los [Optimizadores](funcionalidades-de-cabinet-report/optimizadores.md) y confirma el material, las piezas y las restricciones de la máquina.
- **Planificar compras o cotizar:** revisa el [Reporte de compras](funcionalidades-de-cabinet-report/reporte-de-compras.md) y, cuando corresponda, continúa en [Costos y cotizaciones](funcionalidades-de-cabinet-report/costos-en-desarrollo.md).
- **Agrupar trabajos de fabricación:** conoce la [Orden de producción](funcionalidades-de-cabinet-report/orden-de-produccion.md).
- **Retomar una revisión asistida:** consulta [Auditoría RP y persistencia](funcionalidades-de-cabinet-report/auditoria-rp-persistencia.md) para comprobar decisiones y recuperación de la producción.

## Antes de enviar información al taller

1. Comprueba que **las medidas, los materiales y las cantidades** correspondan al proyecto.
2. Revisa los avisos del sistema y los hallazgos de IA, si la función está habilitada.
3. Verifica el contenido de los archivos generados y que el destinatario pueda utilizarlos.
4. Conserva una copia de la información necesaria para realizar correcciones.

{% hint style="warning" %}
**La revisión humana sigue siendo obligatoria.** Una producción generada, una optimización terminada o una revisión IA sin hallazgos no garantiza la ausencia de errores.
{% endhint %}

## Ensayo operativo: sustitución de un RP ya distribuido

Cuando se corrige un **Reporte de Producción que ya llegó a otras áreas**, generar otro archivo no retira las copias anteriores. El siguiente control ayuda a evitar que el taller trabaje con una versión desactualizada. Es un **procedimiento manual de coordinación**, no una función de envío, revocación o control de versiones automático de Cabinet Report.

### 1. Prepara un caso de prueba sin alterar la producción

1. Trabaja con **copias** de un RP de prueba ya revisado y sus archivos relacionados. Identifica cliente, ambiente, número RP si existe, fecha y responsable; conserva el original sin sobrescribirlo.
2. Llama **V1** a la copia inicialmente entregada y **V2** a la copia corregida. Estas etiquetas son **solo identificadores de este ensayo**, no campos ni versiones que el programa genere.
3. Simula una corrección autorizada en el **canto derecho de una pieza**: sus medidas y cantidad pueden mantenerse iguales mientras cambia una instrucción de canteo. Anota pieza, valor anterior, valor corregido y motivo; verifica también las demás propiedades pertinentes.
4. Identifica qué documentos se habían distribuido desde V1: Excel RP, TXT, resultados de optimización, reportes de compras, complementarios u OP, **solo si realmente existen y se utilizaron**. No supongas que todos cambian por la misma corrección.

### 2. Concilia el cambio y sus destinatarios

| Destinatario o proceso | Verificación antes de reanudar | Evidencia que debes conservar |
| --- | --- | --- |
| **Corte y canteo** | Comparar la pieza y el canto corregido; revisar de nuevo el archivo o instrucciones efectivamente recibidas, y el estado del trabajo iniciado. | Identificador de V2, archivo recibido y confirmación del responsable. |
| **Montaje e instalación** | Confirmar si tienen planos, RP o instrucciones derivados de V1; sustituir los afectados. | Destinatario, documento actualizado y confirmación de sustitución. |
| **Compras y almacén** | Revisar si el cambio modifica materiales, cantos o cantidades solicitadas; si no impacta, registrar también esa conclusión. | Resultado de la revisión y aviso a las áreas afectadas. |
| **Orden de Producción y archivos de corte** | Si existen, conciliar su referencia a los RP y los resultados derivados; un archivo Excel nuevo no demuestra por sí solo la actualización de una OP registrada. | Identificación de los archivos o asociaciones comprobados y su estado. |

Para ubicar cada salida consulta el [Reporte de producción](funcionalidades-de-cabinet-report/reporte-de-produccion.md), los [Optimizadores](funcionalidades-de-cabinet-report/optimizadores.md), el [Reporte de compras](funcionalidades-de-cabinet-report/reporte-de-compras.md) y la [Orden de producción](funcionalidades-de-cabinet-report/orden-de-produccion.md), según corresponda.

### 3. Prueba la sustitución antes de liberar

1. Registra **qué cambió entre V1 y V2**, los archivos regenerados y los que no requieren cambios, con la justificación pertinente. Compara por pieza y atributo, **no únicamente por totales**.
2. Avisa expresamente a quienes recibieron V1 que **esa copia queda sustituida para el trabajo afectado**. Identifica la V2 autorizada y evita mantener dos archivos indistinguibles como «definitivos».
3. Solicita a cada destinatario una **confirmación verificable** de recepción y reemplazo, y comprueba que no seguirá trabajando con V1. Una notificación enviada no demuestra que se haya recibido o aplicado.
4. Si alguna operación de corte, canteo, compra o instalación **ya comenzó con V1**, detén la parte afectada y coordina la evaluación de lo ejecutado con su responsable. Cambiar el archivo no corrige automáticamente piezas cortadas ni pedidos emitidos.
5. Conserva el registro de V1 y V2, sus diferencias, destinatarios, confirmaciones y decisión final. No borres los originales para simular una revocación.

### 4. Resultado comprobable del ensayo

- **CONFORME:** los cambios de V2 se identifican, cada salida afectada se revisó, todos los destinatarios que usaban V1 confirmaron la sustitución y no queda trabajo afectado sin evaluar.
- **NO CONFORME:** algún destinatario continúa con V1, falta confirmar el reemplazo, existen salidas incompatibles o ya se ejecutó un proceso afectado sin aclarar sus consecuencias.
- **NO EJECUTADO:** no se practicó la verificación con archivos, responsables o evidencias reales; disponer de esta guía no acredita una prueba funcional.

**Prueba de detección:** si el encargado de canteo sigue consultando V1 aunque el Excel V2 muestre el canto corregido, el resultado es **NO CONFORME**. No se libera el cambio hasta comprobar el reemplazo y resolver cualquier trabajo iniciado.

{% hint style="warning" %}
**Alcance:** estas comprobaciones deben realizarlas las personas responsables. No se afirma que Cabinet Report gestione automáticamente versiones, notificaciones, acuses, cancelaciones de órdenes o reversión de procesos físicos. Este ensayo documental **no equivale a una prueba funcional en Windows**.
{% endhint %}

## ¿Necesitas ayuda?

Consulta las [Políticas de Soporte](politicas-de-soporte.md) para conocer el alcance de la asistencia y los [canales oficiales](redes-sociales.md) para encontrar novedades. Si vas a solicitar ayuda, identifica la versión instalada, el módulo afectado y los mensajes que aparecen. No compartas contraseñas ni credenciales.

También puedes revisar la [Política de Capacitación e Implementación](politica-de-capacitacion-e-implementacion.md) y las [funcionalidades disponibles](funcionalidades-de-cabinet-report/README.md).

---

[**Documentación oficial**](README.md) · [**🏠 Portal principal**](https://danielmelendez-pma.github.io/cabinet-report-partners/)
