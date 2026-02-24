# Practica 1 - Diagnóstico antes de construir

## Qué es

Antes de escribir una sola línea de código, realizo un **diagnóstico técnico y funcional** del problema a resolver.  
El objetivo no es diseñar la solución final, sino **entender correctamente el problema**, su contexto y sus restricciones reales.

Construir sin diagnóstico es una forma elegante de desperdiciar presupuesto.

---

## Por qué importa

La mayoría de los problemas de software no fallan por mala implementación, sino por:

- suposiciones incorrectas,
- requisitos mal entendidos,
- decisiones técnicas tomadas demasiado pronto.

Un diagnóstico adecuado:

- reduce retrabajo,
- evita sobre–ingeniería,
- expone riesgos antes de que sean caros,
- alinea expectativas técnicas y de negocio.

En otras palabras: **previene sorpresas en producción**.

---

## Qué analizo en esta etapa

Dependiendo del proyecto, el diagnóstico puede incluir:

### Contexto de negocio
- Qué problema se quiere resolver realmente.
- Qué métricas definen el éxito.
- Qué pasa si no se resuelve ahora.

### Estado actual del sistema
- Arquitectura existente (si la hay).
- Deuda técnica relevante.
- Puntos de fallo conocidos o recurrentes.

### Restricciones reales
- Presupuesto.
- Plazos.
- Tamaño y madurez del equipo.
- Cumplimiento, seguridad o regulaciones.

### Riesgos técnicos
- Dependencias críticas.
- Cuellos de botella potenciales.
- Decisiones irreversibles o de alto impacto.

---

## Cómo lo aplico en la práctica

El diagnóstico se traduce en:

- preguntas incómodas pero necesarias,
- revisión de código o arquitectura cuando aplica,
- propuestas con **trade-offs explícitos**, no soluciones mágicas.

El resultado no suele ser un documento extenso, sino:

- un entendimiento compartido,
- un conjunto de decisiones conscientes,
- un camino técnico defendible.

Si algo no está claro en esta etapa, **no se finge certeza**. Se investiga o se acota.

---

## Qué problemas evita

Aplicar esta práctica reduce significativamente:

- desarrollos que no resuelven el problema correcto,
- soluciones sobredimensionadas,
- decisiones técnicas difíciles de revertir,
- fricción entre negocio y tecnología.

Diagnosticar primero no retrasa el proyecto.  
Lo acelera… evitando errores caros.

---

## Principio clave

> Ninguna arquitectura es buena o mala en abstracto.  
> Solo es correcta o incorrecta **para un contexto específico**.

Por eso, el diagnóstico no es opcional:  
es la base sobre la que se construye todo lo demás.