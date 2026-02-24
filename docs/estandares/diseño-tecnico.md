# EQ-03 — Diseño técnico justificable

---

## 1. Nombre del estándar
**ID:** EQ-03  
**Nombre:** Diseño técnico justificable

---

## 2. Propósito

Garantizar que las decisiones técnicas relevantes estén fundamentadas, documentadas y alineadas con el contexto del problema.  
Este estándar existe para evitar soluciones arbitrarias, sobre–ingeniería y elecciones basadas únicamente en preferencias personales.

Las decisiones técnicas deben poder explicarse y sostenerse en el tiempo.

---

## 3. Alcance

Este estándar aplica a:

- decisiones de arquitectura,
- selección de tecnologías,
- patrones estructurales relevantes,
- cambios técnicos con impacto significativo.

No aplica a:

- decisiones triviales de implementación local,
- convenciones de bajo impacto previamente definidas.

---

## 4. Definición del estándar

Toda decisión técnica relevante debe:

- responder a un problema o necesidad concreta,
- considerar al menos una alternativa,
- exponer de forma explícita los trade-offs asumidos.

No se considera aceptable:

- decisiones tomadas solo por preferencia personal,
- introducir complejidad sin justificación,
- adoptar tecnologías sin evaluar impacto futuro.

---

## 5. Criterios de aceptación

- [ ] La decisión técnica responde a un problema definido (EQ-01)  
- [ ] Existe una justificación clara y documentada  
- [ ] Se consideraron alternativas razonables  
- [ ] Los trade-offs están explícitamente descritos  
- [ ] La decisión es coherente con la arquitectura existente  
- [ ] El impacto a futuro fue considerado  

---

## 6. Evidencias esperadas

Al menos una de las siguientes:

- documento de decisión técnica (ADR),
- nota de arquitectura,
- discusión técnica registrada,
- documentación de diseño.

La evidencia debe permitir entender el **por qué**, no solo el **qué**.

---

## 7. Antipatrones comunes

- “Siempre lo hacemos así”
- Uso de tecnologías de moda sin análisis
- Decisiones no documentadas
- Complejidad preventiva innecesaria
- Arquitecturas copiadas sin contexto

---

## 8. Nivel de criticidad

**Alto**

El incumplimiento requiere corrección o documentación explícita de la deuda técnica.

---

## 9. Relación con otras prácticas y estándares

**Prácticas relacionadas:**
- Práctica 2 — Diseño orientado a evolución, no a moda  
- Práctica 3 — Arquitectura clara y documentada  
- Práctica 13 — Software alineado al negocio  

**Estándares relacionados:**
- EQ-01 — Claridad del problema y del alcance  
- EQ-04 — Arquitectura coherente y consistente  

---

## 10. Observaciones

Este estándar no busca justificar cada línea de código, sino proteger las decisiones que definen el sistema.  
Documentar decisiones reduce fricción futura y facilita la evolución del software.

Una decisión no documentada es una deuda silenciosa.