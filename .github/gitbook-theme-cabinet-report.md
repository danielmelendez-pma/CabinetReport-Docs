# Identidad visual y navegación global — Cabinet Report / GitBook

**Actualización:** 2026-11-08 · Etapa 10  
**Estado:** navegación de respaldo implementada en 52 páginas Markdown; personalización **global pendiente de ejecución y comprobación** en administración de GitBook.  
**Referencia gráfica:** portal oficial `cabinet-report-partners`, archivos `portal.css`, `cabinet-header.css` e `index.html` en `main`.

## Objetivo y límites

Aproximar **todos los sitios GitBook** de Cabinet Report (documentación y curso) a la experiencia del portal GitHub Pages, sin cambiar rutas, precios, licencias ni navegación nativa de documentación. La plataforma GitBook administra su propio encabezado, menú lateral y estilos: no se promete igualdad CSS píxel a píxel ni se debe inyectar HTML/CSS/JS no admitidos en Markdown.

El repositorio de documentación controla contenido Markdown/Git Sync; el panel **Customize** controla la presentación pública del sitio y **no se actualiza mediante commits de este repositorio**. El curso es un sitio/espacio distinto; la misma configuración debe revisarse allí por separado.

## Valores de diseño oficiales

| Elemento | Valor objetivo | Observación |
| --- | --- | --- |
| Fondo principal | `#111216` | Portal principal |
| Paneles | `#242424` | Paleta Cabinet Report |
| Separadores/contornos | `#3C3C3C` | Paleta Cabinet Report |
| Acentos, enlaces destacados y foco | `#F08080` | LightCoral |
| Texto alternativo/detalles | `#FFE4E1` | MistyRose |
| Texto principal | `#FFFFFF` | Blanco |
| Color secundario | `#000000` | Negro, no como texto sobre fondo oscuro |
| Tipografía | Sans serif legible, idealmente Inter o la opción más próxima | Depende de opciones GitBook |

Si el plan ofrece **Custom** y permite escoger header links/background, usar `#111216` en fondo de encabezado y LightCoral en los enlaces. En caso contrario, elegir un tema nativo oscuro con contraste y acento lo más cercano posible. Revisar el resultado realmente publicado antes de declararlo aplicado.

## Barra superior (objetivo para GitBook)

Orden y enlaces para el sitio de documentación y, si es posible, el curso:

1. **Inicio** → https://danielmelendez-pma.github.io/cabinet-report-partners/
2. **Documentación** → https://cabinet-report.gitbook.io/cabinet-report-docs/
3. **Partners** → https://danielmelendez-pma.github.io/cabinet-report-partners/partners.html
4. **Cursos** → https://cabinet-report.gitbook.io/curso-de-cabinet-report/
5. **Manual** → https://cabinet-report.gitbook.io/cabinet-report-docs/manual-de-usuario

**Branding:** utilizar el logo oficial **ovalado** en cabecera cuando se busque coherencia exacta con el header del portal, y el **circular** como icono/fav icon o elemento gráfico de portada; ambos archivos existen en el portal. La portada de GitBook ya incorpora el logo circular. Si la interfaz admite `Primary link`/destino del logo, apuntarlo a **Inicio** en GitHub Pages.

### Pasos administrativos

1. Entrar al panel del Docs site **Cabinet Report** de GitBook.
2. Abrir **Customize → General / Styling / Themes** (los nombres pueden variar con la versión de GitBook).
3. Seleccionar modo oscuro; configurar paleta, fondo y enlaces mediante opciones soportadas. Comprobar texto, tabla, avisos, imágenes y contraste.
4. Abrir **Customize → Layout → Header** y añadir los cinco vínculos anteriores como enlaces de encabezado, en ese orden. Permitir el colapso nativo en móvil si el espacio es insuficiente; no forzar una fila desbordada.
5. En **Customize → Configure → Primary link**, si aparece el control, hacer que el logotipo lleve al portal principal. Configurar los logotipos e iconos existentes.
6. Guardar/publicar cambios. Abrir un navegador **sin sesión de administración** y verificar los cinco enlaces, el logotipo y la apariencia real.
7. Repetir el procedimiento en el sitio **Curso de Cabinet Report**; su contenido/ajustes **no** pertenecen al repositorio `CabinetReport-Docs`.
8. Comprobar **Git Sync = Synced** y contrastar la portada pública con `README.md` de `main`.

**Importante:** la navegación textual añadida a las 52 páginas ofrece accesos de respaldo y **no sustituye** esta barra superior nativa. Si se activa el encabezado global, revisar si el menú textual de respaldo causa redundancia visual; no eliminarlo antes de verificar que el encabezado se muestra en todas las páginas y móviles.

## Criterios de aceptación visual

- **Escritorio (1440 px), laptop (1366×768 aprox.), tablet (768 px), móvil (390/430 px):** legibilidad, apertura del menú nativo, focos visibles, ausencia de cortes, tabla de siete planes consultable por desplazamiento horizontal.
- Portada: marca real y enlaces al curso/manual; ficha técnica, RP, Revisor IA, Auditoría RP, Costos y suscripciones: navegación/retorno al portal.
- Ningún control coral con texto de bajo contraste. Verificar modo claro si el lector puede activarlo.
- Confirmar apertura de las seis fichas interactivas con `?plan=`; el plan Gratis no usa `?plan=gratis`.
- Evaluar tamaño de las imágenes y ancho de tablas con el tema oscuro real; no modificar capturas de Windows a ciegas.
- Para recursos gráficos nuevos, solicitar capturas Windows auténticas y ocultar datos personales antes de publicar.

## Bloqueo prioritario de publicación detectado

La extracción de la portada pública en 2026-11-08 devolvió **«Un flujo de trabajo, de principio a fin»** y no mostró **«Ir al curso»**. El archivo `README.md` del HEAD `0458df7f08d5c754749ee7a45503503a8b7fe130` sí contiene **«Tu primera producción, paso a paso»** y el enlace al curso. Esto evidencia una **diferencia entre contenido publicado extraído y repositorio**, pero no identifica la causa. Es imprescindible revisar estado real de Git Sync, publicación del Docs site y caché antes de atribuirla. No modificar Markdown para intentar forzar la sincronización.

## Referencias

- [Guía oficial de identidad GitBook](https://gitbook.com/docs/guides/docs-best-practices/how-to-create-branded-documentation) — temas, colores, enlaces del encabezado y logo.
- [GitBook changelog 2025](https://gitbook.com/docs/changelog/2025-product-updates) — destino personalizado del logo / Primary link.
- [Guía oficial de publicación 2026](https://gitbook.com/docs/guides/editing-and-publishing-documentation/complete-guide-to-publishing-docs-gitbook) — Customize y restricciones por plan.

**No se aplicaron ni validaron cambios en la administración de GitBook desde este repositorio.**
