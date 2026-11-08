# Identidad visual GitBook — fondo de Cabinet Report Partners

**Solicitud:** 2026-11-08  
**Estado:** pendiente de aplicar y comprobar en el panel de administración de GitBook.  
**Repositorio:** `CabinetReport-Docs` (Git Sync activo, raíz `./`).

## Referencia exacta

El CSS publicado en `danielmelendez-pma/cabinet-report-partners/styles.css` declara:

- Fondo general: `--bg: #111216`
- Fondo alternativo: `--bg2: #181920`
- Paneles: `--panel: #1b1d24`
- Texto claro: `--light: #faf6f5`

La paleta base de Cabinet Report se conserva: negro `#000000`, gris `#242424`, gris `#3C3C3C`, LightCoral `#F08080`, MistyRose `#FFE4E1`, blanco `#FFFFFF`. Para armonizar con Partners, el color del fondo del sitio será `#111216`, sin alterar el color oficial de la aplicación.

## Procedimiento manual en GitBook

1. En la administración de GitBook, abrir el **Docs site** público `Cabinet Report`.
2. Entrar en **Customize → General → Themes** (la posición puede variar según la interfaz).
3. Elegir **Dark** como modo por defecto; si se ofrece conmutador claro/oscuro, decidir si se permite al lector cambiarlo.
4. Buscar **Tint / Background tint**, seleccionar **Custom** y probar `#111216` como color.
5. Mantener `#F08080` como color de acento y revisar legibilidad de textos, links, tablas y botones.
6. Verificar que el logotipo circular elegido por el usuario sea legible en el tema oscuro.
7. Previsualizar inicio, suscripciones, tabla comparativa y una página de funcionalidades en escritorio y móvil.
8. Pulsar **Save** para publicar y confirmar el sitio público.

**Límite importante:** el tinte de GitBook no necesariamente equivale a un color CSS de fondo exacto. La capacidad de personalización puede variar por plan; no se debe prometer identidad píxel a píxel. Si el control no aparece, conservar modo oscuro y color de acento, sin intentar inyectar CSS/JS en Markdown.

## Git Sync y responsabilidades

- El archivo `gitbook-docs.yaml` administra estructura y contenido, no el fondo visual.
- Los cambios de **Customize** no son un commit de GitHub y no quedan aplicados por este PR.
- No se deben añadir etiquetas `<style>`, scripts ni temas CSS arbitrarios a los Markdown.
- Comprobar que Git Sync permanece en `Synced` después de la personalización.

**Fuentes de referencia:** documentación oficial GitBook sobre Customization, Themes y Tint; CSS del repositorio Cabinet Report Partners.
