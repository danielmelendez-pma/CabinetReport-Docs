---
description: >-
  Uso inicial del diccionario técnico de Cabinet Report para registrar
  equivalencias entre palabras de origen y denominaciones técnicas.
---

# Diccionario de piezas

[🏠 Volver al portal principal de Cabinet Report](https://danielmelendez-pma.github.io/cabinet-report-partners/)

**CABINET REPORT · NOMENCLATURA TÉCNICA**

## Una terminología consistente para las piezas

La versión anterior de esta página solo decía «Documentación en desarrollo». La revisión del código de Cabinet Report confirma que existe una ventana para **administrar equivalencias entre palabras de origen y traducciones técnicas**. En la aplicación, su título es **Diccionario de Partes**.

Este diccionario está relacionado con la **nomenclatura**. No debe confundirse con el [Creador de piezas](creador-de-piezas.md), que define dimensiones y otros datos constructivos.

<figure><img src="../.gitbook/assets/image (18).png" alt="Captura existente del diccionario de piezas"><figcaption><p>Referencia visual del diccionario de partes.</p></figcaption></figure>

## Funciones identificadas en la implementación

| Función | Uso |
| --- | --- |
| **Consultar** | Visualizar pares de palabra de origen y traducción técnica almacenados. |
| **Agregar** | Incorporar una equivalencia nueva; requiere ambos campos y un origen no duplicado. |
| **Actualizar** | Guardar modificaciones de traducciones en las entradas existentes del listado. |
| **Eliminar** | Quitar del diccionario el término seleccionado. |

{% hint style="info" %}
**Estado verificado:** existe una implementación de estas operaciones. El aviso antiguo «Documentación en desarrollo» indicaba falta de explicación, no demuestra que el módulo esté sin desarrollar. El funcionamiento en la versión Windows del usuario sigue pendiente de prueba específica.
{% endhint %}

## Procedimiento práctico

1. **Abre Diccionario de Partes** si está disponible para tu usuario.
2. **Revisa el listado** de términos y equivalencias antes de introducir otro.
3. **Para agregar:** completa **Palabra origen** y **Traducción técnica** y selecciona **Agregar**.
4. **Para modificar:** edita la traducción de una entrada existente directamente en el listado, pulsa **Actualizar** y comprueba el resultado.
5. **Para eliminar:** selecciona la palabra de origen de la entrada correspondiente y utiliza **Eliminar** solo si estás seguro del cambio.
6. **Acuerda la nomenclatura** con el responsable técnico antes de aplicarla a los procesos de la empresa.

## Ejemplo de aplicación

Si distintos planificadores usan nombres diferentes para referirse a la misma parte de mueble, el equipo técnico puede definir una denominación consistente y registrar su equivalencia. Este proceso **no cambia por sí mismo el tamaño, el material o la fórmula** de una pieza.

{% hint style="warning" %}
**Los cambios afectan registros almacenados.** La implementación revisada no demuestra aislamiento del diccionario por cliente. No modifiques términos compartidos sin autorización ni supongas que la aplicación los aplicará automáticamente en todos los reportes.
{% endhint %}

## Aspectos pendientes de validación funcional

- Ruta exacta de acceso y permisos por perfil.
- Alcance de las entradas entre clientes y usuarios.
- Procesos concretos donde se aplican las traducciones.
- Pruebas de alta, edición y eliminación en Windows.

## Continúa aprendiendo

[Creador de piezas](creador-de-piezas.md) · [Creador de módulos](creador-de-modulos.md) · [Reporte de producción](reporte-de-produccion.md) · [Índice de funcionalidades](README.md)

---

[← Volver al inicio de Cabinet Report](../README.md)
