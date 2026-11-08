# Etapa 6 — Portada comercial de suscripciones

**Fecha:** 2026-11-08

## Objetivo

Crear una experiencia de consulta de suscripciones visualmente comparable a Cabinet Report Partners, sin comprometer la documentación oficial de GitBook ni inventar capacidades de JavaScript que Git Sync no proporciona.

## Implementación

- `planes-de-suscripcion/README.md`: portada renovada con seis planes en pares de columnas nativas, importes mensuales, enlaces a las fichas oficiales, enlace al Plan Gratis y tabla comparativa, logotipo circular y regreso a inicio.
- Repositorio hermano `danielmelendez-pma/cabinet-report-partners`: página independiente `suscripciones.html` con cuadrícula responsive, seis botones, modal oscuro accesible y enlaces directos `?plan=...`.
- La vista interactiva consulta `CabinetReport-Docs/main/planes-de-suscripcion/plan-*.md` por GitHub Raw, muestra estados de verificación y evita exhibir importes desactualizados como si estuvieran comprobados.
- El código interpreta encabezados mensuales explícitos, sin confundir descuentos anuales con tarifa mensual.
- No se cambia el contenido de los planes, promociones, políticas, licencias ni condiciones comerciales.

## Limitación técnica

GitBook Git Sync no ofrece ejecución arbitraria de JavaScript a través del Markdown. Las columnas y enlaces funcionan de forma nativa; el modal está alojado en GitHub Pages, con enlace desde GitBook.

## Validación pendiente

- Merge de ambos PR, sin merges automáticos.
- Publicación de GitHub Pages de `suscripciones.html` y sincronización GitBook.
- Comprobación visual y de interacción en escritorio y móvil.
- Verificación de tarifas contra cada ficha de origen, en especial Profesional ($150/mes), ausente en la tabla comparativa antigua.
- Comprobar enlaces, diálogo, teclado, navegación directa y bloqueo de precios no verificados.
- Actualizar la tabla comparativa, si el usuario lo aprueba, para incorporar el Plan Profesional con datos acreditados.
