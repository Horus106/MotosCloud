# Hito 1 — Repositorio y definición del proyecto

**Proyecto:** MotosCloud  
**Autor:** Juan Antonio Rodríguez Martínez

## 1) Entorno y configuración (evidencias)
- `git` instalado (CLI).
- **SSH**: clave generada y subida a GitHub (capturas en `docs/imgs/`):
  - `ssh-keygen -t ed25519 -C "jantoniorodma@correo.ugr.es"`
  - Subida a GitHub (Settings → SSH and GPG keys).
  - Prueba: `ssh -T git@github.com`.
- `git config`:
  - `git config --global user.name "Juan Antonio Rodríguez Martínez"`
  - `git config --global user.email "jantoniorodma@correo.ugr.es"`
- Perfil GitHub actualizado (avatar, nombre, ciudad, universidad). **Captura** en `docs/imgs/`.
- **2FA activado**. **Captura** en `docs/imgs/`.
- `.gitignore` desde el inicio.

> Las capturas se incluyen en `docs/imgs/`.

## 2) Issues y milestone
- Milestone: **Hito 1**.
- Issues creadas y cerradas con commits (`closes #N`):
  1. Inicializar repo y estructura (`README`, `LICENSE`, `.gitignore`).
  2. Redactar definición del problema y MVP en `README`.
  3. Crear `docs/hito1.md` con evidencias y checklist.
  4. Añadir plantillas de issues (`.github/ISSUE_TEMPLATE`).

## 3) Problema y MVP
- **Problema**: mercado disperso; necesidad de búsquedas avanzadas y recomendaciones.
- **MVP**: API en FastAPI con filtros básicos, datos JSON/SQLite, endpoint de alertas simulado.
- **Ventaja cloud**: escalado, servicios desacoplados, agregación de fuentes futuras.

## 4) Enlace para corrección
**Enlace al repo:**
`https://github.com/Horus106/MotosCloud`

**Enlace a este Hito 1:**  
`https://github.com/Horus106/MotosCloud/blob/main/docs/hito1.md`

## 5) Checklist del Hito 1
- [x] `README.md` con problema, MVP, historias y enlaces.
- [x] `LICENSE` (MIT).
- [x] `.gitignore` activo.
- [x] Documentación de entorno (SSH, 2FA, perfil, `git config`).
- [x] Issues + milestone creados y cerrados con commits.
