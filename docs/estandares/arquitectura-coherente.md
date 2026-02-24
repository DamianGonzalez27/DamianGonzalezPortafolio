# EQ-04 — Arquitectura coherente y consistente

---

## 1. Nombre del estándar
**ID:** EQ-04  
**Nombre:** Arquitectura coherente y consistente

---

## 2. Propósito

Garantizar que la arquitectura del sistema mantenga coherencia interna y consistencia a lo largo del tiempo.  
Este estándar existe para evitar la degradación progresiva del diseño debido a decisiones aisladas o inconsistentes.

Una arquitectura incoherente aumenta la complejidad sin aportar valor.

---

## 3. Alcance

Este estándar aplica a:

- sistemas nuevos,
- evolución de sistemas existentes,
- incorporación de nuevos componentes o servicios,
- cambios estructurales relevantes.

No aplica a:

- implementaciones locales sin impacto estructural,
- experimentos explícitamente aislados.

---

## 4. Definición del estándar

La solución debe:

- respetar los límites y responsabilidades definidos,
- mantener consistencia en patrones y estilos arquitectónicos,
- evitar acoplamientos innecesarios entre componentes.

No se considera aceptable:

- mezclar estilos arquitectónicos sin justificación,
- romper límites establecidos por conveniencia,
- introducir dependencias circulares.

---

## 5. Criterios de aceptación

- [ ] Los componentes respetan sus responsabilidades definidas  
- [ ] Los límites entre módulos o servicios son claros  
- [ ] No existen acoplamientos innecesarios o implícitos  
- [ ] Los patrones arquitectónicos se aplican de forma consistente  
- [ ] Los cambios no contradicen decisiones arquitectónicas previas (EQ-03)  
- [ ] La arquitectura puede explicarse de forma clara  

---

## 6. Evidencias esperadas

Al menos una de las siguientes:

- diagramas arquitectónicos actualizados,
- documentación de límites y responsabilidades,
- revisión técnica del impacto arquitectónico,
- validación de arquitectura en revisiones de diseño.

La evidencia debe reflejar el estado actual del sistema.

---

## 7. Antipatrones comunes

- “Solo esta vez cruzamos la capa”
- Lógica de negocio dispersa
- Dependencias circulares
- Múltiples estilos arquitectónicos mezclados
- Componentes con responsabilidades difusas

---

## 8. Nivel de criticidad

**Alto**

El incumplimiento requiere corrección o justificación explícita documentada.

---

## 9. Relación con otras prácticas y estándares

**Prácticas relacionadas:**
- Práctica 3 — Arquitectura clara y documentada  
- Práctica 12 — Responsabilidad de extremo a extremo  
- Práctica 14 — Estandarización sin rigidez  

**Estándares relacionados:**
- EQ-03 — Diseño técnico justificable  
- EQ-05 — Código legible y mantenible  

---

## 10. Observaciones

La coherencia arquitectónica no implica rigidez absoluta.  
Implica que los cambios respeten la forma general del sistema o la modifiquen de forma consciente.

La arquitectura se degrada por pequeñas concesiones acumuladas, no por grandes decisiones.