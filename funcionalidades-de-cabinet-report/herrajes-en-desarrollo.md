---
description: >-
  Herrajes, accesorios y ferretería de montaje e instalación; catálogos,
  permisos, relaciones con producción y archivos auxiliares TXT.
layout:
  width: wide
---

# Herrajes

**CABINET REPORT · ACCESORIOS Y FERRETERÍA PARA FABRICACIÓN**

## Diferentes elementos, distintos momentos de uso

Cabinet Report dispone de funciones de **herrajes** organizadas en tres áreas: **Accesorios**, **Ferretería de montaje** y **Ferretería de instalación**. Son herramientas implementadas y sujetas a contexto, permisos y datos de catálogo.

{% hint style="info" %}
**Disponibilidad:** los permisos de edición, el funcionamiento sin conexión y la vinculación con archivos TXT pueden variar según la acción, la versión y el acceso utilizado.
{% endhint %}

## 1. Elegir el tipo de herraje

| Sección | Ejemplos de uso |
| --- | --- |
| **Accesorios** | Elementos complementarios utilizados por el mueble o su mecanismo. |
| **Ferretería de montaje** | Insumos y elementos asociados al armado de componentes. |
| **Ferretería de instalación** | Elementos destinados al montaje definitivo en obra. |

Las ventanas de mantenimiento se abren desde el selector de **Herrajes**. El mismo catálogo puede emplearse también como referencia desde un creador de módulos o desde producción, pero esos contextos no conceden automáticamente permisos de administración.

## 2. Catálogo público y privado

Las operaciones maestras utilizan el catálogo **TblAccHerrajes** y aplican filtros de visibilidad y cliente. En términos generales:

- Los elementos **públicos** están sujetos a administración por el perfil autorizado.
- Los elementos **privados** corresponden al cliente propietario, con controles antes de modificarlos o eliminarlos.
- Existen acciones de consulta y, en contextos permitidos, incorporación o clonación de una referencia al catálogo del cliente.

No elimines registros compartidos sin confirmar su alcance y relación con otros usuarios.

## 3. Herrajes dentro de producción

Desde el [Reporte de producción](reporte-de-produccion.md), las herramientas auxiliares permiten revisar los herrajes correspondientes, operar con las líneas del **TXT** auxiliar y sincronizar esos archivos **solo cuando el contexto de producción está realmente activo**.

| Contexto | Alcance |
| --- | --- |
| **Mantenimiento de herrajes** | Alta, edición o eliminación de registros maestros, con permisos. |
| **Reporte de producción** | Trabajo con herrajes y ferretería de la producción actual; no es un editor global de catálogo. |
| **Catálogo o creador de módulos** | Consulta o selección de relaciones técnicas sin reescribir automáticamente TXT de RP. |

{% hint style="warning" %}
Los botones de agregar al catálogo maestro no deben confundirse con **Agregar al TXT**. Al trabajar fuera del modo producción, el código incorpora protecciones para impedir escrituras accidentales del reporte productivo.
{% endhint %}

## 4. Restricciones de conexión

El alta de referencias maestras está limitada en modo **offline**. La lectura y la gestión de datos previamente disponibles pueden variar según el catálogo local; comprueba el modo activo antes de intentar modificar registros.

## 5. Verificaciones recomendadas

Confirma las unidades y cantidades, la clasificación entre montaje e instalación, la identidad del cliente, el permiso de edición y la presencia del archivo auxiliar esperado. Comprueba luego los resultados en el [Reporte de compras](reporte-de-compras.md) cuando corresponda.

## Sigue explorando

[Reporte de producción](reporte-de-produccion.md) · [Reporte de compras](reporte-de-compras.md) · [Creador de módulos](creador-de-modulos.md)

---

[← Volver al inicio de Cabinet Report](../README.md)
