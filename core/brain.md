# Motor de Decisiones — Three.js

## Flujo

```mermaid
graph TD
    A["Trigger ($threejs)"] --> B["$threejs:audit — Escanear escena"]
    B --> C{¿Hallazgos?}
    C -- No --> D["✅ Escena conforme"]
    C -- Sí --> E["Reporte Alta/Media/Baja"]
    E --> F["$threejs:fix — Remediar"]
    F --> G["Re-auditoría automática"]
```

## Matriz de Decisión

| Situación | Severidad | Acción |
|---|---|---|
| Objeto sin `.dispose()` | Alta | Fix inmediato — fuga de memoria GPU |
| Geometría duplicada por objeto | Alta | Migrar a `InstancedMesh` |
| Textura cargada múltiples veces | Media | Implementar caché de `TextureLoader` |
| Shader sin optimización | Baja | Sugerir mejora opcional |
