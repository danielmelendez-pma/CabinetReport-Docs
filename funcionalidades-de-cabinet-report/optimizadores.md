---
description: >-
  Optimizadores de tableros, perfiles y superficies; preparación de piezas,
  parámetros de corte, resultados, exportación y compatibilidad de archivos.
layout:
  width: wide
---

# Optimizadores

**CABINET REPORT · APROVECHAMIENTO DE MATERIALES Y PREPARACIÓN DEL CORTE**

## Optimiza de acuerdo con el material

Cabinet Report incorpora herramientas diferenciadas para organizar cortes de **tableros**, **perfiles lineales** y **superficies o sobres**. Cada herramienta recibe piezas, valida medidas y genera una distribución bajo parámetros que deben revisarse antes de fabricar.

{% hint style="warning" %}
**No existe un único algoritmo para todos los materiales.** La viabilidad depende de medidas, cantidades, veta, posibilidad de giro, ancho de corte, resane, disponibilidad introducida y restricciones de la herramienta elegida.
{% endhint %}

## 1. Optimización de tableros

<figure><img src="../.gitbook/assets/image (20).png" alt="Captura original del optimizador de tableros"><figcaption><p>Distribución de piezas sobre planchas y retazos de material compatible.</p></figcaption></figure>

El optimizador de tableros permite cargar piezas desde **TXT** de producción o introducirlas en la grilla, definir las planchas y retazos disponibles **para el cálculo**, y seleccionar parámetros como **espesor de sierra**, **resane** y **giro**.

En el código se identifican alternativas de ordenamiento **Guillotina**, **MenosMas** y **MasMenos**. Las piezas se agrupan por material; la aplicación muestra las piezas que no pudieron colocarse y ofrece resultados visuales y exportación a Excel.

1. Comprueba que el tablero tenga ancho, largo, cantidad y material válidos.
2. Carga el archivo TXT del [Reporte de producción](reporte-de-produccion.md) o incorpora piezas manualmente.
3. Verifica dimensiones, espesor, veta y orientación; configura corte y resane.
4. Ejecuta la optimización y examina **planchas empleadas, sobrantes y piezas sin colocar**.
5. Exporta el resultado y valídalo contra las exigencias de tu maquinaria y operador.

{% hint style="info" %}
La «cantidad en stock» del optimizador es una **entrada para el plan de corte**, no una certificación de existencias físicas ni un movimiento automático de almacén.
{% endhint %}

## 2. Optimización de perfiles

<figure><img src="../.gitbook/assets/image (21).png" alt="Captura original del optimizador de perfiles"><figcaption><p>Planificación de cortes lineales para materiales de longitud definida.</p></figcaption></figure>

El optimizador de perfiles contempla materiales como **tubos, golas, zócalos y otros perfiles** admitidos por el catálogo. Reúne longitudes, cortes y tramos; permite cargar TXT, preparar el material disponible y generar una optimización lineal exportable a Excel.

Debes revisar **longitud comercial**, cantidad de tramos, pérdida de sierra y denominación del perfil. Un perfil sin longitud válida o que no corresponda al material seleccionado puede impedir un resultado utilizable.

## 3. Optimización de sobres y superficies

<figure><img src="../.gitbook/assets/image (22).png" alt="Captura original del optimizador de sobres y superficies"><figcaption><p>Preparación de piezas sobre planchas de superficie según sus dimensiones.</p></figcaption></figure>

La ventana del optimizador de superficies incluye el tratamiento de piezas como **sobre, zócalo, fascia y backsplash**. Permite **importar y exportar CSV**, indicar dimensiones de plancha, espesor de corte, resane, orientación/veta y visualizar la distribución, con exportaciones según el flujo disponible.

La compatibilidad de un material no acredita automáticamente que todas las condiciones de veta, unión, biselado, manipulación o mecanizado estén resueltas por el programa.

## 4. Archivos externos y formatos

El flujo de [Reporte de producción](reporte-de-produccion.md) contempla selección de optimizador y salidas para determinados formatos de intercambio. Existen rutinas de conversión y tratamiento de archivos relacionados con **Optiplanning** e **Itemizer**; su disponibilidad depende del modo seleccionado y del formato de entrada.

| Entrada o salida | Uso |
| --- | --- |
| **TXT de piezas RP** | Fuente de datos productivos para optimización compatible. |
| **CSV** | Intercambio con determinadas herramientas, incluido el flujo de superficies. |
| **Excel (.xlsx)** | Reportes de optimización, órdenes o resultados según la herramienta. |
| **Archivos específicos de proveedor** | Intercambio condicionado por el optimizador externo y sus reglas. |

No presupongas una integración directa con toda maquinaria: **comprueba el archivo generado, su versión y el formato admitido por el proveedor**.

## 5. Trabajo conectado y sin conexión

Hay rutas de carga de catálogos desde el almacenamiento local al trabajar **offline** en optimizadores de tableros y perfiles. Si no existe una copia local, el sistema puede exigir una conexión previa para actualizarla. Las acciones que requieren catálogos o registros remotos pueden tener restricciones diferentes.

## 6. Lista de comprobación

- Confirma la correspondencia de material, espesor, veta y dimensiones de cada pieza.
- Comprueba la cantidad realmente disponible en taller.
- Revisa espesor de sierra, resanes, retazos y posibilidad de giro.
- Inspecciona las piezas que quedan sin cortar antes de exportar.
- Valida visualmente y con el operario la orden de corte antes de fabricar.

## Navegación relacionada

[Stock de tableros](stock-de-tableros.md) · [Reporte de producción](reporte-de-produccion.md) · [Reporte de compras](reporte-de-compras.md) · [Orden de producción](orden-de-produccion.md)

---

[← Volver al inicio de Cabinet Report](../README.md)
