# CABINET REPORT — Configuración oficial de identidad y navegación en GitBook

**Revisión:** 2026-11-08, Etapa 11.  
**Estado:** especificación lista para aplicar; **NO consta que el tema, la barra nativa o el enlace del logo estén configurados en GitBook**.  
**Repositorios:** documentación `danielmelendez-pma/CabinetReport-Docs` (`main`); portal `danielmelendez-pma/cabinet-report-partners` (`main`).  
**Informe:** [Auditoría Etapa 11](documentation-audit-etapa-11-2026-11-08.md).

> **Distinción esencial:** Git Sync actualiza los archivos y el contenido de un espacio, pero no demuestra que los ajustes globales del sitio estén publicados. Las preferencias de apariencia y los enlaces nativos se administran mediante **GitBook → Docs site → Customization** o su API autenticada. Este repositorio no contiene credenciales de GitBook ni controla el sitio independiente del curso. No introducir CSS/JS en Markdown para simular una cabecera global.

## 1. Referencia visual y activos oficiales

La referencia es el [portal principal](https://danielmelendez-pma.github.io/cabinet-report-partners/), específicamente `index.html`, `portal.css` y `cabinet-header.css` del repositorio de portal. La cabecera real del portal usa `#151519` y no exactamente el mismo fondo del cuerpo; el valor **#111216** sigue siendo el fondo general.

| Elemento | Color de referencia | Uso previsto en GitBook |
| --- | --- | --- |
| Fondo general | `#111216` | Selección nativa de tema oscuro; aproximar donde la interfaz lo permita |
| Cabecera del portal | `#151519` | Fondo del encabezado **si existe selector avanzado** |
| Paneles | `#242424` | Superficies/sidebar donde exista opción nativa |
| Bordes | `#3C3C3C` | Separadores donde exista opción nativa |
| Principal/acento | `#F08080` (LightCoral) | Color primario y estados activos |
| Texto secundario destacado | `#FFE4E1` (MistyRose) | Detalles; evitarlo como fondo de texto claro |
| Texto principal | `#FFFFFF` | Tema oscuro |
| Enlaces normales del encabezado real | `#F0EAEF` | Header links, de existir selector propio |
| Negro | `#000000` | Elementos que realmente requieran negro; no usar texto negro sobre oscuro |

El encabezado HTML del portal usa enlaces de color cercano a blanco, y coral al pasar el cursor. Si GitBook permite un único color fijo para enlaces, usar `#F0EAEF` con primario `#F08080`; no prometer comportamiento hover idéntico. Seleccionar una fuente sans serif legible, preferentemente Inter si está disponible; usar la alternativa nativa más próxima.

**Activos oficiales que existen en el portal:**
- Logo **ovalado** del encabezado: `https://danielmelendez-pma.github.io/cabinet-report-partners/logo-ovalado.png`.
- Logo **circular** para favicon, portada y elementos destacados: `https://danielmelendez-pma.github.io/cabinet-report-partners/logo-redondo.png`.
- La portada de la documentación ya hace referencia al logo circular propio en `.gitbook/assets/Logo Redondo CR.png`.

No usar logotipos nuevos generados por IA ni inventar capturas del programa. Verificar visualmente el contraste/tamaño del logo seleccionado en **modo oscuro** y, si se ofrece modo claro, también en claro. Subir los archivos desde el portal original en caso de que GitBook solicite una carga, en vez de asumir que acepta URL.

## 2. Menú global nativo obligatorio

Configurar **cinco enlaces de cabecera** en el sitio Docs y repetirlos en el sitio independiente Curso:

| Orden | Etiqueta solicitada | URL de destino |
| --- | --- | --- |
| 1 | **Inicio** | https://danielmelendez-pma.github.io/cabinet-report-partners/ |
| 2 | **Documentación** | https://cabinet-report.gitbook.io/cabinet-report-docs/ |
| 3 | **Partners** | https://danielmelendez-pma.github.io/cabinet-report-partners/partners.html |
| 4 | **Cursos** | https://cabinet-report.gitbook.io/curso-de-cabinet-report/ |
| 5 | **Manual** | https://cabinet-report.gitbook.io/cabinet-report-docs/manual-de-usuario |

- **Inicio** debe abrir la raíz del portal en GitHub Pages, **nunca** la raíz interna de GitBook.
- Cuando el sitio ofrezca `Primary link` o destino del logotipo, usar exactamente la **misma URL de Inicio**.
- Mantener navegación de páginas, búsqueda y sidebar nativas de GitBook, y verificar que los cinco enlaces caben o se agrupan mediante las opciones **responsive nativas** en tablet y móvil.
- Para evitar una cabecera excesiva en pantallas reducidas, utilizar la posibilidad nativa de agrupación/desplegable si la interfaz la ofrece; no insertar HTML/CSS personalizados ni ocultar enlaces obligatorios. Si algún enlace debe agruparse, verificar que permanece accesible en no más de dos interacciones.
- El bloque textual ya existente en las **52 páginas** del repositorio es un **respaldo**; no es barra global ni sticky. **No eliminarlo** antes de comprobar header nativo en escritorio, móvil y rutas profundas de ambos sitios.

## 3. Procedimiento de administración: Documentación

1. Iniciar sesión en [GitBook](https://app.gitbook.com/) con permisos para administrar el sitio publicado **Cabinet Report Docs**.
2. Abrir el **Docs site** correspondiente a `https://cabinet-report.gitbook.io/cabinet-report-docs/` (no confundir el espacio de edición ni el sitio del curso). Abrir **Customization / Customize**.
3. En **General / Themes** o **Styling** (rótulos sujetos a cambios de GitBook):
   - Elegir un tema compatible con **modo oscuro**; fijar oscuro como predeterminado cuando el selector lo permita.
   - Color primario: `#F08080`; si existe opción **Custom**, fondo de cabecera `#151519`, color de enlaces de cabecera `#F0EAEF`, tint o color de fondo `#111216` *solo donde exista un control nativo para ello*.
   - Elegir tipografía legible y bordes/sombras sobrios. No forzar colores para superficies que GitBook no permita editar.
4. En **General / Branding** o zona de logo: subir logo ovalado oficial (versión legible para oscuro) y, cuando esté disponible, logo circular como favicon.
5. En **Layout → Header**, incorporar los cinco enlaces de la sección 2, en ese orden. Usar estilo de enlace y no cinco botones voluminosos. Configurar el menú responsive/desplegable si está disponible.
6. En **Layout**, configuración del propio header o campo **Primary link** (la ubicación exacta puede variar), cambiar el destino de logo/título al portal principal. Si esa opción no aparece o no la permite el plan, **anotar la limitación** y mantener `Inicio` en el menú y en el respaldo textual.
7. En **Configure** verificar comportamiento de enlaces externos, idioma de interfaz y navegación sin alterar innecesariamente la estructura del sitio. Elegir misma pestaña si se quiere una transición uniforme, comprobando que el retorno es comprensible.
8. Hacer **Preview** y después **Save**. Comprobar en una ventana de navegador ajena a la sesión del editor que el nuevo encabezado se ve realmente; guardar captura y fecha.
9. Comprobar la portada, una página funcional profunda, ficha de plan y tabla comparativa. Validar los cinco enlaces y el clic en el logo.

**Atención:** la API oficial de GitBook dispone de `site customization`, pero exige **token Bearer y IDs de organización/sitio**. No incluir secretos en el repositorio, en PR, capturas o chats. Este procedimiento prefiere el panel administrativo; no se ha invocado la API.

## 4. Procedimiento de administración: Curso

1. Abrir el **Docs site** que publica `https://cabinet-report.gitbook.io/curso-de-cabinet-report/`.
2. Repetir **tema, logo, favicon, colores, cinco enlaces de cabecera y destino del logo**; no asumir que comparte personalización con Documentación.
3. Confirmar que las páginas del curso y su sidebar mantienen títulos y rutas propias. La página **Inicio** del menú debe conducir al portal de GitHub Pages desde cualquier lección.
4. Guardar y verificar la **publicación pública** del curso por separado. Anotar si las opciones de personalización difieren por permisos o configuración de ese sitio.

## 5. Diagnóstico de sincronización y publicación — NO editar Markdown para forzar el resultado

**Hecho verificable en 2026-11-08:** la extracción textual de la portada pública devolvió `Un flujo de trabajo, de principio a fin`, un único enlace `Volver al portal principal de Cabinet Report` y **no** mostró `Ir al curso`. La lectura directa de `CabinetReport-Docs/main/README.md` en el HEAD `096501fb99084fe0d853e0924262802d8c1cc552` contiene `Tu primera producción, paso a paso`, el menú textual de **cinco enlaces** y `Ir al curso`. Esto **no demuestra por sí solo** el origen del desfase.

**Orden de comprobación, guardando evidencia de cada paso:**

1. Abrir el **espacio** usado por el Docs site. En integración **Git Sync**, comprobar: repositorio `danielmelendez-pma/CabinetReport-Docs`, rama `main`, sincronización habilitada, última ejecución, estado `Synced` o errores. Registrar fecha/hora, commit si se muestra y captura. Si se usa otro espacio o rama, documentarlo; no activar una resincronización destructiva.
2. En el **Docs site** de Documentación, comprobar que la sección pública apunta al **espacio realmente sincronizado** y a su contenido principal, sin una versión/variante distinta o borrador sin publicar.
3. Revisar si la revisión está **publicada** (no solamente en editor o preview). Abrir la portada pública en sesión privada; buscar exactamente `Tu primera producción, paso a paso`, `Ir al curso` y el menú `Inicio · Documentación · Partners · Cursos · Manual`.
4. Si el navegador muestra la versión nueva pero el extractor devuelve la vieja, sospechar **extracción/caché** y contrastar HTML/texto accesible con la vista real antes de tocar Git.
5. Si navegador y extractor muestran la versión anterior, comprobar estado de **publicación**, versión/espacio publicado y Git Sync. Si Git Sync figura correcto, revisar el destino del sitio y el estado del cambio publicado; no asumir que GitHub no sincroniza.
6. Si Git Sync informa fallo, registrar el mensaje completo y resolver el problema de integración/permisos, rama o conflicto desde el panel. No reemplazar `README.md` con texto artificial para activar otro commit.
7. Repetir publicación y navegación del curso desde su **propio sitio**; el repositorio de documentación **no es** evidencia de su estado de sincronización.

Un error de extracción, ausencia de acceso o respuesta de caché **no** equivale a prueba de fallo de Git Sync. Una discrepancia solo se considera resuelta con **lectura pública en navegador** y contenido equivalente al `README.md` correcto.

## 6. Matriz de aceptación responsive — pruebas reales pendientes

Abrir cada tamaño mediante **navegador con viewport real / DevTools**, sin confundir inspección estática de Markdown con una prueba visual.

| Viewport | Qué comprobar | Resultado exigido |
| --- | --- | --- |
| 1440 px ancho | Cabecera completa, logo ovalado, cinco vínculos, sidebar, color oscuro | Sin solapamientos ni enlaces faltantes |
| 1366 × 768 | Encabezado y primeras secciones, navegación y regreso | Legibilidad y altura de menú razonable |
| 768 px | Navegación responsive, búsqueda, sidebar y tablas | Se accede a los cinco enlaces |
| 390 px | Menú móvil, foco, scroll, fichas y tabla comparativa | Sin controles cortados; desplazamiento de tabla utilizable |
| 430 px | Comportamiento móvil alternativo y enlaces de cabecera | Retorno a Inicio y contenido legible |

Páginas representativas: portada, Manual, Curso, Funcionalidades, RP, Revisor IA, Auditoría RP, Creador de Módulos, Creador de Piezas, Costos, Optimizadores, Suscripciones y Tabla comparativa. Probar ambos sitios, teclado/foco y contrastes. GitBook controla el encabezado/sidebar: no puede garantizarse coincidencia exacta con `cabinet-header.css` ni fijar toda la documentación dentro de 768 px de altura.

Los controles `?plan=optimizador`, `basico`, `intermedio`, `profesional`, `empresarial` y `socio` se prueban **en el portal** mediante navegador. El plan Gratis no usa `?plan=gratis`. No modificar precios ni condiciones durante esta fase.

## 7. Activos visuales y resguardo

- `.gitbook/assets/banner.bmp`: **7.322.926 bytes** (auditoría previa), candidato a optimización solo tras comparación visual real.
- Existen tres grupos de imágenes con contenido SHA idéntico; conservar rutas y referencias mientras no se demuestre que una deduplicación es segura.
- No eliminar ni sustituir capturas de Windows sin cotejar el software real. Cuando hagan falta, solicitar ventana específica, versión, datos de demostración y ocultar información personal.
- Para quitar el menú textual duplicado en una fase posterior, exigir **antes** validación del header global en **Docs y Curso**, incluida versión móvil y ruta profunda. En este punto no hay esa evidencia.

## 8. Evidencia y cierre administrativo

Por **cada sitio** anotar: usuario/rol autorizante (sin secretos), fecha de cambios, captura de `Customization`, enlace público, esquema oscuro visible, cinco enlaces, destino real del logo, resultado en móvil y estado de publicación. Para **Docs** registrar además Git Sync y comparación de portada. Separar casillas **configurado en panel**, **guardado**, **observado en público**: no equivalen.

Fuentes oficiales:
- https://gitbook.com/docs/guides/docs-best-practices/how-to-create-branded-documentation
- https://gitbook.com/docs/guides/customizing-your-site/how-to-customize-your-sites-theme
- https://gitbook.com/docs/developers/gitbook-api/api-reference/docs-sites/site-customization
- https://www.gitbook.com/blog/new-in-gitbook-november-2025
- https://gitbook.com/docs/guides/editing-and-publishing-documentation/import-or-migrate-your-content-to-gitbook-with-git-sync
