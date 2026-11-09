---
description: >-
  Guía del Reporte de Producción: origen de datos, módulos, piezas, edición,
  comprobaciones técnicas, generación, optimización y revisión asistida por IA.
layout:
  width: wide
---

# Reporte de Producción

**CABINET REPORT · PLANIFICACIÓN Y PREPARACIÓN DE FABRICACIÓN**

## Del despiece al documento que recibe la planta

El **Reporte de Producción (RP)** reúne las piezas de un proyecto y permite revisar sus dimensiones, cantidades, materiales, espesores, vetas y cantos. Es el entorno central para **organizar y preparar la información de corte, canteo y montaje** antes de liberar el trabajo.

El RP combina cálculos y controles programados en Cabinet Report, operaciones de edición realizadas por el usuario y, cuando está habilitado, el [Revisor de Inteligencia Artificial](revisor-inteligencia-artificial.md).

{% hint style="warning" %}
**Responsabilidad técnica:** una validación satisfactoria no garantiza que el mueble pueda fabricarse o instalarse sin errores. El usuario debe confirmar planos, medidas reales, criterios constructivos y particularidades de su planta antes de generar u optimizar.
{% endhint %}

<figure><img src="../.gitbook/assets/image (5) (1) (1).png" alt="Captura original de la ventana Reporte de Producción de Cabinet Report"><figcaption><p>Entorno principal de revisión de piezas y módulos.</p></figcaption></figure>

## ¿Qué quieres hacer con el RP?

{% columns %}
{% column width="50%" %}
### 🧩 Preparar o corregir un despiece

Consulta el [Creador de módulos](creador-de-modulos.md) y el [Creador de piezas](creador-de-piezas.md) si debes ajustar estructuras o fórmulas.

### 🤖 Revisar antes de generar

Usa el [Revisor IA](revisor-inteligencia-artificial.md) como apoyo y comprueba el registro de decisiones en [Auditoría RP](auditoria-rp-persistencia.md).
{% endcolumn %}
{% column width="50%" %}
### ⚙️ Planificar el corte

Después de validar el RP, consulta los [Optimizadores](optimizadores.md) para tableros, perfiles o superficies.

### 🛒 Preparar compras

Continúa con el [Reporte de compras](reporte-de-compras.md) cuando necesites organizar materiales.
{% endcolumn %}
{% endcolumns %}

## 1. Formas de iniciar un reporte

Desde el menú de Reporte de Producción, según los permisos y la versión instalada, se contemplan estas rutas:

| Origen | Uso recomendado | Consideración |
| --- | --- | --- |
| **Importación CSV de Promob / Cut Pro** | Recibir un despiece generado en una herramienta externa. | Verificar encabezados, formato, materiales y resultados de la conversión. |
| **Archivo TXT de Cabinet Report** | Recuperar información de piezas ya organizada para el sistema. | Comprobar el cliente, ambiente y la correspondencia con el proyecto. |
| **Conversión de RP existente a TXT** | Reutilizar o reconstruir un origen editable. | Revisar nuevamente los datos convertidos. |
| **Reporte nuevo o manual** | Comenzar con una estructura inicial y agregar módulos o piezas. | Se requieren datos de identificación y una carpeta de trabajo. |

El menú contiene opciones diferenciadas; no todas las importaciones ni integraciones externas están disponibles para todos los clientes. Las operaciones dependen de los controles de acceso correspondientes.

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1).png" alt="Opciones originales de entrada al Reporte de Producción"><figcaption><p>Opciones de apertura y creación del reporte.</p></figcaption></figure>

## 2. Comprender la información del RP

| Dato | Qué debes verificar |
| --- | --- |
| **Cliente y ambiente** | Que la producción corresponda al proyecto correcto. |
| **Módulo e identificadores** | Que el conjunto esté identificado sin confundir piezas sueltas con piezas pertenecientes a un módulo. |
| **Pieza y cantidad** | Función de la pieza y unidades necesarias para la fabricación. |
| **Ancho y largo** | Medidas de corte efectivas, orientación y unidades utilizadas en el reporte. |
| **Espesor y material** | Compatibilidad entre la pieza y el tablero seleccionado. |
| **Veta** | Dirección requerida según el diseño y la ficha del material. |
| **Cantos** | Bordes superior, inferior, derecho e izquierdo que deban recibir canteo. |

