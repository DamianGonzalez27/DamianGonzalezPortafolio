# EQ-01 — Claridad del problema y del alcance

---

## 1. Nombre del estándar
**ID:** EQ-01  
**Nombre:** Claridad del problema y del alcance

---

## 2. Propósito

Garantizar que todo trabajo se base en una comprensión clara y compartida del problema a resolver y del alcance del trabajo.  
Este estándar existe para evitar desarrollos basados en suposiciones, interpretaciones ambiguas o expectativas implícitas.

Un problema mal definido genera soluciones incorrectas, sin importar su calidad técnica.

---

## 3. Alcance

Este estándar aplica a:

- nuevos desarrollos,
- mejoras funcionales,
- refactors significativos,
- iniciativas técnicas con impacto en negocio u operación.

No aplica únicamente a:

- tareas puramente operativas sin impacto funcional,
- correcciones triviales claramente acotadas.

---

## 4. Definición del estándar

Antes de iniciar cualquier implementación:

- el problema debe estar descrito de forma explícita,
- el alcance debe estar claramente delimitado,
- las suposiciones deben estar identificadas y documentadas.

No se considera aceptable iniciar trabajo cuando:

- el problema se define solo como una solución deseada,
- el alcance es implícito o cambiante,
- existen dependencias críticas no identificadas.

---

## 5. Criterios de aceptación

- [ ] El problema a resolver está descrito en términos claros y comprensibles  
- [ ] Se distingue el problema del enfoque de solución  
- [ ] El alcance del trabajo está explícitamente delimitado  
- [ ] Los elementos fuera de alcance están identificados  
- [ ] Las suposiciones relevantes están documentadas  
- [ ] Los objetivos de éxito están definidos  

---

## 6. Evidencias esperadas

Al menos una de las siguientes:

- documento de definición del problema,
- ticket o historia con descripción completa,
- nota técnica de diagnóstico,
- acta de acuerdo de alcance.

La evidencia debe ser accesible y compartida con las partes involucradas.

---

## 7. Antipatrones comunes

- “Esto es solo agregar X”
- Requerimientos expresados únicamente como soluciones
- Cambios de alcance no documentados
- “Ya se entiende, luego lo afinamos”
- Inicio de desarrollo sin validación del problema

---

## 8. Nivel de criticidad

**Crítico**

El incumplimiento de este estándar bloquea el inicio del trabajo hasta que se cumpla.

---

## 9. Relación con otras prácticas y estándares

**Prácticas relacionadas:**
- Práctica 1 — Diagnóstico antes de construir  
- Práctica 11 — Comunicación técnica honesta  

**Estándares relacionados:**
- EQ-02 — Criterios de aceptación explícitos  
- EQ-03 — Diseño técnico justificable  

---

## 10. Observaciones

Este estándar no busca ralentizar el trabajo, sino eliminar ambigüedad temprana.  
Invertir tiempo en claridad inicial reduce de forma significativa el retrabajo y los conflictos posteriores.

Cuando el problema está claro, las decisiones técnicas se vuelven mucho más simples.