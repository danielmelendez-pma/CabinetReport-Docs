---
description: >-
  Costos y cotizaciones: importación de reportes, materiales, márgenes,
  impuestos, resúmenes por ambiente y documentos exportables.
layout:
  width: wide
---

# Costos y cotizaciones

[🏠 Volver al portal principal de Cabinet Report](https://danielmelendez-pma.github.io/cabinet-report-partners/)

**CABINET REPORT · DEL MATERIAL AL PRESUPUESTO**

## De la información productiva a un precio revisable

La ventana **Costos** está implementada en Cabinet Report: reúne partidas de materiales, cantidades, precios, márgenes y condiciones para calcular importes y preparar cotizaciones. Su funcionamiento se apoya en archivos y catálogos disponibles; no debe considerarse una estimación automática infalible.

<figure><img src="../.gitbook/assets/image (1).png" alt="Vista original del módulo Costos"><figcaption><p>Los costos se organizan por proyecto y ambiente.</p></figcaption></figure>

{% hint style="info" %}
**Disponibilidad:** las opciones de carga, cálculo, guardado y exportación pueden variar según la versión y los permisos. Comprueba los importes y revisa el archivo exportado antes de utilizarlo en una cotización.
{% endhint %}

## 1. Qué puedes preparar

| Sección | Uso |
| --- | --- |
| **Materia prima (MA)** | Partidas con descripción, cantidad, unidad, costo unitario y total. |
| **Margen de producción (MP)** | Porcentajes o importes vinculados a fabricación y transformación. |
| **Margen operativo (MO)** | Gastos y márgenes propios de la operación comercial. |
| **Precio de venta** | Subtotal, ITBMS y total de venta calculados. |
| **Ambientes** | Organización y resumen de diferentes espacios del proyecto. |
| **Notas y condiciones** | Descripciones, exclusiones, observaciones y condiciones de pago para revisión. |

<figure><img src="../.gitbook/assets/image (6).png" alt="Resumen de subtotales e importes en Costos"><figcaption><p>Los totales dependen de la información cargada y de la configuración aplicable.</p></figcaption></figure>

## 2. Cargar datos

1. Identifica el proyecto y el ambiente que deseas costear.
2. En el menú, utiliza **Cargar reporte de compras** para importar uno o varios Excel compatibles.
3. Si ya trabajaste el presupuesto, usa **Cargar costos** para recuperar archivos XML.
4. Revisa cada partida importada: cantidad, unidad, descripción y precio.
5. Ajusta los márgenes y las notas antes de calcular la oferta.
6. Revisa los totales y conserva el respaldo correspondiente.

Existe además una ruta de procesamiento de **PDF de Promob**, cuya compatibilidad debe verificarse según la estructura del archivo de origen.

<figure><img src="../.gitbook/assets/image (2).png" alt="Detalle de materia prima del presupuesto"><figcaption><p>La materia prima puede alimentarse desde el reporte de compras y ajustarse con control del usuario.</p></figcaption></figure>

## 3. Precios de los materiales

El código contiene lectura de precios desde catálogos de tableros y herrajes, diferenciando registros públicos y privados, así como mecanismos para actualizar referencias privadas y clonar materiales permitidos al catálogo del cliente.

{% hint style="warning" %}
**Un precio almacenado no demuestra vigencia.** Antes de enviar la cotización, comprueba proveedor, formato, espesor, moneda, unidad e impuestos. Una partida sin precio confiable debe revisarse expresamente.
{% endhint %}

No confundas el **precio de venta comercial** de esta ventana con la **economía de errores del Revisor IA**. Esta última registra estimaciones de impacto técnico y referencias económicas con una finalidad diferente.

## 4. Márgenes de producción y operación

{% columns %}
{% column width="50%" %}
### Fabricación

<figure><img src="../.gitbook/assets/image (7).png" alt="Margen de producción"><figcaption><p>Importes relacionados con los procesos de fabricación.</p></figcaption></figure>

Revisa los conceptos propios del corte, canteo, mecanizado, armado, inspección o instalación que apliquen al trabajo.
{% endcolumn %}

{% column width="50%" %}
### Operación

<figure><img src="../.gitbook/assets/image (8).png" alt="Margen operativo"><figcaption><p>Gastos y objetivos de rentabilidad del negocio.</p></figcaption></figure>

El sistema contempla guardar y recuperar márgenes, para que el usuario pueda reutilizar su configuración y modificarla cuando cambien las condiciones.
{% endcolumn %}
{% endcolumns %}

El cálculo de **precio de venta** suma los subtotales pertinentes y aplica el parámetro de ITBMS de la aplicación. La tasa y su aplicabilidad deben revisarse para cada operación.

## 5. Comparar ambientes

<figure><img src="../.gitbook/assets/image (10).png" alt="Resumen de ambientes"><figcaption><p>El resumen agrupa los importes del proyecto por ambiente.</p></figcaption></figure>

Los ambientes permiten revisar diferencias de materiales, márgenes y precios. Comprueba que no se dupliquen partidas comunes cuando consolides varios espacios.

## 6. Guardar y exportar cotizaciones

Desde el menú se implementan **Exportar costos**, exportación a **Excel (.xlsx)** y creación de cotizaciones en dos presentaciones: **Word (.docx) tipo carta** y **Excel (.xlsx) tipo tabla**. Para ambas cotizaciones, el programa exige que primero exista un **Excel de costos exportado y disponible**.

<figure><img src="../.gitbook/assets/image (12).png" alt="Notas y condiciones comerciales"><figcaption><p>Las notas, exclusiones y condiciones deben revisarse antes de compartir una oferta.</p></figcaption></figure>

{% hint style="warning" %}
**Antes de entregar:** revisa el Excel fuente, los importes, el ITBMS, las cantidades, los términos comerciales y el documento exportado. La exportación no certifica el precio final ni la aceptación de la oferta.
{% endhint %}

## Sigue el proceso

[Reporte de compras](reporte-de-compras.md) · [Stock de tableros](stock-de-tableros.md) · [Reporte de producción](reporte-de-produccion.md) · [Auditoría RP y economía de errores](auditoria-rp-persistencia.md)
---

[← Volver al inicio de Cabinet Report](../README.md)