La información técnica se representa en el archivo de piezas de Cabinet Report, con campos identificadores y atributos como **ID, CLIENTE, AMBIENTE, MODULO, CANT, PIEZA, ESP, ANCHO, LARGO, MATERIAL, VETA y CANTO** por lado.

### Módulos y piezas sueltas

- **Módulos:** conjuntos constructivos identificados por su nombre y ficha técnica. Pueden comprender varias piezas y asociarse con información adicional del proyecto.
- **Piezas sueltas:** elementos que se controlan individualmente y no deben confundirse con un módulo completo.
- **Cantidad de módulos frente a cantidad de piezas:** son magnitudes diferentes. Una producción con varios conjuntos fusionados exige revisar tanto las cantidades por pieza como la cantidad real de módulos.

{% hint style="info" %}
**Ejemplo:** tres módulos de estructura idéntica pueden quedar representados por piezas con cantidades agregadas; esto no significa que tres piezas duplicadas constituyan necesariamente un error. Se debe confirmar si son tres módulos iguales o un único conjunto compuesto antes de unificar filas.
{% endhint %}

## 3. Vista Técnica y ficha de un módulo

La Vista Técnica reúne, cuando existe la información correspondiente, **nombre, tipo, profundidad, ancho, alto, código, identificador técnico y cantidad** del módulo. También puede ofrecer contexto de **observaciones, apertura, giro, tipo de sobre y estilo personalizado**, según la definición y las herramientas disponibles.

Estos atributos son referencias para interpretar correctamente las piezas: **no todas las dimensiones de las piezas tienen que coincidir con las dimensiones exteriores del mueble**.

1. Selecciona el módulo correspondiente en la vista de trabajo.
2. Revisa sus medidas generales y su tipo constructivo.
3. Contrasta costados, bases, tapas, puertas, entrepaños y otras piezas con el diseño.
4. Comprueba si las medidas provienen de una fórmula o de una edición manual.
5. Guarda los cambios y vuelve a examinar las piezas afectadas.

**Atención:** modificar el alto de un costado o invertir ancho y largo puede alterar la posibilidad de montaje, incluso cuando los demás campos estén completos.

## 4. Materiales, espesores, vetas y cantos

Antes de generar los documentos, verifica que el material seleccionado sea el correcto y que el espesor de la pieza responda a la especificación del tablero. La existencia de un nombre parecido en un catálogo **no demuestra equivalencia técnica**.

En las piezas con veta direccional, confirma su orientación en relación con el mueble y el proceso de corte. Para el canteo, comprueba **qué lados reciben canto**, su tipo y su espesor. Las necesidades de excedente, repasado o reducción de pieza dependen del proceso y de las configuraciones aplicables.

{% hint style="warning" %}
No sustituyas automáticamente un tablero de 4 mm por otro de 3, 3,5 o 4,2 mm. Una referencia comercial similar requiere confirmar material, tolerancias, composición, dimensiones y autorización técnica.
{% endhint %}

## 5. Variables y fórmulas por cliente

Cabinet Report dispone de definiciones y parámetros de producción que pueden afectar los cálculos de piezas: **luces y separaciones, golas, espesores, ranuras y otras reglas constructivas**.

- Revisa que la fórmula aplique a **esa pieza y a ese módulo**, no únicamente a otra pieza con nombre parecido.
- Comprueba los **valores efectivos del cliente**, que pueden diferir de una definición general.
- Un valor configurado como **cero** puede ser válido: no debe interpretarse automáticamente como ausencia del parámetro.
- Las puertas y otras piezas pueden requerir restar luces por uno o ambos lados, según la fórmula aplicable.
- Cuando una variable o procedencia no esté acreditada, evita asumir una medida esperada exacta.

**Ejemplo ilustrativo:** una puerta exterior vinculada a una abertura de 450 mm no tiene por qué medir 450 mm si la fórmula considera luces efectivas. Verifica la fórmula y sus parámetros antes de tratar la diferencia como un error.

Para crear o revisar definiciones reutilizables, consulta el [Creador de módulos](creador-de-modulos.md) y el [Creador de piezas](creador-de-piezas.md).

## 6. Herramientas de edición y reorganización

Según el contexto de la selección y los permisos disponibles, el RP incorpora operaciones de trabajo como las siguientes:

