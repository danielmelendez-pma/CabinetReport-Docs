---
description: >-
  Generador QR para piezas de producción: lectura de archivos, códigos
  identificadores, previsualización y elaboración de informe Excel.
layout:
  width: wide
---

# Generador de QR

**CABINET REPORT · IDENTIFICACIÓN DE PIEZAS**

## Lleva la identificación al despiece

El **Generador de QR** cuenta con un formulario y rutas implementadas para leer piezas de producción, preparar identificadores y crear códigos QR asociados a ellas. Puede producir un **informe Excel** con los datos de las piezas y sus imágenes QR.

{% hint style="info" %}
**Funcionalidad desarrollada:** el repositorio incluye generación de imágenes QR y un informe Excel. Su disponibilidad para cada usuario, impresión y lectura con dispositivos externos deben comprobarse en la instalación concreta.
{% endhint %}

## 1. Preparar los archivos

1. Abre el Generador de QR desde la opción habilitada en Cabinet Report.
2. Utiliza **Seleccionar parámetros** para cargar los metadatos de módulo XML o el archivo **ParametrosRP** compatible.
3. Selecciona los **TXT de producción** que contengan las piezas.
4. Comprueba cliente, ambiente, referencia, módulos y cantidades.
5. Inicia la generación y revisa las piezas y los códigos resultantes.

Los datos de piezas considerados por el código abarcan **módulo, nombre, cantidad, espesor, ancho, largo, material, veta y cantos**, cuando están presentes en el origen.

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
