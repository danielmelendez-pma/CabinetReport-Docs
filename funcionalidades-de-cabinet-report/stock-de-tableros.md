---
description: >-
  Catálogo de tableros y materiales: fabricante, proveedor, medidas, veta,
  precios registrados, fichas técnicas y visibilidad pública y privada.
layout:
  width: wide
---

# Stock de tableros

**CABINET REPORT · CATÁLOGO TÉCNICO DE MATERIALES**

## Identifica los tableros de tu proyecto

**Stock de Tableros** es la ventana de consulta y administración de referencias de materiales utilizadas en Cabinet Report. Su interfaz contempla búsqueda, filtros, tarjetas, vista de lista, detalles y un editor con operaciones sujetas a permisos.

<figure><img src="../.gitbook/assets/image (15) (1).png" alt="Vista original del catálogo de tableros"><figcaption><p>Consulta de referencias con sus datos técnicos y comerciales disponibles.</p></figcaption></figure>

{% hint style="warning" %}
**Catálogo no es inventario físico.** Aunque la pantalla se denomina «Stock», no se comprobó en este formulario un registro integral de entradas/salidas, ubicación en almacén, reservas o existencias verificadas en tiempo real.
{% endhint %}

## 1. Información de cada tablero

| Campo | Para qué sirve |
| --- | --- |
| **Material / descripción** | Identificar la referencia del tablero. |
| **Proveedor y fabricante** | Reconocer su origen comercial. |
| **Espesor** | Revisar compatibilidad con piezas y fórmulas. |
| **Ancho y largo** | Registrar el formato comercial de la plancha. |
| **Veta** | Considerar la orientación durante el corte. |
| **Código de proveedor** | Identificar el artículo en catálogos externos. |
| **Precio** | Consultar la referencia registrada, cuando existe y es válida. |
| **Imagen y ficha** | Facilitar la identificación y abrir una búsqueda técnica. |

La ventana contiene filtros combinables por proveedor, fabricante, código, espesor, veta, dimensiones, precio y tipo de catálogo; permite cambiar entre **tarjetas paginadas** y **tabla de lista**.

## 2. Públicos y privados

- **Catálogo público:** referencias compartidas según reglas de acceso del software.
- **Catálogo privado:** referencias correspondientes al cliente propietario.
- **Agregar a mi catálogo:** bajo las condiciones y permisos implementados, permite clonar un tablero público como referencia privada del cliente actual.

Los controles de edición distinguen el **nivel A**, para administración de tableros públicos, y el **nivel B**, limitado a referencias privadas propias. Ciertas acciones requieren columnas de visibilidad y precio disponibles en la base de datos.

## 3. Crear y editar

1. Busca la referencia antes de crearla para evitar duplicados.
2. Selecciona **Nuevo tablero** o un registro existente con permisos de edición.
3. Introduce descripción, proveedor, fabricante, código, medidas, espesor, veta y precio, según corresponda.
4. Selecciona la visibilidad que permite tu perfil.
5. Guarda y comprueba que la ficha muestre los datos esperados.
6. Si lo necesitas, administra una imagen o consulta la búsqueda de ficha técnica.

El editor contempla **alta, edición y eliminación con confirmación**, con autorización respecto al registro seleccionado. La búsqueda en el navegador **no garantiza** encontrar una ficha oficial o del mismo producto.

## 4. Relación con el RP y el optimizador

El catálogo proporciona materiales para el [Reporte de producción](reporte-de-produccion.md) y las [herramientas de optimización](optimizadores.md). Debes corroborar espesor, veta, formato y nombre antes de preparar los cortes.

La grilla de tableros y cantidades dentro del optimizador representa disponibilidad **para el cálculo** y puede incluir retazos; esto no sincroniza automáticamente un almacén físico.

## 5. Precios y limitaciones

Los campos de precio dependen de datos y permisos realmente disponibles. No supongas que un valor ausente o almacenado representa una cotización vigente del proveedor. Para presupuestar utiliza [Costos y cotizaciones](costos-en-desarrollo.md); para posibles pérdidas detectadas por IA consulta [Auditoría RP](auditoria-rp-persistencia.md).

{% hint style="info" %}
**Validación pendiente:** probar en Windows alta, edición, clonación pública/privada, permisos por cliente, precios, imágenes y selección del tablero en los demás formularios.
{% endhint %}

## Navegación relacionada

[Reporte de producción](reporte-de-produccion.md) · [Costos y cotizaciones](costos-en-desarrollo.md) · [Optimizadores](optimizadores.md) · [Índice de funcionalidades](README.md)
---

[← Volver al inicio de Cabinet Report](../README.md)
