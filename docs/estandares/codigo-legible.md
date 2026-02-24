# EQ-05 — Código legible y mantenible

---

## 1. Nombre del estándar
**ID:** EQ-05  
**Nombre:** Código legible y mantenible

---

## 2. Propósito

Garantizar que el código producido pueda ser entendido, modificado y mantenido por otros desarrolladores en el tiempo.  
Este estándar existe para reducir dependencia de personas, facilitar la evolución del sistema y minimizar errores introducidos por malentendidos.

El código se lee muchas más veces de las que se escribe.

---

## 3. Alcance

Este estándar aplica a:

- todo código de producción,
- scripts operativos relevantes,
- configuraciones versionadas,
- automatizaciones y pipelines.

No aplica a:

- pruebas exploratorias desechables,
- prototipos explícitamente marcados como temporales.

---

## 4. Definición del estándar

El código debe:

- ser comprensible sin explicación externa,
- seguir convenciones claras y consistentes,
- priorizar claridad sobre complejidad innecesaria.

No se considera aceptable:

- código críptico o excesivamente “inteligente”,
- lógica densa sin separación de responsabilidades,
- estilos inconsistentes dentro del mismo sistema.

---

## 5. Criterios de aceptación

- [ ] El código se entiende al leerlo sin contexto adicional  
- [ ] Los nombres de variables, funciones y componentes son descriptivos  
- [ ] La lógica está organizada en unidades con responsabilidad clara  
- [ ] No existen secciones complejas sin justificación  
- [ ] Se siguen las convenciones definidas del proyecto  
- [ ] El código puede modificarse sin riesgo excesivo  

---

## 6. Evidencias esperadas

Al menos una de las siguientes:

- revisiones de código aprobadas,
- convenciones documentadas,
- estructura de proyecto consistente,
- feedback técnico registrado.

La evidencia debe demostrar que el código puede mantenerse por terceros.

---

## 7. Antipatrones comunes

- Código “clever” difícil de leer
- Funciones o clases con demasiadas responsabilidades
- Nombres genéricos o ambiguos
- Comentarios que explican *qué* hace el código en lugar de *por qué*
- Estilos mezclados sin criterio

---

## 8. Nivel de criticidad

**Alto**

El incumplimiento requiere refactor antes de aceptar la entrega o registro explícito como deuda técnica.

---

## 9. Relación con otras prácticas y estándares

**Prácticas relacionadas:**
- Práctica 8 — Calidad como estándar, no como fase  
- Práctica 10 — Control consciente de deuda técnica  
- Práctica 15 — Transferencia de conocimiento  

**Estándares relacionados:**
- EQ-04 — Arquitectura coherente y consistente  
- EQ-07 — Pruebas con propósito  

---

## 10. Observaciones

La legibilidad no es subjetiva cuando existe un estándar claro.  
El código mantenible reduce errores, acelera cambios y protege al equipo.

El mejor código no impresiona: se entiende.