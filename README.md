# MotosCloud — Búsqueda y recomendación de motos en la nube

**Autor:** Juan Antonio Rodríguez Martínez  
**Asignatura:** Cloud Computing: Fundamentos e Infraestructuras  
**Estado (Hito 1):** Definición de problema, alcance cloud, MVP y documentación enlazada.

## 1. ¿Qué problema resuelve?
El mercado de motos de segunda mano está disperso y es difícil comparar opciones rápidamente. Los compradores necesitan **búsqueda con filtros avanzados** (marca, precio, km, año, ubicación) y **recomendaciones**; los vendedores necesitan **estadísticas** y **alertas**.

## 2. Por qué desplegarlo en la nube
- **Escalabilidad** de búsquedas y recomendaciones ante picos.
- **Procesamiento** de datos de múltiples fuentes (en el futuro).
- **Servicios** desacoplados: búsqueda, recomendaciones y alertas como componentes independientes.

## 3. Lógica de negocio (resumen)
- Ingesta/indexación de listados de motos.
- Búsqueda con filtros + ordenación por relevancia (precio/km).
- Recomendaciones iniciales (MVP) por similitud de marca/modelo/rango de precio (sin ML).
- Suscripción a criterios para alertas de precio/disponibilidad (simulada en MVP).

## 4. Historias de usuario (ejemplos)
- *Como comprador*, quiero filtrar por marca, precio y km para encontrar motos acordes a mi presupuesto.
- *Como comprador*, quiero recibir un aviso cuando aparezca una moto que cumpla mis criterios.
- *Como vendedor*, quiero conocer el precio medio de mercado para publicar con un precio competitivo.

## 5. MVP (producto mínimo viable)
**Stack inicial:** FastAPI + Python, `uvicorn`, datos de ejemplo (JSON) o SQLite.  
**Endpoints (plan):**
- `GET /motos?marca=&modelo=&precio_min=&precio_max=&km_max=&ubicacion=`
- `GET /motos/{id}`
- `POST /alerts` (simulado: guarda suscripción en memoria/JSON)

Con esto ya hay lógica de negocio server-side y valor claro en cloud.

## 6. Roadmap (encaja con próximos hitos)
- **Hito 2 (CI):** GitHub Actions (lint + tests).
- **Hito 3 (Microservicios):** separar `search`, `reco`, `alerts`.
- **Hito 4 (Composición):** API Gateway + eventos/colas.
- **Hito 5 (PaaS):** despliegue (Railway/Fly.io/Render).

## 7. Buenas prácticas de repositorio
- Commits pequeños y descriptivos.
- Issues ligadas a commits (`closes #N`).
- `.gitignore` desde el inicio.
- Nada de binarios; releases si es necesario.
- Si se reusa código externo, usar *fork* o dependencia declarada.

## 8. Documentación por hitos
- 📄 [Hito 1 — Repositorio y definición](docs/hito1.md)

## Licencia
MIT — ver [LICENSE](LICENSE).
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
