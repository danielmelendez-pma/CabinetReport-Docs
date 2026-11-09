# Validación post-merge GitBook — Etapa 9

**Fecha:** 2026-11-08  
**Base:** `main` en `2f89db744709c2828d3e9f8945a81f378982d1a3` (PR #14 fusionado).  
**Rama:** `docs/etapa-09-validacion-navegacion-accesibilidad`

## Verificaciones iniciales
- `gitbook-docs.yaml`: espacio `Documentation`, raíz `./`, idioma `es-419`. Configuración preservada.
- `SUMMARY.md`: 52 páginas públicas. Se revisaron sus referencias y las del propio índice (53 archivos Markdown).
- **406 referencias locales inspeccionadas:** cero destinos de archivos inexistentes detectados con el análisis estático de Markdown, HTML y atributos `cover`.
- `cabinet-report-partners/main`: la ficha interactiva acepta `?plan=optimizador`, `basico`, `intermedio`, `profesional`, `empresarial` y `socio`; el Plan Gratis se expone sin `?plan=gratis`. Validación estática de `suscripciones.html`, no ejecución en navegador.

## Correcciones documentales
1. La portada enlaza las cuatro etapas para realizar la primera producción.
2. El manual orienta la elección posterior entre optimización, reporte de compras, costos, orden de producción y seguimiento de auditoría.
3. El índice de funcionalidades ofrece accesos rápidos según el punto del recorrido.
4. La tabla comparativa enlaza **todos** los planes por nombre, elimina un encabezado redundante y explica cómo consultar las columnas en móvil.
5. Las siete fichas incluyen retorno visible al portal, comparativa y catálogo interactivo; las seis pagadas emplean sus claves existentes `?plan=`.
6. Las ilustraciones de los planes cuentan con `alt` descriptivo, sin pies de imagen vacíos, y el subtítulo de precio pasa de H3 a H2 para no saltar jerarquía.

## Hallazgos gráficos sin intervención destructiva
- `.gitbook/assets/banner.bmp`: **7.322.926 bytes**. Se recomienda evaluar compresión y formato web tras cotejar el diseño en GitBook.
- Grupos de archivos con SHA idéntico: `image (1) (1).png` / `image (10).png` / `image (3).png` / `image (9).png`; `image (10) (1) (1).png` / `image (11) (1) (1).png`; `image (11).png` / `image (12).png`.
- Sin eliminaciones: diferentes páginas pueden referenciar nombres distintos al mismo contenido. Se requieren capturas Windows reales para decidir si alguna imagen quedó obsoleta.

## Publicación: observaciones y límites explícitos
- Se pudo consultar mediante extracción textual la portada pública; aparecían la presentación y el logotipo circular, pero no el enlace «Ir al curso» presente en `README.md` de GitHub. **Posible desfase de caché/publicación, no fallo probado de Git Sync**.
- La consulta automatizada de manual, curso, índice y portal/modal no ofreció acceso estable. No se verificaron los diálogos ni el render completo en escritorio, laptop o móvil.
- Se debe comprobar en navegador real la visualización, tamaño de portadas, contraste de tablas, retorno al portal, curso, modal de cada plan y la sincronización en estado `Synced`.
- El tema oscuro, fondo `#111216` y acento `#F08080` siguen sujetos a configuración de GitBook (véase `.github/gitbook-theme-cabinet-report.md`).
- Permanecen pendientes la URL oficial de Instagram, cotejo de fechas históricas y ejecución de pruebas Windows del flujo de Auditoría RP.

## Integridad y alcance
- Sin alteraciones en tarifas, prestaciones, promociones, cláusulas legales, imágenes, nombres de archivos, `SUMMARY.md`, `gitbook-docs.yaml` ni código de la aplicación o portal.
- Validar cambios en un solo PR de Etapa 9. **No hacer merge automático**.
