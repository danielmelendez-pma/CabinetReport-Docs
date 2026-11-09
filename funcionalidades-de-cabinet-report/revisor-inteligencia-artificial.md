---
description: >-
  Revisor IA de Cabinet Report: ejecución automática y manual, niveles de
  hallazgos, decisiones, historial, límites técnicos y disponibilidad.
layout:
  width: wide
---

# Revisor de Inteligencia Artificial

**CABINET REPORT · ASISTENCIA PARA REVISIÓN TÉCNICA**

## Cabinet Report calcula. La IA interpreta. El usuario decide.

El **Revisor IA** es un apoyo a la comprobación del [Reporte de Producción](reporte-de-produccion.md). Analiza un contexto que puede incluir piezas, cantidades, módulos, dimensiones, materiales, fórmulas y parámetros técnicos, y propone hallazgos que el usuario debe examinar.

No cambia por sí solo las piezas del reporte ni sustituye las validaciones programadas de Cabinet Report. **La decisión de corregir, resolver o pasar por alto corresponde al usuario.**

{% hint style="warning" %}
**La IA no detecta todos los errores humanos o constructivos.** Una respuesta sin hallazgos no certifica que el despiece esté libre de problemas. Comprueba siempre el diseño, la fabricación y la instalación con criterio técnico.
{% endhint %}

## Ruta breve para revisar con criterio

1. **Prepara el reporte:** confirma piezas, cantidades y parámetros en el [Reporte de Producción](reporte-de-produccion.md).
2. **Ejecuta la revisión:** interpreta los hallazgos y contrástalos con el diseño y las medidas reales.
3. **Decide:** corrige lo que corresponda o registra una decisión consciente.
4. **Comprueba el registro:** consulta [Auditoría RP y persistencia](auditoria-rp-persistencia.md) y verifica que no aparezcan avisos de guardado.

## 1. Cuándo utilizarlo

Utilízalo cuando hayas preparado las piezas del proyecto y quieras una **segunda revisión** de posibles contradicciones o riesgos. Los resultados dependen de la calidad del contexto y de la disponibilidad de un proveedor autorizado.

El Revisor IA puede investigar, entre otros aspectos:

| Área | Ejemplos de preguntas técnicas |
| --- | --- |
| **Dimensiones** | ¿Son compatibles los costados homólogos y las dimensiones exteriores del módulo? |
| **Cantidades** | ¿Coinciden las unidades indicadas con los conjuntos reales? |
| **Material y espesor** | ¿Se ha definido una especificación incompatible con la pieza? |
| **Veta y cantos** | ¿La orientación y los bordes declarados son coherentes con el uso? |
| **Fórmulas** | ¿La fórmula realmente pertenece a la pieza y utiliza los parámetros efectivos del cliente? |
| **Contexto constructivo** | ¿Tipo de módulo, apertura, giro, sobre y estilo justifican las medidas? |

Una coincidencia de nombre, una pieza repetida o una diferencia dimensional **no son por sí solas un error demostrado**: el análisis necesita evidencia de la relación constructiva y de la procedencia de los datos.

## 2. Modalidades de revisión

{% columns %}
{% column width="50%" %}
### Revisión automática

El sistema selecciona entre perfiles de IA habilitados y con credenciales válidas, teniendo en cuenta las restricciones de capacidad. Si un proveedor falla en condiciones admitidas, la ejecución puede utilizar una ruta alternativa.

{% endcolumn %}
{% column width="50%" %}
### Revisión manual

Si utilizas una revisión manual, sigue las indicaciones de la aplicación para preparar la solicitud y aportar una respuesta en el formato que admite el Revisor IA. Un texto libre sin la estructura solicitada puede ser rechazado.

{% endcolumn %}
{% endcolumns %}

El Centro IA puede utilizar **Gemini, Groq, Mistral u OpenAI**, dependiendo de la configuración, las credenciales, los permisos y la disponibilidad del servicio. No todas las opciones tienen que aparecer habilitadas en tu instalación.

En la revisión automática, el sistema prioriza **Gemini → Groq → Mistral → OpenAI** entre las opciones elegibles. Si un proveedor no está disponible, comprueba los mensajes del Centro IA y cuál figura finalmente en el resultado.

## 3. Estados de la revisión

| Estado | Significado |
| --- | --- |
| **No iniciada** | Aún no se ha ejecutado una revisión. |
| **En curso** | Existe un análisis en procesamiento. |
| **Completada** | Terminó el procesamiento técnico. Puede contener hallazgos o **cero hallazgos**. |
| **Fallida** | La ejecución no pudo completarse correctamente. |
| **Cancelada** | La ejecución fue cancelada. |

{% hint style="info" %}
**Importante:** «Completada» identifica el estado de ejecución, **no es prueba suficiente de que el resultado se guardó correctamente en el XML de auditoría**. El sistema utiliza verificaciones adicionales para reconocer su persistencia.
{% endhint %}

## 4. Interpretar la gravedad de un hallazgo

| Clasificación | Cómo interpretarla |
| --- | --- |
| **Error grave** | Una incompatibilidad técnica demostrada que puede impedir ensamblar o utilizar el conjunto según lo definido. |
| **Error moderado** | Una corrección técnica sustentada que no demuestra el mismo nivel de bloqueo estructural. |
| **Advertencia** | Riesgo o discrepancia que requiere confirmar datos, diseño o excepciones constructivas. |
| **Recomendación** | Mejora operativa o de claridad sin error constructivo demostrado. |

