---
description: >-
  Auditoría RP de Cabinet Report: seguimiento de revisiones, guardado de
  decisiones, recuperación de información y referencias económicas.
layout:
  width: wide
---

# Auditoría RP y persistencia

**[🏠 Inicio](https://danielmelendez-pma.github.io/cabinet-report-partners/)** · [Documentación](https://cabinet-report.gitbook.io/cabinet-report-docs/) · [Partners](https://danielmelendez-pma.github.io/cabinet-report-partners/partners.html) · [Cursos](https://cabinet-report.gitbook.io/curso-de-cabinet-report/) · [Manual](https://cabinet-report.gitbook.io/cabinet-report-docs/manual-de-usuario)

**CABINET REPORT · SEGUIMIENTO DE PRODUCCIÓN**

## ¿Para qué sirve la Auditoría RP?

La **Auditoría RP** ayuda a conservar el historial de una producción: qué información se revisó, qué observaciones surgieron y qué decisiones tomaste antes de continuar. Complementa el [Reporte de Producción](reporte-de-produccion.md) y el [Revisor de Inteligencia Artificial](revisor-inteligencia-artificial.md).

No certifica que las piezas ya se hayan fabricado ni sustituye la inspección del responsable técnico.

## 1. Qué información acompaña al proyecto

| Archivo o información | ¿Para qué se utiliza? |
| --- | --- |
| **Reporte de producción (TXT)** | Contiene las piezas y los datos utilizados para preparar la fabricación. |
| **Metadatos técnicos (XML)** | Conservan información adicional sobre los módulos, cuando corresponde. |
| **Auditoría RP (XML)** | Registra eventos, revisiones y decisiones relacionadas con la producción. |
| **Datos económicos** | Permiten consultar estimaciones y referencias de costos cuando existe información suficiente. |

{% hint style="info" %}
**No son archivos intercambiables.** Trabaja siempre con la producción correcta y evita modificar manualmente sus archivos sin respaldo.
{% endhint %}

## 2. Cómo comprobar que una revisión quedó guardada

1. Abre el proyecto con el **cliente, ambiente y reporte de producción** correctos.
2. Ejecuta o consulta la revisión del [Revisor IA](revisor-inteligencia-artificial.md), si está disponible para tu licencia.
3. Lee los hallazgos y verifica las medidas, materiales y piezas afectadas.
4. Registra las decisiones que corresponda tomar: **Resuelto** o **Pasar por alto**.
5. Comprueba que no aparezcan advertencias de guardado o acreditación.
6. Cuando necesites retomar el trabajo, **vuelve a abrir la misma producción** y confirma que las revisiones y decisiones esperadas siguen visibles.

Una revisión puede mostrar **Completada**, incluso con **cero hallazgos**, sin que ese estado por sí solo garantice que todos sus datos se hayan guardado correctamente.

## 3. Comprender las decisiones

| Acción | Qué significa | Qué no significa |
| --- | --- | --- |
| **Resuelto** | Indicas que atendiste el hallazgo. | No prueba que la pieza física esté corregida. |
| **Pasar por alto** | Decides continuar sin efectuar esa corrección. | No elimina el riesgo ni confirma un ahorro. |
| **Nueva revisión** | Solicitas otra evaluación del estado de la producción. | No implica que una observación anterior se haya corregido. |
| **Continuar con pendientes** | Autorizas continuar cuando el sistema solicita una confirmación. | No garantiza que el documento final o la fabricación estén correctos. |

{% hint style="warning" %}
**La decisión es tuya.** Si un hallazgo es grave o no comprendes sus consecuencias, verifica la información antes de generar u optimizar la producción.
{% endhint %}

## 4. Recuperar información al abrir nuevamente

Cabinet Report dispone de mecanismos para recuperar y reconocer revisiones previamente registradas, siempre que su identidad corresponda con la producción actual.

Si no encuentras una revisión o el sistema informa un problema de persistencia:

1. Confirma que abriste el **mismo cliente, ambiente y RP**.
2. Comprueba que tienes acceso a la carpeta del proyecto y a los archivos de auditoría.
3. Lee cualquier aviso de guardado, acreditación o recuperación y conserva el mensaje.
4. Evita eliminar, renombrar o combinar archivos XML para intentar corregir el problema.
5. Conserva una copia del proyecto y contacta con soporte si el estado sigue sin recuperarse.

**No des por guardada una decisión si el sistema informa que no pudo acreditarla.** Comprueba el estado antes de continuar y no sustituyas un archivo anterior sin respaldo.

## 5. Interpretar costos y posibles pérdidas

Cuando hay datos suficientes, la auditoría puede acompañarse de estimaciones relacionadas con materiales, cantos y reposición. Para valorar una referencia comprueba, entre otros elementos, el **material, marca, espesor, formato comercial, medidas y unidad de precio**.

Una cantidad calculada **no equivale automáticamente** a dinero gastado, material perdido o ahorro confirmado. Si no existen precios utilizables, la revisión técnica puede seguir siendo relevante aunque la estimación económica esté pendiente.

Para preparar una cotización consulta [Costos y cotizaciones](costos-en-desarrollo.md) y para validar un material consulta [Stock de tableros](stock-de-tableros.md).

## 6. Comprobación final antes de fabricar

Antes de distribuir los documentos, revisa que corresponden a la producción actual, que el TXT contiene los cambios esperados y que las decisiones importantes siguen guardadas. Conserva una copia de seguridad y asegúrate de que el equipo de fabricación recibe la versión correcta.

## Navegación relacionada

[Reporte de Producción](reporte-de-produccion.md) · [Revisor IA](revisor-inteligencia-artificial.md) · [Manual de usuario](../manual-de-usuario.md) · [Índice de funcionalidades](README.md)

---

[← Volver al inicio de Cabinet Report](../README.md)
