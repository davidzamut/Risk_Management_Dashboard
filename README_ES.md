# 🏦 Dashboard de Analítica de Riesgo Crediticio

![Status](https://img.shields.io/badge/Estado-En%20Progreso-yellow)
![Tool](https://img.shields.io/badge/Herramienta-Power%20BI-F2C811?logo=powerbi&logoColor=black)
![Data Processing](https://img.shields.io/badge/Datos-Power%20Query%20%7C%20DAX-blue)

## Resumen Ejecutivo
Este proyecto presenta un dashboard interactivo en Power BI diseñado para analizar y monitorear el riesgo crediticio en el portafolio de clientes del banco. 

En lugar de un modelo predictivo de caja negra, esta herramienta empodera a los tomadores de decisiones para identificar visualmente segmentos de alto riesgo, monitorear ratios financieros clave (como Deuda/Ingresos) y comprender el perfil de los clientes que caen en mora. El objetivo final es minimizar las pérdidas financieras y optimizar la estrategia de aprobación de créditos.

---

## 1. Entendimiento del Negocio

### El Problema
Las instituciones financieras pierden millones anualmente debido a la cartera vencida o préstamos incobrables ("Bad Debt"). Sin una visibilidad clara y en tiempo real de las características de los clientes morosos, los gerentes de riesgo no pueden ajustar sus políticas de crédito de manera efectiva.

### Objetivos
1.  **Identificar Impulsores de Riesgo:** Descubrir patrones demográficos y financieros asociados con el incumplimiento de préstamos (`TARGET = 1`).
2.  **Monitoreo del Portafolio:** Proveer una visión general del total de crédito en riesgo y las tasas de morosidad actuales.

### Métricas de Éxito (KPIs)
* **Exposición Total ($):** Monto total de crédito en riesgo.
* **Tasa de Morosidad (%):** Porcentaje de préstamos que han caído en incumplimiento.
* **Ratio Promedio Crédito/Ingreso:** Monitoreo del nivel de apalancamiento del cliente.
* **Años para Pagar la Deuda:** Monitoreo de factores de riesgo asociados con la duración del préstamo. 

---

## 2. Visión General de los Datos
**Fuente:** [Kaggle: Application Data](https://www.kaggle.com/datasets/dssouvikganguly/application-datacsv)  
**Dimensiones:** +455k filas, 122 columnas.

### Variables Clave:
* `TARGET`: 1 = Cliente cuyo préstamo fue aprobado, 0 = Préstamo denegado. *(Nota: Revisar esta definición según el objetivo real del negocio)*.
* `AMT_INCOME_TOTAL`: Ingresos totales del cliente.
* `AMT_CREDIT`: Monto de crédito del préstamo.
* `NAME_EDUCATION_TYPE`: Nivel máximo de educación alcanzado por el cliente.

---

## 3. Metodología y Modelado de Datos
Este proyecto sigue un flujo de trabajo estándar de Business Intelligence:

1.  **Ingesta y Transformación de Datos (vía CSV):** * Limpieza de valores nulos y estandarización de campos de texto.
    * Creación de columnas condicionales para grupos de edad y rangos de ingresos.
2.  **Modelado de Datos:** * Debido a la estructura del set de datos, no se requirió una fase de modelado compleja, ya que todas las características correspondían a una única tabla plana de clientes.
3.  **Medidas DAX:** * Desarrollo de medidas DAX personalizadas para KPIs dinámicos (ej. morosidad del año a la fecha, promedios móviles, segmentación dinámica).
4.  **Diseño del Dashboard:** * Construcción de una interfaz intuitiva centrada en la experiencia del usuario (UX), utilizando filtros cruzados, tooltips y funciones de *drill-through* para análisis profundos.

---

## 4. Principales Hallazgos (Insights)

* *Existe un total de 63 préstamos aprobados de alto riesgo que suman un total de $68.27 millones en posibles pérdidas.*
* *Hay alrededor de 3,789 préstamos no aprobados de bajo riesgo y alto valor que representan $860.4 millones en posibles ganancias perdidas.*
* *No se encontraron distinciones demográficas ni correlaciones significativas en este análisis.*

---

## 5. Cómo Interactuar con este Proyecto

### Visualización del Dashboard
* **Opción Local:** 1. Clona este repositorio.
  2. Asegúrate de tener instalado [Power BI Desktop](https://powerbi.microsoft.com/desktop/).
  3. Abre el archivo `Credit_Risk_Dashboard.pbix` ubicado en la carpeta `dashboards/`.

### Estructura del Repositorio



##  Recomendaciones para el Negocio
* Hay posibles oportunidades de creditos que pudieron ser aprovados siendo de bajo riesgo para la compañia que no lo fueron, es recomendable insistir en el manejo del riesgo en creditos que son de alto riesgo, sobre todo los otorgados a poblacion pensionada y que tienen
* un mayor riesgo de impago por condiciones relacionadas con la edad, en las que ademas el banco no cuenta con una garantia completa en caso de que los activos de dichas personas sean vendidos*

---

**Autor:** David Zamudio 
**Contacto:** www.linkedin.com/in/davidzamudiotab

