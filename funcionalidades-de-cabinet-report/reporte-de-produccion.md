# Reporte de Producción

### 🏭 Reporte de Producción – Cabinet Report

La sección **Reporte de Producción** es el **núcleo operativo** donde se revisa, valida y prepara toda la información necesaria para iniciar la fabricación.\
Aquí convergen **módulos, piezas, materiales, cantos y herrajes**, y es donde Cabinet Report aplica sus **algoritmos de control** para reducir errores antes de llegar a planta.

***

<figure><img src="../.gitbook/assets/image (5) (1) (1).png" alt=""><figcaption></figcaption></figure>

***

### 🎯 ¿Qué es el Reporte de Producción?

Es el entorno donde se **verifica pieza por pieza** que todo lo planificado cumple con las reglas técnicas de fabricación, garantizando que la información enviada a corte, canteo, montaje y almacén sea **consistente, clara y confiable**.

***

### 🔍 Validaciones automáticas del sistema

Dentro del Reporte de Producción, Cabinet Report revisa automáticamente que cada pieza cumpla con lo siguiente:

#### ✔️ Validación de tableros

* El material utilizado **exista en la base de datos**.
* El **espesor del tablero** coincida con el espesor de la pieza.
* Las **dimensiones de la pieza no excedan** el tamaño del tablero.
* La **veta de la pieza** coincida con la veta del tablero.
* Acceso con un clic a la **ficha del tablero** para validar imagen, veta y especificaciones.

***

#### ✔️ Validación de piezas

* Que todas las piezas tengan **medidas definidas**.
* Que cumplan con la **medida mínima de corte y canteo**.
* Control de piezas duplicadas o inconsistentes.
* Conteo en tiempo real de:
  * **Cantidad de piezas**
  * **Cantidad de módulos**

***

#### ✔️ Validación de cantos

* Consistencia en nombres y espesores de cantos.
* Cálculo automático del **metraje total de cantos** por tipo.
* Identificación de:
  * Necesidad de **activar bloque de repasado** en enchapadora.
  * Necesidad de **reducir pieza** según espesor del canto.
* Cálculo de **cantos especiales** para piezas enchapadas.
* Validación de piezas que deben:
  * Cortarse con **excedente**
  * Repasarse a medida final antes del canteo

***

#### ✔️ Control avanzado de producción

* Multiplicar o dividir producción **pieza por pieza** automáticamente.
* Invertir medidas de piezas seleccionadas con un solo clic.
* Agrupar piezas existentes para **crear nuevos módulos**.
* Renombrar módulos sin editar pieza por pieza.
* Replicar módulos completos de forma automática.

***

### 🧩 Gestión integral desde una sola ventana

Dentro del Reporte de Producción también puedes agregar y gestionar:

* Zócalos
* Accesorios
* Ferretería de montaje
* Ferretería de instalación
* Tubos
* Perfiles tipo Gola

Todo queda vinculado directamente al mismo reporte.

***

### ⚙️ Generación final del Reporte de Producción

Cuando el reporte está listo, Cabinet Report ejecuta automáticamente sus algoritmos finales y realiza lo siguiente:

#### 📄 Archivos generados

* Genera el archivo **Excel – Reporte de Producción** con todas las piezas estructuradas.
* Inserta referencias claras de:
  * Tableros
  * Cantos
  * Uso dentro del mueble (para operadores y montaje)
* Verifica que **todas las piezas estén incluidas** antes de exportar.

***

#### 📐 Optimización automática

* Genera archivos de **optimización por tipo de aglomerado**, listos para el optimizador.
* Genera archivos de optimización para:
  * Zócalos
  * Golas
  * Tubos
  * Perfiles especiales

***

#### 📦 Listados para almacén

* Genera listados automáticos de:
  * Accesorios
  * Ferreterías
  * Herrajes\
    Listos para ser entregados a almacén o despacho de producción.

***

### 📂 ¿Cómo puedes crear un Reporte de Producción?

Puedes iniciar un Reporte de Producción a partir de:

* 📄 **Archivo CSV de Promob**
* 📄 **Archivo TXT de Cabinet Report**
* 🔁 Convirtiendo **RP existente a TXT de Cabinet Report**
* 🆕 **Reporte en blanco de Cabinet Report**

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Esto te permite integrarte fácilmente a distintos flujos de trabajo o sistemas externos.

***

### ✅ Beneficio clave

El Reporte de Producción de Cabinet Report actúa como un **filtro técnico previo a fábrica**, reduciendo errores humanos, reprocesos y desperdicios, y asegurando que cada área de producción reciba información **clara, validada y lista para ejecutar**.

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

---

[← Volver al inicio de Cabinet Report](../README.md)
