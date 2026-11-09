---
description: >-
  Generador QR para piezas de producción: lectura de archivos, códigos
  identificadores, previsualización y elaboración de informe Excel.
layout:
  width: wide
---

# Generador de QR

[🏠 Volver al portal principal de Cabinet Report](https://danielmelendez-pma.github.io/cabinet-report-partners/)

**CABINET REPORT · IDENTIFICACIÓN DE PIEZAS**

## Lleva la identificación al despiece

Con el **Generador de QR** puedes preparar identificadores para las piezas de una producción y elaborar un **informe Excel** que reúne sus datos y códigos QR. Úsalo para facilitar la identificación de componentes durante el trabajo de taller.

{% hint style="info" %}
**Qué puedes obtener:** imágenes QR asociadas a piezas y un informe Excel, cuando la función esté habilitada. Antes de imprimir etiquetas o utilizarlas con lectores externos, verifica el resultado con tu equipo.
{% endhint %}

## 1. Preparar los archivos

1. Abre el Generador de QR desde la opción habilitada en Cabinet Report.
2. Utiliza **Seleccionar parámetros** para cargar los metadatos de módulo XML o el archivo **ParametrosRP** compatible.
3. Selecciona los **TXT de producción** que contengan las piezas.
4. Comprueba cliente, ambiente, referencia, módulos y cantidades.
5. Inicia la generación y revisa las piezas y los códigos resultantes.

Según la información disponible en los archivos de origen, el informe puede incluir **módulo, nombre de la pieza, cantidad, espesor, ancho, largo, material, veta y cantos**.

## 2. Generar el informe

La acción de registro crea un archivo de tipo **Informe QR - [cliente] - [ambiente].xlsx** en la carpeta de las fuentes seleccionadas y contempla insertar el logotipo configurado. Las imágenes QR se preparan temporalmente durante la creación.

{% hint style="warning" %}
El nombre interno de un control menciona «registrar en DB», pero el flujo de la acción inspeccionada **genera un informe Excel**. No debe interpretarse como prueba de un sistema completo de trazabilidad por escaneo ni de un registro de eventos de almacén en base de datos.
{% endhint %}

## 3. Uso en taller

Revisa la legibilidad de cada código, el tamaño de impresión, la asociación con la pieza correcta y la coincidencia del informe con el reporte de producción. La etiqueta facilita identificar piezas, pero **no demuestra que una pieza haya sido cortada, canteada, entregada o instalada**.

## Navegación relacionada

[Reporte de producción](reporte-de-produccion.md) · [Orden de producción](orden-de-produccion.md) · [Auditoría RP](auditoria-rp-persistencia.md)

---

[← Volver al inicio de Cabinet Report](../README.md)