La severidad técnica **no equivale automáticamente a la pérdida económica**. Una pieza puede estar equivocada antes del corte y todavía no haber generado desperdicio.

### Ejemplo: costados de distinta altura

Si dos costados del mismo módulo presentan largos distintos, el análisis debería identificar ambos componentes y contrastarlos con la ficha técnica. La diferencia puede ser intencional o revelar una incompatibilidad. Para declarar un **error grave** debe existir una contradicción constructiva acreditada, no solamente una diferencia numérica.

### Ejemplo: piezas repetidas tras una fusión

La repetición puede corresponder a varios módulos iguales. Antes de recomendar unir filas, se deben comprobar función, material, espesor, veta, cantos y cantidades. La sugerencia no autoriza cambios automáticos.

## 5. Qué hacer con un hallazgo

1. Abre la revisión y selecciona el hallazgo.
2. Lee su **explicación, evidencia, valores y recomendación**, cuando estén disponibles.
3. Localiza el módulo o pieza indicada y contrasta el diseño original.
4. Si corregiste el problema y procede registrarlo, utiliza **Resuelto**.
5. Si conscientemente decides no aplicar la recomendación, utiliza **Pasar por alto**.
6. Comprueba que la decisión haya sido **guardada** antes de continuar.

| Decisión | Efecto conceptual |
| --- | --- |
| **Sin decisión** | El usuario todavía no ha cerrado el asunto. |
| **Resuelto** | El usuario declara que atendió el hallazgo; la corrección física y su resultado se deben comprobar aparte. |
| **Pasar por alto** | El usuario decide continuar sin aplicar esa corrección; no acredita un ahorro ni transforma el riesgo en inexistente. |

Al resolver, la aplicación puede solicitar una **confirmación económica independiente** sobre si se evitó un costo de reposición. No responder afirmativamente sin evidencia.

{% hint style="warning" %}
**Si aparece un error al acreditar la decisión:** no supongas que quedó guardada. Vuelve a revisar el estado y la [Auditoría RP](auditoria-rp-persistencia.md). Los controles de persistencia pueden rechazar operaciones cuando cambió la producción o no coincide la identidad de la revisión.
{% endhint %}

## 6. Nuevas revisiones e historial

El producto incluye estructuras para recuperar la última revisión completada, consultar **historial** y correlacionar hallazgos entre análisis. También existen rutas para realizar una nueva revisión o revisar con otro proveedor cuando se autoriza.

Estas acciones pueden estar sujetas a:

- Estado y acreditación de la revisión anterior.
- Identidad del cliente, usuario y Reporte de Producción.
- Huella de la producción y conservación del contexto.
- Disponibilidad de proveedores, límites de capacidad y controles sobre revisiones automáticas.
- Recuperación o conciliación de información pendiente de persistencia.

**No se debe interpretar un cambio de estado o una comparación histórica como prueba de que una pieza fue corregida físicamente.**

## 7. Revisión de parámetros y fórmulas

La IA recibe contexto técnico, pero **no debe inventar una fórmula** porque coincidan los nombres de una pieza o un módulo. Las luces de puertas, dimensiones efectivas, sobre, tipo constructivo, apertura, giro y estilo personalizado pueden modificar lo esperado.

Cuando la evidencia sea insuficiente, el resultado debe expresar la incertidumbre o abstenerse de asignar una medida exacta. Las revisiones pueden continuar analizando otros componentes aun si falta parte del contexto.

## 8. Precios y economía: una capa diferente

El Revisor IA dispone de servicios para referencias de precios de tableros y cantos, valoraciones y seguimiento de impactos. El sistema contempla información del cliente, referencias comerciales y búsquedas asistidas cuando corresponda.

- Un **precio de referencia** no equivale necesariamente a una cotización vigente o comprobada.
- Una coincidencia de material requiere validar marca, formato, espesor y unidad comercial.
- Un hallazgo técnico puede ser válido aun cuando **no exista precio** disponible.
- La economía de una posible reposición es una **estimación condicionada**, no una factura ni una pérdida confirmada.
- Decidir «Pasar por alto» **no acredita ahorro económico**.

Consulta [Auditoría RP y persistencia](auditoria-rp-persistencia.md) para comprender dónde se registran decisiones y datos económicos.

## 9. Lista de comprobación final

Antes de liberar la producción, confirma que revisaste la evidencia de los hallazgos relevantes, verificaste los cambios en las piezas reales, atendiste las advertencias necesarias y comprobaste el guardado de tus decisiones. La conclusión de la IA es una ayuda; **la responsabilidad de validar la producción sigue siendo humana**.

## Navegación relacionada

[Reporte de Producción](reporte-de-produccion.md) · [Auditoría RP y persistencia](auditoria-rp-persistencia.md) · [Creador de módulos](creador-de-modulos.md) · [Índice de funcionalidades](README.md)

---

[**🏠 Volver al portal principal de Cabinet Report**](https://danielmelendez-pma.github.io/cabinet-report-partners/)
