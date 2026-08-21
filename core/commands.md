# $-Comandos de Three.js

| Comando | Acción | Descripción |
|---|---|---|
| `$threejs` | Bootstrap | Inicializa la skill y carga contexto Three.js. |
| `$threejs:audit` | Auditoría | Escanea fugas de memoria GPU y antipatrones de render. |
| `$threejs:fix` | Remediación | Aplica dispose(), caching y optimizaciones del audit. |
| `$threejs:fix [ruta]` | Remediación puntual | Aplica fix a un archivo específico. |
| `$threejs:perf` | Performance | Analiza draw calls, geometrías instanciadas y texturas. |
