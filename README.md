# NFL Big Data Bowl — UNAM

Repositorio compartido para preparar una demostración de análisis deportivo centrada en la **probabilidad de convertir un tercer down según las yardas pendientes**.

> **Estado actual:** estructura inicial de colaboración. Todavía no hay un backend estadístico ni una aplicación React funcional publicados en este repositorio. Los indicadores de práctica no constituyen una validación del modelo.

## Organización

| Área | Ruta | Rama de trabajo |
|---|---|---|
| Frontend: dashboard y presentación | `dashboard/` | `frontend` |
| Backend: datos, modelo y API | `backend/` | `backend` |
| Reglas compartidas de Kiro | `.kiro/steering/rules.md` | `main` (mediante PR) |
| Documentación y contrato propuesto | `docs/` | `main` (mediante PR) |
| Orientaciones sobre datos | `data/README.md` | Compartido |

Los dos integrantes usan **clones locales independientes** y sus propias sesiones de Kiro. GitHub sincroniza el código a través de commits, ramas y pull requests, no las conversaciones de los agentes.

## Empezar

Clonar el repositorio en una **carpeta nueva**:

```bash
git clone https://github.com/LeonardoSolis0303/nfl-data-hack-unam-1.git
cd nfl-data-hack-unam-1
```

En Kiro, usar **Clone Repository** y pegar esa misma URL; abrir la carpeta clonada.

Para el integrante de frontend:
```bash
git switch --track origin/frontend
```

Para el integrante de backend:
```bash
git switch --track origin/backend
```

Si alguna de esas ramas ya existe localmente, usar `git switch frontend` o `git switch backend`.

Lee [la guía de colaboración](docs/COLABORACION.md) antes de subir cambios.

## Integración propuesta

Se propone que el backend exponga **`GET /api/resumen`** y entregue estimaciones, tamaños muestrales, intervalos de confianza y metadatos de procedencia. **El endpoint aún no está implementado aquí**; su contrato debe acordarse en [docs/CONTRATO_API.md](docs/CONTRATO_API.md).

El frontend debe distinguir claramente:
- Conversión observada vs. probabilidad pronosticada.
- Resultado calculado desde datos vs. demostración temporal.
- Información ausente (`null`) vs. cero.

## Seguridad de datos

Este repositorio es actualmente **público**. No subas CSV de distribución restringida, claves, tokens, contraseñas ni archivos `.env`. Los datos locales bajo `data/` están excluidos por defecto mediante `.gitignore`.

## Pendientes

1. Incorporar el código inicial del frontend desde el clon del responsable.
2. Incorporar el código del backend desde el clon del compañero.
3. Acordar el contrato JSON de `/api/resumen`.
4. Ejecutar y registrar las pruebas de ambos componentes antes de declarar la demostración lista.
