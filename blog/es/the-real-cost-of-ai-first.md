---
title: "El coste real de ser IA-first"
date: 2026-09-08
slug: "the-real-cost-of-ai-first"
tags: ["ia-first", "costes", "estrategia", "operaciones"]
status: "published"
excerpt: "La inferencia es la partida más barata. La factura de ser IA-first es sobre todo evaluación, revisión, mantenimiento y cumplimiento, y la mayoría de los presupuestos no la ve venir. Esta es la aritmética que decide si una función de IA merece construirse."
---

La primera función de IA que lanza una empresa suele ser barata. Una clave de API, un prototipo, una demo que cae bien en una reunión de dirección. El dinero se va en el segundo año, y rara vez es el dinero que alguien había previsto.

## La factura no es la de la inferencia

Las llamadas a los modelos son el coste más visible y, cada vez más, el menos importante. Los precios de un nivel de capacidad dado han caído aproximadamente un orden de magnitud al año durante los últimos tres años, y la presión competitiva sigue empujándolos a la baja. Mientras tanto, los costes que rodean a la llamada al modelo están estables o suben:

- **Evaluación e infraestructura de datos.** Registrar cada interacción con etiquetas de resultado, mantener conjuntos de referencia y construir controles de regresión. Sin esto no puedes distinguir una mejora del ruido, y lo pagarás en forma de regresiones que llegan a producción.
- **Revisión humana y escalado.** Allí donde una respuesta incorrecta es cara, una persona tiene que comprobar la salida. Ese trabajo no es gratis y no se reduce porque el modelo haya mejorado: se desplaza.
- **Mantenimiento ante el recambio de modelos.** Los proveedores retiran versiones, cambian los valores por defecto y dejan obsoletos parámetros. Cada uno de esos eventos obliga a repetir pruebas, ajustar prompts y, a veces, a recualificar la función completa.
- **Cumplimiento y revisión de seguridad.** Residencia de los datos, retención, listas de subencargados, acuerdos de tratamiento de datos y, ahora, preguntas específicas sobre IA por parte de clientes y tiendas de aplicaciones. Este trabajo es puntual por función, pero se repite por proveedor y por jurisdicción.
- **Soporte para software probabilístico.** Los usuarios reportan cosas difíciles de reproducir porque la respuesta cambia cada vez. Las herramientas y los manuales de soporte tienen que reescribirse para esa realidad.
- **Coste del fallo.** Un precio alucinado, un resumen incorrecto en la revisión de un contrato, una salida ofensiva mostrada a un cliente. Puede que nunca veas esto en un modelo de costes, pero es la razón por la que varias funciones de IA se retiraron discretamente.

Ninguna de estas partidas aparece en una comparación de «coste por millón de tokens», que es exactamente por lo que es tan fácil pasarlas por alto.

## Qué dice la evidencia sobre el retorno

El reparto del retorno no es homogéneo. En el mismo mercado conviven dos tipos de evidencia.

Por un lado, la medición controlada muestra ganancias reales en trabajo acotado y de alto volumen: un experimento aleatorizado de GitHub de 2023 encontró que los desarrolladores terminaban una tarea un 55.8% más rápido con un asistente de IA (arXiv:2302.06590), y un estudio sobre herramientas de atención al cliente encontró que los casos resueltos por hora subían alrededor de un 14% de media, con cerca de un 34% entre los trabajadores con menos experiencia (Brynjolfsson, Li y Raymond, NBER working paper 31161).

Por otro, los resultados a nivel de cartera son pobres. Un estudio del MIT de 2025 sobre pilotos de IA generativa en empresas reportó que la gran mayoría no produjo ningún impacto medible en la cuenta de resultados, y una encuesta de S&P Global de 2024 encontró que una gran parte de las empresas había abandonado la mayoría de sus iniciativas de IA. Ambos hallazgos deben leerse como aproximaciones a una realidad desordenada, no como mediciones precisas, pero apuntan en la misma dirección.

La reconciliación no es complicada. Las ganancias aparecen donde un flujo de trabajo tiene una métrica medible, volumen suficiente para importar y una salida que una persona puede comprobar rápido. Las pérdidas se concentran donde la métrica nunca se definió, el volumen era bajo o la función se construyó porque era posible y no porque alguien respondiera por el resultado.

## La aritmética que lo decide

Antes de construir, escribe tres números:

1. **Coste por tarea** con el modelo, incluidos reintentos, trabajo de revisión y mantenimiento amortizado.
2. **Coste por tarea hoy**, con todo incluido: salario, herramientas, corrección de errores.
3. **Coste de equivocarse**, y si un paso de revisión humana lo acota.

Una función de IA es defendible cuando el primer número está claramente por debajo del segundo una vez incluidos los costes de revisión, el tercero está acotado por un proceso que de verdad operas y el volumen es lo bastante alto para que la diferencia se acumule. Si el tercer número no tiene límite —una decisión que puede lesionar a alguien, incumplir una norma o destruir una relación—, entonces el paso de revisión no es opcional y hay que ponerle precio desde el principio.

De ahí se siguen dos consecuencias. Primera: algunos de los mejores proyectos de IA son pequeños, porque sustituyen una tarea acotada, repetitiva y de alto volumen. Segunda: hay funciones que deberían rechazarse. Eso no es una postura anti-IA; es lo que hace un presupuesto.

## Donde la IA es sencillamente la herramienta equivocada

- **Lógica determinista.** Cálculo de impuestos, reglas de elegibilidad, aritmética de inventario. Las reglas son más baratas, más rápidas, auditables y estables. Añadir un modelo las empeora; no las moderniza.
- **Volumen bajo.** Si una tarea se ejecuta cincuenta veces al mes, el coste fijo de un conjunto de evaluación, un proceso de revisión y un responsable de mantenimiento nunca se recuperará.
- **Entradas malas.** Si los datos de base están incompletos o el proceso no está definido, un modelo producirá disparates con mucha seguridad y a escala. Arregla primero los datos; el modelo no tiene con qué trabajar.
- **Coste del error sin límite y sin revisión.** Cuando una persona tiene que aprobar cada salida de todos modos, pregúntate con honestidad si el modelo ahorró algo o solo movió el trabajo de sitio.

## Presupuestarlo con honestidad

Tres hábitos separan a los equipos que obtienen valor de los equipos que reciben facturas.

**Fija un techo antes de construir.** Un coste máximo por tarea resuelta y una hipótesis de volumen. Si la función no puede batir ese techo con ese volumen, no se lanza, por buena que fuera la demo.

**Mide el coste por resultado correcto, no por llamada.** Un modelo barato que falla un tercio de las veces es caro. Un modelo capaz usado solo para el 20% de casos difíciles, con un modelo pequeño encargándose del resto, suele ser la arquitectura más barata disponible.

**Escribe por adelantado el criterio de cancelación.** «Si la calidad no llega a X en nuestro conjunto de evaluación para la fecha Y, paramos.» Casi todas las iniciativas de IA que acaban siendo un centro de costes permanente empezaron como un piloto que nadie tenía autoridad para terminar.

Los precios seguirán bajando, y eso ayuda, pero una inferencia más barata no reduce el trabajo de revisión, el mantenimiento ni el coste de una respuesta incorrecta. IA-first no es decidir usar IA en todas partes. Es la disciplina de encontrar los sitios donde los números salen de verdad y tener el valor de decirlo cuando no salen.

*Relacionado: [IA-first es una disciplina, no un eslogan](/blog/es/ai-first-is-a-discipline).*
