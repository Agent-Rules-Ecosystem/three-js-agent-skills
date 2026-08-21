# Plantilla: Setup Canónico de Escena Three.js

Estructura mínima correcta para inicializar una escena Three.js con gestión de recursos:

```
// Patrón de implementación:
// 1. Crear renderer, scene, camera UNA SOLA VEZ
// 2. Usar renderer.setAnimationLoop() para el loop
// 3. Guardar referencias de todos los objetos creados
// 4. Implementar dispose() al destruir el componente:
//    - Detener animation loop
//    - Liberar geometrías, materiales y texturas
//    - Liberar renderer
//    - Remover el canvas del DOM

// Ver knowledge/memory_management.md para detalles de dispose
```
