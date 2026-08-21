---
name: three-js-agent-skills
description: Patrones 3D con Three.js/WebGL.
---

# Three.js Skill Matrix

## Capacidades

```mermaid
graph LR
    A[THREEJS] --> B[Auditoría de Escena]
    A --> C[Gestión de Memoria GPU]
    A --> D[Optimización de Render]
    A --> E[Patrones de Animación]
```

## Protocolo de Auditoría (`$threejs:audit`)

1. Detectar archivos con inicialización de Three.js
2. Verificar dispose() en objetos de escena
3. Detectar creación de geometrías/texturas duplicadas
4. Revisar animation loop y gestión de frames
5. Reporte por severidad: fugas GPU (Alta) / antipatrones de render (Media) / mejoras opcionales (Baja)