| Operación | Para qué sirve | Comprobación posterior |
| --- | --- | --- |
| **Editar dimensiones, cantidad y propiedades** | Ajustar información de una pieza. | Confirmar que la corrección respete el diseño. |
| **Duplicar o replicar** | Reutilizar piezas o módulos. | Revisar cantidades e identificadores. |
| **Fusionar, agrupar o reorganizar** | Consolidar piezas o conjuntos compatibles. | No combinar funciones ni especificaciones incompatibles. |
| **Mover a piezas sueltas** | Separar elementos del módulo al que estaban asociados. | Revisar su clasificación y trazabilidad. |
| **Multiplicar o dividir** | Escalar cantidades en las categorías compatibles. | Verificar las reglas numéricas de cada categoría. |
| **Invertir ancho y largo** | Corregir orientación de medidas seleccionadas. | Confirmar veta, cantos y función de la pieza. |
| **Eliminar o renombrar** | Corregir la estructura del listado. | Comprobar que no se pierdan piezas necesarias. |

También pueden integrarse **zócalos, accesorios, ferretería de montaje e instalación, tubos y perfiles tipo gola**. Su captura y los documentos derivados dependen de las funcionalidades configuradas.

{% hint style="info" %}
**Buena práctica:** después de cada cambio estructural, compara el listado con la ficha del módulo y revisa los totales. Nunca interpretes una sugerencia de unificación como autorización para modificar automáticamente piezas incompatibles.
{% endhint %}

## 7. Comprobaciones antes de fabricar

Usa esta secuencia como control práctico:

1. **Identidad:** cliente, ambiente, referencia y módulo correctos.
2. **Integridad:** están todas las piezas requeridas y sus cantidades corresponden a las unidades reales.
3. **Geometría:** ancho, largo, espesor, orientación y relaciones entre piezas coinciden con el diseño.
4. **Materiales:** tableros, veta y especificaciones apropiadas.
5. **Canteo:** lados, espesores, acabados y preparación de repasado acordes con el proceso.
6. **Complementarios:** herrajes, accesorios, zócalos, tubos y perfiles necesarios.
7. **Decisiones pendientes:** revisar advertencias del sistema y, cuando corresponda, los hallazgos del Revisor IA.

Las comprobaciones programadas pueden ayudar a localizar inconsistencias conocidas. La cobertura **no es universal** y puede variar con los datos de entrada y la versión.

## 8. Generar u optimizar la producción

**Generar producción** y **Optimizar producción** son acciones diferentes. El RP puede preparar **reportes Excel**, archivos técnicos de intercambio y listados relacionados con los materiales o los complementarios aplicables. La optimización prepara salidas para procesos o herramientas específicas en función del material y la configuración.

1. Completa la revisión técnica y verifica el estado de la producción.
2. Si utilizas el [Revisor IA](revisor-inteligencia-artificial.md), examina sus resultados y decisiones.
3. Comprueba los avisos o consentimientos que solicite la aplicación.
4. Ejecuta la operación de **Generar** u **Optimizar** que corresponda.
5. Revisa los documentos producidos antes de entregarlos a corte, canteo, almacén o montaje.

Cuando se intenta generar sin una revisión IA completada, el programa incluye una **confirmación del usuario**; una autorización para continuar **no equivale a un resultado productivo exitoso**. También puede solicitar consentimiento al continuar con hallazgos pendientes.

{% hint style="warning" %}
**No confundas generar con optimizar.** Comprueba el tipo de archivo obtenido y su compatibilidad con la maquinaria o el flujo de trabajo correspondiente. Un archivo generado no acredita por sí solo la fabricación correcta.
{% endhint %}

## 9. Archivos y trazabilidad

El flujo utiliza información de piezas en **TXT**, puede mantener **metadatos técnicos XML** y dispone de un **XML de Auditoría RP** para registrar hechos y decisiones vinculados a la producción. Estos archivos cumplen funciones diferentes; no deben intercambiarse ni editarse manualmente sin respaldo.

Para entender la conservación de revisiones, la asociación de identidades y las limitaciones de recuperación, consulta [Auditoría RP y persistencia](auditoria-rp-persistencia.md).

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1).png" alt="Imagen original complementaria del flujo de Reporte de Producción"><figcaption><p>El reporte organiza la transferencia de información hacia la fabricación.</p></figcaption></figure>

## Continúa el flujo

[Revisor de Inteligencia Artificial](revisor-inteligencia-artificial.md) · [Auditoría RP y persistencia](auditoria-rp-persistencia.md) · [Optimizadores](optimizadores.md) · [Índice de funcionalidades](README.md)

---

[**🏠 Volver al portal principal de Cabinet Report**](https://danielmelendez-pma.github.io/cabinet-report-partners/)
