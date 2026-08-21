# Optimización de Render en Three.js

## Draw Calls

Reducir draw calls es el principal factor de rendimiento en escenas complejas:

| Técnica | Cuándo usar | Beneficio |
|---|---|---|
| `InstancedMesh` | Muchos objetos con misma geometría/material | 1 draw call por grupo |
| `merge` de geometrías | Objetos estáticos no interactivos | 1 draw call total |
| `LOD` (Level of Detail) | Objetos visibles a diferentes distancias | Reduce vértices procesados |
| `frustum culling` | Habilitado por defecto en Three.js | Omite objetos fuera de cámara |

## Antipatrones de Render

1. Crear nueva geometría por frame en el animation loop.
2. Modificar `geometry.attributes` cada frame sin `needsUpdate = true`.
3. Usar `scene.traverse()` en cada frame para buscar objetos.
4. Recrear materiales en lugar de actualizar `uniforms`.
