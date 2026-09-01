# 🎲 Three.js Agent Skill

> **Skill especializada** — Auditoría y optimización de escenas 3D con Three.js/WebGL.
> Skill de tipo **Especializada Web** (requiere `web-agent-rules` como base).

---

## 📌 Propósito y Alcance

1. 🔍 **Auditar** fugas de memoria GPU (dispose, geometrías, texturas).
2. 🛠️ **Detectar** antipatrones de render (draw calls excesivos, geometrías duplicadas).
3. 📐 **Validar** el animation loop y gestión de frames.
4. 🔧 **Optimizar** con InstancedMesh, caché de texturas y LOD.
5. 📋 **Reportar** deuda técnica de rendimiento 3D.

---

## ⚡ $-Comandos

| Comando | Acción |
|---|---|
| `$threejs` | Bootstrap |
| `$threejs:audit` | Auditoría completa de escena |
| `$threejs:fix` | Remediación post-audit |
| `$threejs:perf` | Análisis de performance de render |

---

## ⚡ Quick Start

**1. Instala la skill como submódulo**
```bash
git submodule add git@github.com:Agent-Rules-Ecosystem/three-js-agent-skills.git .skill/three-js-agent-skills
```

**2. Activa la skill con `$boot`**
```text
$boot
```

**3. Ejecuta el primer comando de la skill**
```text
$work agregar escena 3D básica con controles de órbita
```

---

