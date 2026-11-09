# CABINET REPORT — Auditoría visual y publicación GitBook — Etapa 11

**Fecha:** 2026-11-08 (hora de Panamá)  
**Repositorio de cambios:** `danielmelendez-pma/CabinetReport-Docs`  
**Base de la rama:** `main` en `096501fb99084fe0d853e0924262802d8c1cc552`  
**Rama de trabajo:** `docs/etapa-11-tema-global-publicacion`  
**Objetivo:** unificar la navegación y la apariencia del sitio Documentación y del sitio Curso con la web oficial; diagnosticar publicación sin provocar cambios destructivos.

## 1. Verificación de base y etapa anterior

- GitHub reporta PR **#16 cerrado, merged**, fecha `2026-11-09T00:51:05Z` (2026-11-08, Panamá), commit de merge **`096501fb99084fe0d853e0924262802d8c1cc552`**.
- Antes de iniciar, `main` coincidía exactamente con ese SHA; el repositorio Docs tenía **cero PR abiertos**.
- Leídos `.github/documentation-audit-etapa-09-2026-11-08.md`, `.github/documentation-audit-etapa-10-2026-11-08.md`, `.github/gitbook-theme-cabinet-report.md`, `README.md`, `SUMMARY.md`, `gitbook-docs.yaml`.
- `SUMMARY.md`: **52 destinos Markdown distintos**. El diff confirmado del PR #16 contiene **54 archivos** (52 páginas + 2 internos); cada cambio incluye enlace de regreso a Inicio del portal. Es verificación del diff anterior, no una ejecución navegador.
- `gitbook-docs.yaml`: `Documentation`, contenido `./`, idioma `es-419`, sin alteraciones en esta etapa.
- Los nombres públicos de **Costos**, **Herrajes** y **Generador de QR** no contienen `(En desarrollo)`; se conservan sus rutas con nombres históricos.
- Se consultaron los CSS/HTML originales del portal: `cabinet-header.css`, `portal.css`, `index.html`. Se observó `#151519` en su header real; `#111216` es el fondo general y el color coral `#F08080` el acento.

## 2. Publicación pública contrastada tras PR #16

La consulta pública de `https://cabinet-report.gitbook.io/cabinet-report-docs/` realizada en esta etapa devolvió texto **anterior al HEAD de GitHub**:

| Componente | Publicación textual extraída | `main/README.md` |
| --- | --- | --- |
| Navegación bajo título | Un enlace: `Volver al portal principal de Cabinet Report` | Cinco: `Inicio · Documentación · Partners · Cursos · Manual` |
| Bloque de recorrido | `Un flujo de trabajo, de principio a fin` | `Tu primera producción, paso a paso` |
| CTA inicial | `Explorar funcionalidades` y `Abrir manual de usuario` | Ambos, más `Ir al curso` |

**Resultado:** hay discrepancia entre **extracción pública** y contenido vigente de `main`. **No es posible atribuirla de forma concluyente** a Git Sync, publicación diferida, versión/espacio mal conectado, caché o modo de extracción. No se modificó `README.md` para intentar arreglarla. La consulta pública del curso y la del portal no suministraron lectura completa estable mediante la herramienta de navegación textual; ello **no prueba inaccesibilidad para los visitantes**.

**Faltó acceso a:** estado administrativo `Git Sync → Synced`, enlace del espacio al Docs site publicado, revisión pendiente/draft y registros de publicación. El navegador conectado del usuario no estaba disponible en esta sesión (requiere contexto de extensión asociado), por lo que **no hubo inspección visual autenticada, DevTools, screenshot ni pruebas por resolución**.

### Diagnóstico exigido en GitBook (P0)

1. En espacio Docs, comprobar cuenta/repositorio/branch: `danielmelendez-pma/CabinetReport-Docs` / `main`, fecha de último sync y errores.
2. En **Docs site** comprobar que la portada que se publica es el contenido de ese espacio, sin apuntar a otra variante/revisión antigua.
3. Comprobar que la última actualización fue **publicada**, no solo guardada en editor.
4. Navegador privado real: verificar presencia simultánea de `Tu primera producción, paso a paso`, `Ir al curso` y el menú de cinco enlaces.
5. Si versión real es correcta pero el extractor sigue viejo, revisar comportamiento de extracción/caché antes de editar Markdown.
6. Conservar evidencia de pantallas y horas; si `Sync` falla, registrar error y corregir integración/permiso/branch sin sobrescribir archivos manualmente.

## 3. Capacidades nativas documentadas y limitación concreta

GitBook documenta formalmente:
- configuración **site-wide/space-specific**, colores, logo, tipografías, temas claros/oscuros;
- personalización de encabezado `header.links`, destino del logo `header.primaryLink`, icono de sitio `favicon`;
- personalización mediante API `GET/PUT /v1/orgs/{organizationId}/sites/{siteId}/customization` que requiere **Bearer token**, `organizationId` y `siteId` autorizados.

**Sin acceso administrativo GitBook ni token autorizado, estos ajustes no se pueden aplicar desde un commit de `CabinetReport-Docs`.** Tampoco se conoce el repositorio/administración del sitio Curso. Por ello **NO se implementaron globalmente el modo oscuro, la barra de cinco enlaces ni el redireccionamiento del logotipo en el GitBook publicado**. La guía actualizada distingue expresamente lo preparado de lo configurado y publicado, con instrucciones exactas para ambos sitios.

