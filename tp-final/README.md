<div align="center">
<h1>Invetigación: Plataforma financiera y predicción de riesgo político</h1>
</div>

## Necesidad de negocio 
#### Contexto
> Un fondo de inversión gestiona un portafolio diversificado: renta variable, bonos soberanos, materia prima, activos tecnológicos.

#### Áreas involucradas
> - Gerencia de riesgos
> - Mesa de operaciones
> - Equipo de investigación económica
> - Comité de inversiones

#### Problema actual
> Las decisiones de inversión frente a eventos políticos, desde elecciones o aprobaciones de leyes hasta regulaciones tecnológicas (por ejemplo, de IA) o cambios de tasas de interés, dependen altamente de encuestas tradicionales o reportes de consultoría política. Pero esta metodología presenta limitaciones: \
> - _Alta latencia._ 
> - _Sesgo de respuesta_ (desfase entre opinión declarada y comportamiento real). 
> - _Incapacidad de reacción_ (imposible ajustarse en tiempo real ante eventos de gran e inmediato impacto). 

#### Objetivo 
> Desarrollar una plataforma de Big Data que procese el flujo en tiempo real de mercados de predicción (Prediction Markets) y los relacione con indicadores socioeconómicos estructurales y la adopción de tecnologías estratégicas. La plataforma construirá un Índice Dinámico de Riesgo Político y Regulatorio (IDR-PR) para guiar la asignación de activos y la estrategia de cobertura en tiempo real.

#### Beneficios esperados
> 1. Optimización de coberturas (_hedging_), que se traduce en reducir las pérdidas de capital durante eventos de alta volatilidad política (por ejemplo, elecciones).
> 2. Anticiparse a cambios en la cotización de activos mediante la detección temprana de desplazamientos de probabilidad en eventos políticos clave (por ejemplo, regulaciones).
> 3. Automatizar procesamientos tradicionalmente manuales, que se traduce en reducción de falibilidad y tiempo (y, probablemente, empleados).

#### Evaluación de éxito
> El éxito de la propuesta se evaluaría de varias maneras, yendo de la validación técnica en desarrollo hasta el impacto económico, pasando por el rendimiento en producción:
> - **MLflow**
>   - **Registro y comparación de runs:** seguimiento continuo de parámetros, hiperparámetros y artefactos durante la etapa de experimentación.
>   - **Métricas de Aprobación (Gatekeepers):** para que un modelo sea promovido al estado `Production` en el **MLflow Model Registry**, debe alcanzar de manera consistente un **AUC-ROC > 0.82** y un **Brier Score < 0.15**.
> - **Desempeño y Observabilidad en Producción:**
>   - **Control de Drift:** seguimiento de *Data Drift* y *Concept Drift*.
>   - **Latencia:** alertas recalculadas en menos de 5 minutos tras cambios ≥ 5% en probabilidades clave.
