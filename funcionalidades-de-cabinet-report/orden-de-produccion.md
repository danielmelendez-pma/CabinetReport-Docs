---
description: >-
  Orden de Producción: agrupación de reportes RP, identificación de OP,
  materiales, archivos Excel y seguimiento de la asociación.
layout:
  width: wide
---

# Orden de producción

**CABINET REPORT · ORGANIZACIÓN DE REPORTES PARA FABRICACIÓN**

## Agrupa reportes de un mismo proyecto

La **Orden de Producción (OP)** reúne reportes de producción compatibles para organizar la fabricación bajo un identificador de orden. La herramienta trabaja con reportes **RP en Excel**; no debe confundirse con un sistema de seguimiento físico de todas las etapas de planta.

<figure><img src="../.gitbook/assets/image (19).png" alt="Ventana original de Orden de Producción"><figcaption><p>Los reportes seleccionados se relacionan con una orden y un resumen de materiales.</p></figcaption></figure>

{% hint style="info" %}
**Qué puedes preparar:** selecciona reportes compatibles, comprueba sus asignaciones, identifica la orden y genera el Excel correspondiente. La disponibilidad de cada acción depende de tu versión, tus permisos y los archivos seleccionados.
{% endhint %}

## 1. Preparar los reportes

1. Genera y revisa los [reportes de producción](reporte-de-produccion.md) de los ambientes correspondientes.
2. En la ventana de OP, selecciona uno o varios archivos **RP - *.xlsx** almacenados localmente.
3. Comprueba el cliente, proyecto, ambientes y números RP reconocidos.
4. Revisa los materiales y las cantidades que aparecen en el resumen.
5. Confirma que los reportes que deseas incluir aún no estén asignados a otra OP.

Si el sistema informa que un RP ya pertenece a otra orden, revisa la asociación antes de continuar. Si la carpeta de red no está admitida para seleccionar archivos, utiliza una copia local autorizada y verifica que sea la versión correcta.

## 2. Crear la orden

- **Comprobar número OP** — Evitar asignar nuevamente un identificador ya utilizado.
- **Elegir destino** — Guardar un archivo **OP-[número] - [cliente].xlsx**.
- **Usar plantilla** — Construir el Excel desde el recurso de la carpeta `Plantillas`.
- **Registrar asociación** — Vincular los RP seleccionados con el número OP en el almacenamiento correspondiente.
- **Consultar el listado** — Recuperar las órdenes previamente registradas para el cliente, cuando el contexto lo permite.

{% hint style="warning" %}
**Un Excel creado no equivale automáticamente a una OP registrada.** Si la plantilla falta, el archivo está bloqueado o el guardado de la orden falla, atiende el mensaje y no distribuyas una orden incompleta.
{% endhint %}

## 3. Conexión y continuidad

Cuando hay conexión, las órdenes y sus vínculos pueden registrarse en el almacenamiento correspondiente. Si trabajaste sin conexión, **verifica la sincronización al recuperarla** y comprueba que la OP y los RP asociados aparezcan correctamente antes de distribuir el documento.

Estas operaciones ayudan a conservar referencias administrativas; **no acreditan por sí mismas ejecución de corte, armado, entrega o instalación**.

## 4. Herramientas relacionadas

En este flujo también puedes encontrar herramientas relacionadas con **unir o separar optimizaciones** y con la conversión de determinados formatos de trabajo. Consulta los [optimizadores](optimizadores.md) y comprueba la compatibilidad de los archivos: estas operaciones no sustituyen la creación de la OP.

## 5. Antes de iniciar la fabricación

Verifica números RP y OP, cliente, cantidades, materiales, plantilla, destino del Excel y vínculos almacenados. Contrasta cada documento con las instrucciones reales de taller y comprueba las autorizaciones de uso.

## Sigue el flujo

[Reporte de producción](reporte-de-produccion.md) · [Reporte de compras](reporte-de-compras.md) · [Optimizadores](optimizadores.md) · [Auditoría RP](auditoria-rp-persistencia.md)

---

[← Índice de funcionalidades](README.md) · [🏠 Portal principal de Cabinet Report](https://danielmelendez-pma.github.io/cabinet-report-partners/)
