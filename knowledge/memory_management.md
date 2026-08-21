# Gestión de Memoria GPU en Three.js

## Regla de Oro: Dispose

**Todo recurso creado en Three.js debe liberarse explícitamente.** WebGL no tiene garbage collection automático para recursos GPU.

| Tipo de Recurso | Método de Liberación |
|---|---|
| `BufferGeometry` | `.dispose()` |
| `Material` (y variantes) | `.dispose()` |
| `Texture` | `.dispose()` |
| `WebGLRenderTarget` | `.dispose()` |
| `Mesh` | Geometry + Material `.dispose()` por separado |

## Antipatrones a Detectar

1. **Creación en bucle sin dispose**: Objetos creados en `requestAnimationFrame` sin liberación.
2. **Materiales únicos por objeto**: `new MeshStandardMaterial()` por cada instancia en lugar de compartir.
3. **Texturas re-cargadas**: `new TextureLoader().load(url)` repetido con la misma URL.
4. **Objetos eliminados sin dispose**: `scene.remove(mesh)` sin `mesh.geometry.dispose()` y `mesh.material.dispose()`.
