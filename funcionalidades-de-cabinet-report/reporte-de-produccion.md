# Reporte de Producción

Dentro del entorno de Reporte de Producción es donde revisas y preparas cada pieza de cada módulo para generar los reportes necesarios para dar inicio a la fabricación.

<figure><img src="../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

## Que puedes hacer dentro de Reporte de Producción?

Cabinet Report hace lo siguiente por tí dentro de la funcionalidad de Reporte de Producción para ayudar a no cometer muchos errores:

* Revisa si los tableros utilizados están registrados en la base de datos para de esa manera verificar si cada pieza cumple con:
  * Espesor correcto
  * Que la medida de la pieza no exceda del tamaño del tablero
  * Que el espesor de la pieza coincida con el espesor del tablero
  * Que la veta de la pieza coincida con la veta del tablero
  * Si no estas seguro y necesitas ver imagen del tablero para validar la veta, puedes con un clic ver la ficha del tablero, previamente registrado en la base de datos
* Revisa si las piezas cumplen con la medida mínima de corte y canteo
* Revisa que todas las piezas cuentan con sus medidas
* Revisa que los cantos tengan consistencia y un espesor establecido para poder establecer si:
  * Si hay que activar el bloque de repasado en la enchapadora
  * Si hay que reducir la pieza, el espesor del canto antes de enviar a la seccionadora
* Si necesitas multiplicar la producción, Cabinet Report lo hace por ti, pieza por pieza
* Te lleva un conteo en tiempo real de la cantidad de piezas actuales
* Te lleva un conteo en tiempo real de la cantidad de módulos actuales
* Te calcula el metraje de cantos por cada tipo de canto de manera automática
* Si debes invertir medidas en algunas piezas, sólo indicas cual pieza y te hace la inversión automática
* Si quieres agrupar piezas existentes para crear un módulo, solo debes hacer unos clics y Cabinet Report hace el resto del trabajo
* Si necesitas cambiar el nombre del módulo, no lo debes hacer para cada pieza, sólo le indicas el nombre a Cabinet Report y lo cambia por ti
* Si quieres crear un módulo a partir de otro módulo existente, solo le indicas a Cabinet Report cual modulo quieres replicar y te lo hace de manera automática
* Dentro de la misma ventana de Reporte de Producción puedes agregar:
  * Zócalos
  * Accesorios
  * Ferretería de Montaje
  * Ferretería de Instalación
  * Tubos
  * Perfiles Gola
* Cuando ya estas listo para genear el reporte de producción, Cabinet Report activa los algoritmos de revisión y ocurre lo siguiente:
  * Revisa de manera automática pieza por pieza en busca de inconsistencias de todo lo listado arriba
  * Crea de manera automática el archivo excel "Reporte de Producción" de manera estructurada con todas las piezas
  * Le indicas a Cabinet Report en que parte de los muebles se utilizarán las referencias de tableros de aglomerados y cantos para que te lo pueda colocar en el reporte y le muestre la información a los operadores de máquina y montaje
  * Revisa por ti que el archivo excel "Reporte de Producción" contenga todas las piezas que has agregado y en caso de haber alguna inconsistencia te lo hará saber para que haga tu revisión visual
  * Te genera los archivos de Optimización por cada tipo de aglomerado exclusivo para tu programa de optimización y así evitar tabular de manera manual
  * Te genera los archivos de listado de Accesorios, Ferreterías y Herrajes listos para que los entregues a tu departamento de almacén y te despachen o necesario para tu producción
  * Te genera de manera automática los archivos de Optimización de los perfiles como Zócalo, Golas, Tubos, Etc.
