# Reglas compartidas — NFL Big Data Bowl UNAM

Estas reglas se aplican a ambos integrantes y sus agentes de Kiro cuando trabajan en este repositorio.

## Propósito
Desarrollar una demostración reproducible sobre la probabilidad de conversión en tercer down. El repositorio comienza como **estructura de colaboración**: no presupongas que existe un modelo, un CSV cargado ni un backend funcional.

## Responsabilidades
- **Frontend / rama `frontend`:** `dashboard/`, visualización, manejo de errores, accesibilidad y documentación de presentación.
- **Backend / rama `backend`:** `backend/`, carga autorizada de datos, procesamiento, modelos, pruebas estadísticas y servicio de API.
- **Compartidos:** `.kiro/`, `docs/`, `README.md` y configuración raíz. Coordinar antes de modificarlos.

## Normas de seguridad y colaboración
1. Leer `git status`, `git branch --show-current` y los archivos relevantes antes de editar.
2. No usar `git push --force`, `git reset --hard`, `git clean -fd` ni borrados masivos.
3. No cambiar de rama, integrar commits, eliminar archivos o modificar el área del compañero sin indicación del usuario.
4. Trabajar en la rama asignada. Abrir pull request hacia `main`; no mezclar cambios sin revisión.
5. Nunca subir tokens, contraseñas, `.env`, archivos privados, CSV no autorizados ni conjuntos de datos oficiales con restricciones de distribución.
6. Si un comando falla, registrar la salida; no declarar pruebas exitosas que no se ejecutaron. Ante fallos repetidos de terminal, parar y explicar el bloqueo.
7. Conservar implementaciones existentes y preferir correcciones pequeñas; no iniciar un proyecto nuevo sin autorización.

## Integridad de los datos
- El **backend** calcula métricas y entrega la información al frontend. El frontend no inventa estadísticas.
- Distinguir siempre `real`, `demo` y `no_disponible`, conforme al contrato acordado.
- El valor `null` no significa cero. Sin posiciones, mostrar **Seguimiento pendiente**; no inventar tracking.
- Probabilidades pronosticadas, tasas observadas y desenlaces binarios son cantidades distintas.
- Los valores históricos de ensayo (2,649 jugadas, 128 partidos, Brier 0.2208) no deben incorporarse como cálculos reales sin datos y validación.
- No afirmar que una API procesa CSV solo porque devuelve HTTP 200.

## Verificación
- **Verificado:** prueba ejecutada con salida observada.
- **Inspeccionado:** código leído sin ejecución.
- **No verificado / bloqueado:** no se pudo ejecutar la prueba.
- Para considerar funcional la demo: build del frontend, respuesta API válida, origen de los datos identificado y comprobación visual cuando sea posible.

Consulta `docs/COLABORACION.md` y `docs/CONTRATO_API.md` antes de integrar cambios.
