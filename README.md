# NFL Big Data Bowl UNAM · Equipo de Leo y Pablo

Base oficial del equipo para el evento del 20 de noviembre de 2026. La plantilla del organizador aporta la API de salud, el dashboard inicial, los archivos de bloqueo y el empaquetador. El ensayo de 2012 pertenece a la preparación previa.

## Pregunta para el coach

¿Qué situaciones de tercer down conviene priorizar en la revisión de video? Si el paquete incluye posiciones al snap, contrastaremos dos pronósticos de conversión: uno por distancia pendiente y otro que incorpora la posición defensiva. El tablero permitirá elegir una situación, revisar una jugada y consultar la frecuencia, el número de partidos y jugadas y el intervalo del 95%. El hallazgo oficial queda pendiente del dataset del evento.

La NFL ya publica el [Next Gen Stats Decision Guide](https://www.nfl.com/news/introducing-the-next-gen-stats-decision-guide-a-new-analytics-tool-for-fourth-do) para decisiones en cuarta oportunidad. Nuestra pregunta propuesta mide cuánto añade observar la defensa en tercera oportunidad sobre conocer las yardas pendientes.

## Trabajo del equipo

- **Leo · Arch · backend.** Inspeccionar columnas, unidades, claves y cobertura. Dividir por partidos antes del ajuste, congelar la hipótesis y comparar modelos en las mismas jugadas reservadas. Reportar la diferencia de Brier con intervalo pareado por partido y una explicación alternativa.
- **Pablo · Windows · frontend.** Mostrar una decisión, una jugada real y la evidencia agregada. Distinguir pronóstico y desenlace. Consumir la API con rutas relativas como `fetch('api/resumen')` y conservar `base: './'`.
- **Integración.** Trabajar desde la carpeta preparada por el instalador. Usar ramas del evento que partan de esta versión de main. Revisar los cambios en un pull request antes de integrarlos.

## Ejecutar y entregar

Consultar [INSTALACION.md](INSTALACION.md) y las [reglas del stack](.hackathon/rules.md). Python 3.12.12, uv 0.11.19, Node 22.23.1 y npm 10.x. Los archivos de bloqueo fijan las dependencias. El punto de entrada es `backend.main:app`. La plantilla responde a `GET /health`. Colocar los datos oficiales en `data/` y mantener las credenciales locales.

| Desde la raíz instalada | Arch | Windows PowerShell |
|---|---|---|
| Verificar | `sh .hackathon/setup.sh --check` | `.\.hackathon\setup.cmd --check` |
| Generar ZIP para AWS | `sh .hackathon/setup.sh --entregar` | `.\.hackathon\setup.cmd --entregar` |

Al cerrar, actualizar este README con el hallazgo confirmado, el tamaño de muestra, su incertidumbre, una jugada reproducible y una limitación. Probar la aplicación integrada y generar el ZIP oficial. Leo y Pablo deberán confirmar personalmente la declaración de autoría y fechas, distinguiendo la plantilla y la preparación previa de sus aportaciones durante el evento.
