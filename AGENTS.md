---
name: three-js-agent-skills
description: Patrones 3D con Three.js/WebGL: escenas, geometrías, shaders, animaciones, rendimiento y optimización de render.
---

# Three.js Agent Skill Directive

## Bootstrap de la Habilidad

Al detectar triggers de Three.js/WebGL (`$threejs`, `three.js audit`, `webgl patterns`, `3d web`):

1. `.skill/three-js-agent-skills/SKILL.md` ← Directiva principal
2. `.skill/three-js-agent-skills/core/commands.md` ← $-Comandos
3. `.skill/three-js-agent-skills/core/brain.md` ← Motor de decisiones

## Reglas Canónicas de Three.js

- **Dispose obligatorio**: Todo `Geometry`, `Material`, `Texture` y `RenderTarget` creado debe liberarse con `.dispose()` al destruir objetos para evitar fugas de memoria GPU.
- **Animation Loop**: Usar `requestAnimationFrame` a través del `renderer.setAnimationLoop()` de Three.js, nunca raw `requestAnimationFrame` externo.
- **Geometrías reutilizadas**: No crear instancias de geometría nuevas por objeto — usar instancias compartidas con `InstancedMesh` para objetos repetidos.
- **Texturas cacheadas**: Usar `TextureLoader` con caché explícito; nunca cargar la misma textura múltiples veces.
- **Separación de responsabilidades**: Lógica de escena separada de lógica de animación y de UI del framework.
