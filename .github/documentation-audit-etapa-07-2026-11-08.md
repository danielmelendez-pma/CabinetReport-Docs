# Etapa 7 — Experiencia del usuario, manual y navegación

**Fecha:** 2026-11-08  
**Repositorio:** `danielmelendez-pma/CabinetReport-Docs`  
**Base:** `main` `94ada02e2ff52b17f871d74b86b72d26e23a2095`  
**Solicitud:** todas las páginas públicas deben dirigirse a clientes y usuarios, no a vendedores o administradores de contenidos.

## Hallazgo que inicia la etapa

En `planes-de-suscripcion/README.md` aparecía la sección **«Comparte la página con tus clientes»** con instrucciones de campañas de WhatsApp e Instagram. No corresponde a un lector que evalúa su propia licencia.

## Correcciones

1. Se eliminó por completo la sección y sus instrucciones de campañas. Se conserva el acceso al catálogo interactivo como **opción de consulta del usuario**, sin referencias promocionales a Partners.
2. Se reescribió `manual-de-usuario.md` con ruta de aprendizaje (sesión, proyectos, piezas, reporte), enlace al curso y guía de soporte, preservando la ilustración.
3. Se normalizaron etiquetas de `SUMMARY.md` y se aclararon textos de Instagram y prueba de 30 días para el lector final.
4. Se revisaron las páginas de funcionalidades que hablaban del «repositorio», «código» o pruebas internas: Costos, QR, Herrajes, Optimizadores, Compras, Auditoría RP y el índice. Ahora presentan condiciones de uso y precauciones directamente útiles al usuario.
5. Se agregaron accesos de consulta a manual, funcionalidades y planes en las políticas de soporte y capacitación **sin modificar sus cláusulas originales**.

## Reglas editoriales de aquí en adelante

- **Audiencia:** cliente, usuario actual, posible usuario y personal de taller; segunda persona, instrucciones claras y beneficios verificables.
- **Contenido público:** explicar cómo consultar y utilizar el software, qué revisar y dónde encontrar ayuda. No incluir instrucciones para vender, publicar campañas, editar GitHub o administrar GitBook.
- **Separación:** los informes de auditoría y decisiones de mantenimiento quedan en `.github/`, fuera del índice público.
- **Limitaciones:** conservar advertencias sobre revisión humana, licencia, precios y verificación; evitar promesas absolutas.
- **Navegación:** mantener el enlace de regreso a la portada en todas las páginas de contenido.
- **Estilo:** paleta Cabinet Report; el ajuste del fondo `#111216` sigue dependiendo de la personalización del sitio en GitBook.
- **Legal:** no alterar el sentido de términos, licencia, privacidad, ética, soporte o capacitación sin revisión expresa.

## Validaciones

- Confirmar que no reaparezca el bloque «Comparte la página con tus clientes».
- Confirmar que la portada de planes mantiene las seis tarjetas y el Plan Gratis, la tabla y las condiciones.
- Comprobar rutas relativas de enlaces e imágenes de archivos editados.
- Verificar el curso externo y la vista interactiva de planes en navegador.
- Revisar la publicación Git Sync y las vistas móvil/escritorio tras el merge.
- No realizar merge automático.

## Siguiente etapa

**Etapa 8:** revisión final de consistencia de navegación y contenido público, pruebas visuales en GitBook, correcciones de enlaces y evaluación de pendientes históricos; un PR por etapa.
