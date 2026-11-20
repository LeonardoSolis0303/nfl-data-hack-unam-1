# Propuesta de contrato — GET /api/resumen

**BORRADOR, NO IMPLEMENTADO NI VALIDADO.** El responsable del backend y el responsable del dashboard deben acordar los nombres de los campos antes de escribir código que dependa de ellos.

## Objetivo
Que el backend entregue un resumen estadístico reproducible para un dashboard que estudia conversión de tercer down según distancia pendiente.

## Información mínima que se debe acordar
| Concepto | Semántica requerida |
|---|---|
| Procedencia | `real`, `demo` o `no_disponible`, con identificación del conjunto y periodo cuando se conozcan |
| Muestra | Número de jugadas y, si se conoce, partidos; identificar entrenamiento vs. evaluación |
| Bandas de distancia | Definiciones explícitas, tamaño de muestra, conversiones y tasas |
| Incertidumbre | IC 95 % con límites y método estadístico documentado |
| Pronóstico | Probabilidad del modelo separada del resultado observado |
| Brier | Valor y metodología de evaluación; intervalo solo si se calculó |
| Ejemplo de jugada | Identificadores, distancia, ganancia, resultado y predicción disponible |
| Tracking | Datos espaciales o `null` si están ausentes |
| Errores | Respuestas HTTP claras ante ausencia o incompatibilidad del CSV |

## Reglas de interpretación
- Convención recomendada para probabilidades: valores entre 0 y 1. Confirmar contra el backend antes de programar.
- `null` significa dato no disponible, nunca 0.
- Un HTTP 200 no prueba que el cálculo fue realizado. El backend debe exponer o documentar origen, versión y metodología.
- No sustituir errores de procesamiento por las cifras de práctica.
- Datos de práctica NFL 2012 deben identificarse como **demo** cuando sean usados para construir la interfaz.
- Las cifras de referencia de ensayo (2,649 jugadas, 128 partidos, Brier 0.2208, intervalo [0.2158, 0.2259]) no constituyen por sí mismas datos verificables del backend.

## Criterio de integración
Primero acordar un ejemplo JSON real, luego validar el tipo y la petición en el frontend, finalmente comprobar que las cifras visualizadas coinciden con la respuesta de la API.
