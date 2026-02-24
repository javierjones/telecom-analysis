# 📊 Proyecto: Análisis de Uso de Clientes -- ConnectaTel

## 🎯 Objetivo del Proyecto

El objetivo es analizar cómo los clientes utilizan realmente los
servicios móviles (llamadas y mensajes) para:

-   Identificar patrones reales de consumo.
-   Detectar comportamientos atípicos (outliers).
-   Segmentar clientes por nivel de uso y edad.
-   Generar conclusiones accionables para optimizar la oferta comercial.

------------------------------------------------------------------------

## 📂 Datasets Utilizados

El proyecto se basa en tres datasets estructurados que simulan operaciones reales de telecomunicaciones.

---

### plans.csv

Contiene la estructura comercial de los planes ofrecidos por ConnectaTel.

| Columna             | Descripción                       |
| ------------------- | --------------------------------- |
| `plan_name`         | Nombre del plan (Basico, Premium) |
| `messages_included` | Mensajes incluidos por mes        |
| `gb_per_month`      | GB incluidos por mes              |
| `minutes_included`  | Minutos incluidos por mes         |
| `usd_monthly_pay`   | Pago mensual en USD               |
| `usd_per_gb`        | Costo por GB adicional            |
| `usd_per_message`   | Costo por mensaje adicional       |
| `usd_per_minute`    | Costo por minuto adicional        |

Este dataset define la estructura económica del servicio y permite comparar el uso real con los beneficios del plan.

---

### users_latam.csv

Contiene información demográfica y de suscripción de cada cliente.

| Columna      | Descripción                        |
| ------------ | ---------------------------------- |
| `user_id`    | Identificador único del cliente    |
| `first_name` | Nombre                             |
| `last_name`  | Apellido                           |
| `age`        | Edad                               |
| `city`       | Ciudad de residencia               |
| `reg_date`   | Fecha de registro                  |
| `plan`       | Plan contratado (Basico o Premium) |
| `churn_date` | Fecha de cancelación (si aplica)   |

Este dataset permite segmentación demográfica y análisis por tipo de plan.

---

### usage.csv

Contiene el registro histórico de actividad a nivel de evento.

| Columna    | Descripción                               |
| ---------- | ----------------------------------------- |
| `id`       | Identificador único del evento            |
| `user_id`  | Identificador del cliente (clave foránea) |
| `type`     | Tipo de evento (`call` o `text`)          |
| `date`     | Fecha y hora del evento                   |
| `duration` | Duración de la llamada (solo para `call`) |
| `length`   | Longitud del mensaje (solo para `text`)   |

Nota importante:

* `duration` solo aplica a llamadas.
* `length` solo aplica a mensajes.

------------------------------------------------------------------------

## ▶️ Cómo Ejecutarlo

### Opción 1 -- Google Colab (Recomendado)

1.  Subir el notebook a https://colab.research.google.com\
2.  Subir los datasets
3.  Ejecutar todas las celdas en orden

------------------------------------------------------------------------

## 🔁 Reproducibilidad

-   Colocar el notebook en el directorio /notebooks
-   Colocar los datasets en el directorio /datasets/
-   Ejecutar las celdas en orden
-   Completar los pasos de limpieza antes del análisis

------------------------------------------------------------------------

## 📌 Hallazgos Clave

-   El comportamiento de uso es más determinante que la edad.
-   La mayoría de clientes pertenece al segmento de uso medio.
-   Existe un segmento pequeño de alto consumo con alto valor
    estratégico.
-   Los outliers representan usuarios reales intensivos.
-   Hay oportunidades para alinear mejor los planes con el uso real.
