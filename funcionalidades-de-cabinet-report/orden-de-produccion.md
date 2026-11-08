---
description: >-
  Orden de Producción: agrupación de reportes RP, identificación de OP,
  materiales, archivos Excel y seguimiento de la asociación.
layout:
  width: wide
---

# Orden de producción

[🏠 Volver al portal principal de Cabinet Report](https://danielmelendez-pma.github.io/cabinet-report-partners/)

**CABINET REPORT · ORGANIZACIÓN DE REPORTES PARA FABRICACIÓN**

## Agrupa reportes de un mismo proyecto

La **Orden de Producción (OP)** reúne reportes de producción compatibles para organizar la fabricación bajo un identificador de orden. La herramienta está implementada en la ventana de órdenes y trabaja con reportes **RP en Excel**; no debe confundirse con un control integral de avance de planta.

<figure><img src="../.gitbook/assets/image (19).png" alt="Ventana original de Orden de Producción"><figcaption><p>Los reportes seleccionados se relacionan con una orden y un resumen de materiales.</p></figcaption></figure>

{% hint style="info" %}
**Alcance verificado en código:** selección de varios RP, revisión de asignaciones existentes, creación de número OP, archivo Excel con plantilla y registro de vínculo RP–OP. La ejecución real depende de la versión, permisos, archivos y almacenamiento.
{% endhint %}

## 1. Preparar los reportes

1. Genera y revisa los [reportes de producción](reporte-de-produccion.md) de los ambientes correspondientes.
2. En la ventana de OP, selecciona uno o varios archivos **RP - *.xlsx** almacenados localmente.
3. Comprueba el cliente, proyecto, ambientes y números RP reconocidos.
4. Revisa los materiales y las cantidades que aparecen en el resumen.
5. Confirma que los reportes que deseas incluir aún no estén asignados a otra OP.

El código detecta asociaciones previas y advierte si un número RP ya pertenece a una orden. El selector bloquea determinadas rutas de red: copia antes los archivos al equipo si aparece ese aviso.

## 2. Crear la orden

| Paso | Resultado esperado |
| --- | --- |
| **Comprobar número OP** | Evitar asignar nuevamente un identificador ya utilizado. |
| **Elegir destino** | Guardar un archivo **OP-[número] - [cliente].xlsx**. |
| **Usar plantilla** | Construir el Excel desde el recurso de la carpeta `Plantillas`. |
| **Registrar asociación** | Vincular los RP seleccionados con el número OP en el almacenamiento correspondiente. |
| **Consultar el listado** | Recuperar las órdenes previamente registradas para el cliente, cuando el contexto lo permite. |

{% hint style="warning" %}
**Un Excel creado no equivale automáticamente a una OP registrada.** Si la plantilla falta, el archivo está bloqueado o el guardado de la orden falla, atiende el mensaje y no distribuyas una orden incompleta.
{% endhint %}

## 3. Conexión y continuidad

En modo conectado, el formulario contempla guardar información en **TblTrackingOP** y asociar los RP mediante **TblTrackingRP**. En modo sin conexión, el código emplea caché local y una cola de sincronización, cuya conciliación posterior debe comprobarse al volver a conectarse.

Estas operaciones ayudan a conservar referencias administrativas; **no acreditan por sí mismas ejecución de corte, armado, entrega o instalación**.

## 4. Herramientas relacionadas

La misma área del código conserva acciones para **fusionar o separar optimizaciones** y convertir ciertos archivos de **Optiplanning** hacia formatos de **Itemizer**, condicionadas por la compatibilidad de los archivos. Esas transformaciones no sustituyen la creación del documento OP.

## 5. Antes de iniciar la fabricación

Verifica números RP y OP, cliente, cantidades, materiales, plantilla, destino del Excel y vínculos almacenados. Contrasta cada documento con las instrucciones reales de taller y comprueba las autorizaciones de uso.

## Sigue el flujo

[Reporte de producción](reporte-de-produccion.md) · [Reporte de compras](reporte-de-compras.md) · [Optimizadores](optimizadores.md) · [Auditoría RP](auditoria-rp-persistencia.md)

---

[← Volver al inicio de Cabinet Report](../README.md)
