# EQ-16 — Consistencia entre entornos

## 1. Nombre del estándar
**ID:** EQ-16  
**Nombre:** Consistencia entre entornos

## 2. Propósito
Reducir errores derivados de diferencias ambientales.

## 3. Alcance
Aplica a dev, uat y prod.

## 4. Definición del estándar
El comportamiento debe ser consistente entre entornos.

## 5. Criterios de aceptación
- [ ] Configuración coherente
- [ ] Diferencias controladas
- [ ] Reproducción posible

## 6. Evidencias esperadas
- IaC
- configuraciones versionadas

## 7. Antipatrones comunes
- Configuración manual
- Entornos únicos

## 8. Nivel de criticidad
**Alto**

## 9. Relación con otras prácticas y estándares
Prácticas: 4  
Estándares: EQ-08

## 10. Observaciones
Entornos inconsistentes generan bugs fantasmas.