No se intentó incrustar `<style>`, scripts, iframes de navegación ni CSS del portal dentro de Markdown. `gitbook-docs.yaml` no se alteró con claves de tema no comprobadas.

## 4. Especificación de identidad y controles de contraste

- Paleta completa: `#111216` (body), `#151519` (header real del portal), `#242424` (panel), `#3C3C3C` (borde), `#F08080` (coral), `#FFE4E1` (rosa), `#FFFFFF`, `#000000`.
- Referencias oficiales: `logo-ovalado.png` en encabezado y `logo-redondo.png` en portada/favicon.
- Cálculo estático de contraste sRGB tipo WCAG: `#F08080` frente a `#151519` ≈ **7,03:1**; `#F08080` frente a `#242424` ≈ **5,99:1**; blanco frente a `#242424` ≈ **15,52:1**. **No constituye una inspección de la apariencia final de GitBook**.
- La cabecera objetivo incluye, en orden, `Inicio`, `Documentación`, `Partners`, `Cursos`, `Manual`; `Inicio` y, si es configurable, el logo llevan a GitHub Pages.
- La navegación textual de las 52 páginas permanece como respaldo hasta probar una barra nativa realmente publicada en **ambos sitios y móvil**.

## 5. Trabajo realizado en el PR de esta etapa

1. Actualización completa de `.github/gitbook-theme-cabinet-report.md`: separación del fondo principal y header real, paleta y logos del portal, los cinco enlaces exactos, procedimientos administrativos diferenciados **Docs/Curso**, diagnóstico ordenado de publicación, matriz responsive y criterios de evidencia.
2. Creación de este informe `.github/documentation-audit-etapa-11-2026-11-08.md`.
3. **No se modificaron** las 52 páginas públicas, `SUMMARY.md`, `gitbook-docs.yaml`, imágenes, precios, condiciones legales, repositorio de aplicación, portal oficial ni el sitio independiente del curso.
4. No se realizan cambios de `Customize` por falta de acceso administrativo autorizado y no se efectúa ningún merge.

## 6. Pruebas y pendientes de aceptación

| Prueba | Estado | Motivo / siguiente evidencia |
| --- | --- | --- |
| HEAD / PR #16 | **Verificado** | GitHub API reporta merge y SHA idéntico |
| 52 rutas en SUMMARY | **Verificado estáticamente** | 52 referencias únicas; PR #16 muestra navegación común por diff |
| Datos de tema / header del portal | **Verificado en código fuente** | CSS/HTML originales de `cabinet-report-partners/main` |
| Desfase README vs publicación Docs | **Detectado** | Lectura textual pública; origen aún sin diagnosticar |
| Git Sync y versión publicada | **Pendiente** | Requiere sesión de administración de GitBook |
| Tema oscuro global Docs | **Pendiente** | Requiere Customize |
| Tema oscuro global Curso | **Pendiente** | Requiere Customize del otro sitio |
| Header nativo + logo con retorno Docs/Curso | **Pendiente** | Requiere Customize + verificación pública |
| Responsive 1440, 1366×768, 768, 390, 430 px | **No ejecutado** | No hay navegador visual conectado; no confundir lectura Markdown con test UI |
| Tabla comparativa y ficha 7 planes | **Revisión estática parcial** | Sus precios se conservaron; verificación de scroll/contraste y modales pendiente |
| `banner.bmp` y 3 grupos duplicados | **Sin cambios** | Necesitan cotejo visual previo para optimizar sin romper referencias |

**P0 (bloqueante para declarar etapa visual completada):** diagnosticar publicación y Git Sync en el panel, activar el tema oscuro y header en los dos sitios, probar en navegador real el retorno a Inicio.

**P1:** comparar logo, navbar, tablas, avisos, sidebar y primeras pantallas en 1440, 1366×768, 768, 390, 430. Documentar capturas/resultado de los cinco enlaces y clic del logo.

**P2:** decidir si retirar navegación textual duplicada **después** de pruebas positivas de header nativo; evaluar `banner.bmp` y las capturas de Windows mediante imágenes auténticas.

## 7. Fuentes oficiales y trazabilidad

- [Personalizar el tema de GitBook](https://gitbook.com/docs/guides/customizing-your-site/how-to-customize-your-sites-theme).
- [API de personalización de sitios GitBook](https://gitbook.com/docs/developers/gitbook-api/api-reference/docs-sites/site-customization).
- [GitBook, opciones de branding](https://gitbook.com/docs/guides/docs-best-practices/how-to-create-branded-documentation).
- [Página pública de Docs contrastada](https://cabinet-report.gitbook.io/cabinet-report-docs/).
- [Portal GitHub Pages de referencia](https://danielmelendez-pma.github.io/cabinet-report-partners/).
- [PR #16](https://github.com/danielmelendez-pma/CabinetReport-Docs/pull/16).

**Cierre honesto:** este PR entrega un diagnóstico y una especificación ejecutable por el administrador, **no una modificación visual ya publicada**. La personalización global queda pendiente de acceso a Customize y validación en navegador. No hacer merge automático.
