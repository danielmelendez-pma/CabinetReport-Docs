# Auditoría integral GitBook — Etapa 8

**Fecha:** 2026-11-08  
**Repositorio:** `danielmelendez-pma/CabinetReport-Docs`  
**Rama de trabajo:** `docs/etapa-08-auditoria-integral-usuarios`  
**Base verificada:** `main` en `9907d8c363175093d661b2d1500dc0da9e7e96fd` (PR #13 mergeado después del PR #12).

## Alcance revisado

- Índice `SUMMARY.md`: 52 entradas de páginas Markdown de contenido (sin incluir el índice) y estructura jerárquica conservada.
- **52 páginas públicas** distribuidas entre portada, información del producto, perfiles, funcionalidades, planes, manual, redes sociales, evolución y documentos legales.
- Referencias locales Markdown/HTML de imágenes y archivos, relativas a la ruta de cada página: **cero destinos locales inexistentes detectados** en los archivos revisados.
- Las 52 páginas disponen de un acceso a `https://danielmelendez-pma.github.io/cabinet-report-partners/` incorporado en el PR #13.
- Siete planes revisados: Gratis $0, Optimizador $25, Básico $50, Intermedio $75, Profesional $150, Empresarial $200 y Socio $300 mensuales.
- Portal de suscripciones inspeccionado en `cabinet-report-partners/main` (`e56a8d7e9b5401cd1c040903ca2923d56020ff4a`): seis tarjetas pagadas y consulta del parámetro `?plan=`, acceso independiente al Plan Gratis.
- Comparación selectiva de formularios con `CabinetReport/master` (`7b1f2f8bb4d6583e8e2a82067b9c453e979e16b4`), incluyendo `FrmCostos`, `FrmGeneradorQR`, `FrmAccesorios`, `FrmReporteDeCompras` y `FrmReporteProduccion`. La disponibilidad real depende de versión, licencia y configuración.

## Hallazgos y correcciones

1. **Auditoría RP:** la página contenía detalles de implementación (identificadores, bloqueos, serialización y mecanismos internos) poco útiles para usuarios. Se reestructuró alrededor de guardado, revisión, recuperación, decisiones, archivos y lectura de referencias económicas.
2. **Diccionario de piezas:** quedaron textos de auditoría (`La revisión del código`, `Estado verificado`, `pruebas pendientes`). Se sustituyeron por explicaciones y comprobaciones concretas para el usuario.
3. **Orden de Producción:** se retiraron tablas internas de base de datos y referencias al código. Se conservaron las acciones del flujo, restricciones de asignación y recomendaciones de sincronización.
4. **Catálogo de tableros:** se reemplazaron declaraciones de pruebas internas pendientes por verificaciones de material y permisos útiles al usuario.
5. **Compras, Costos, QR y Herrajes:** se sustituyó lenguaje de código/implementación por instrucciones prácticas, conservando advertencias técnicas.
6. **Revisor IA:** se explicó el formato de respuesta manual y la selección de proveedores desde la perspectiva del usuario, sin prometer disponibilidad universal.
7. **Presentación de funciones:** se retiró la afirmación genérica de que la optimización de tableros y otras herramientas podían estar en desarrollo; las páginas son de funciones implementadas sujetas a licencia y formatos.
8. **Planes:** la tabla comparativa deja de hablar de `prometer comercialmente`; se conservan precios, beneficios, valores, filas y vínculos.
9. **Evolución:** se retiró la referencia pública al repositorio y se mantuvieron las reservas sobre fechas históricas.
10. **Navegación:** enlaces directos al curso desde la portada y el índice de funcionalidades, además de los accesos existentes al portal, manual y planes.

## Integridad y exclusiones

- **Sin cambios de rutas** ni renombres de archivos; Costos, QR y Herrajes conservan los archivos históricos terminados en `-en-desarrollo.md`, sin exponer el sufijo en títulos.
- `SUMMARY.md` y `gitbook-docs.yaml` se conservan sin cambios para evitar alteraciones de navegación/sincronización.
- Sin nuevas imágenes ni eliminación de recursos. Se mantienen las capturas originales y el logo circular.
- Sin cambios en suscripciones, precios, descuentos, beneficios, licencias o textos legales.
- Sin cambios al repositorio de la aplicación ni al portal web.
- Markdown de GitBook: sin CSS/JS inyectado y sin alteraciones a sus directivas nativas.

## Pendientes posteriores al merge

1. Confirmar **Git Sync = Synced** y que la portada pública muestre el logo circular y los textos actualizados.
2. Revisar visualmente portada, funcionalidades, tabla comparativa y manual en escritorio, laptop y móvil; verificar contraste y espaciado.
3. Aplicar, si se desea y el plan de GitBook lo permite, **Customize → Themes / Tint** con modo oscuro, acento `#F08080` y fondo de referencia `#111216`. Esta configuración no es modificable mediante el presente Markdown.
4. Abrir desde navegador el curso, manual, portal y las fichas interactivas `?plan=` para confirmar publicación, diálogo y retorno. La comprobación programática de URL pública no sustituye prueba visual.
5. Comprobar con pruebas reales de Windows recuperación/acreditación de Auditoría RP, permisos del diccionario, tableros privados, archivos de compras y compatibilidad externa. Estas funciones no se han ejecutado desde GitHub.
6. Confirmar el vínculo público oficial de Instagram y contrastar el orden/fechas de algunos hitos de evolución antes de modificarlos.
7. Evitar afirmaciones de exactitud absoluta sobre precios de Internet, resultados de IA o existencias físicas de almacén.

**Flujo:** un único PR para Etapa 8, revisión por el usuario y **sin merge automático**.