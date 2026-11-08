---
description: >-
  Reporte de Compras: informes Excel de uno o varios ambientes, fuentes
  de materiales, opciones de perfilería y trazabilidad de consolidación.
layout:
  width: wide
---

# Reporte de compras

**CABINET REPORT · RELACIÓN DE MATERIALES PARA ABASTECIMIENTO**

## Reúne lo necesario para comprar

El módulo **Reporte de Compras** procesa archivos de materiales de producción, agrupa partidas y genera un **Excel**. Tiene dos modalidades implementadas: **Un ambiente** y **Varios ambientes**.

<figure><img src="../.gitbook/assets/image (16) (1).png" alt="Ventana original del Reporte de Compras"><figcaption><p>El informe parte de archivos de materiales y requiere comprobar las unidades y cantidades.</p></figcaption></figure>

{% hint style="info" %}
**Alcance del reporte:** permite generar y consolidar informes de compras. No debe interpretarse como una compra automática a proveedores, una confirmación de recepción o una actualización de inventario físico.
{% endhint %}

## 1. Prepara las fuentes

El [Reporte de producción](reporte-de-produccion.md) y sus archivos auxiliares pueden aportar información para compras. Comprueba que materiales, cantidades y unidades correspondan con el proyecto actual. La importación no corrige necesariamente errores de origen.

## 2. Un ambiente

1. Selecciona **Un ambiente**.
2. Completa **cliente, ambiente y referencia**.
3. Ejecuta la acción y selecciona los archivos admitidos.
4. El formulario valida las rutas y prepara un resumen de materiales.
5. Genera el **Excel del Reporte de Compras** y comprueba su contenido.
6. Revisa el documento antes de enviarlo a almacén o a un proveedor.

El código evita registrar como éxito una generación que no complete las etapas obligatorias de resumen, Excel y logo.

## 3. Varios ambientes

Permite escoger una carpeta principal o agregar carpetas `Materiales`, identificar los ambientes, marcar los incluidos y consolidar fuentes compatibles bajo un **cliente oficial** y una **referencia consolidada**.

| Resultado | Descripción |
| --- | --- |
| **Excel consolidado** | Resumen de materiales de los ambientes seleccionados. |
| **Hoja Trazabilidad** | Ambiente y archivos incluidos/excluidos, órdenes, advertencias y resultado. |
| **TXT de trazabilidad** | Archivo auxiliar en una subcarpeta `Trazabilidad`. |
| **Órdenes de corte opcionales** | Publicación de órdenes consolidadas de perfilería cuando los archivos y las opciones lo permiten. |

El módulo advierte si las fuentes corresponden a clientes diferentes. También puede continuar con un ambiente sin ciertos parámetros complementarios **si hay archivos válidos**, informando la circunstancia. No debe escribirse el consolidado dentro de la carpeta de origen `Materiales`.

## 4. Tubos, golas, zócalos y unidades

La implementación lee y clasifica archivos de perfilería y contempla cálculos de corte lineal para materiales seleccionados. No supongas que todas las partidas se miden igual; comprueba si una partida representa **unidades, tramos o longitud**.

## 5. Revisar antes de adquirir

{% hint style="warning" %}
**Generar compras no equivale a comprar.** Verifica proveedor, stock real, precio, cantidad, formato de presentación, transporte, impuestos y plazos antes de emitir una solicitud comercial.
{% endhint %}

Los archivos Excel de compras pueden importarse después en [Costos y cotizaciones](costos-en-desarrollo.md) para completar la valoración del proyecto.

## Continúa el flujo

[Reporte de producción](reporte-de-produccion.md) · [Costos y cotizaciones](costos-en-desarrollo.md) · [Optimizadores](optimizadores.md) · [Orden de producción](orden-de-produccion.md)
---

[← Volver al inicio de Cabinet Report](../README.md)
