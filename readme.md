**Modelo de Inteligencia Transaccional para la Prevención de Fraude Bancario (AML)**
![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)
![FastAPI](https://img.shields.io/badge/FastAPI-0.110.0-009688.svg)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-1.4.1-orange.svg)
![Power BI](https://img.shields.io/badge/Power_BI-Dashboard-F2C811.svg)

Este proyecto presenta una solución técnica integral para la gestión de riesgos operativos y la Prevención de Lavado de Dinero (AML). La plataforma transiciona de la validación tradicional basada en reglas fijas a la implementación de algoritmos de aprendizaje supervisado para la detección de anomalías transaccionales complejas.

**Impacto y Viabilidad Financiera**

El modelo está estructurado para evaluarse estrictamente como un proyecto de inversión. El pipeline analítico calcula los siguientes indicadores de rentabilidad (PnL):
* Retorno de Inversión (ROI): 257.2%
* Período de Recuperación (Breakeven): 1.3 meses
* Optimización Operativa: Reducción de costos por horas-hombre en la revisión de falsos positivos y mitigación de fricción con clientes legítimos (control de churn).

[Insertar aquí captura de pantalla - Vista de Impacto Financiero y Rentabilidad]

[Insertar aquí captura de pantalla - Vista de Monitoreo Transaccional]

**Arquitectura del Modelo**

El sistema opera bajo evaluación de riesgo híbrido:
1. Reglas de Negocio (40%): Evaluación heurística basada en canales de origen, geografía (países de alto riesgo FATF) y tipologías conocidas (Smurfing, Frecuencia Anormal).
2. Machine Learning (60%): Modelo predictivo de clasificación optimizado para maximizar la identificación de amenazas sin comprometer el gasto operativo mediante falsos positivos.

El feature engineering manual y la ponderación del score buscan equilibrar la interpretabilidad económica exigida por las normativas de cumplimiento con la precisión estadística del modelo.

**Estructura del Repositorio**

* `generadordata1.py`: Simulación de entorno transaccional y perfiles de riesgo.
* `atributosfe2.py`: Construcción de variables (feature engineering) basadas en comportamiento histórico y ventanas temporales.
* `modelo3.py`: Pipeline de entrenamiento, validación cruzada y selección del algoritmo óptimo.
* `impactofinanciero6.py`: Motor de cálculo económico para estructurar las métricas de rentabilidad y matrices de costos operativos.
* `API4.py`: Integración RESTful construida con FastAPI para la evaluación de transacciones y consulta de perfiles en tiempo real.
* `scriptpowerbi.py`: Ingesta y transformación de las tablas de hechos y dimensiones para su visualización en tableros de control gerencial.

**Notas de Validación y Limitaciones**
El sistema documentado en este repositorio utiliza datos generados mediante simulación para establecer un entorno controlado. Los niveles de accuracy observados responden a esta naturaleza sintética. Para su despliegue en un entorno de producción, la arquitectura requiere calibración con transacciones históricas reales y ajustes en los umbrales de decisión para prevenir anomalías estadísticas como el overfitting o el data leakage.

**Instrucciones de Ejecución**

Instalación de dependencias:
   pip install -r requirements.txt



**Guía de Uso**



Ejecución del Pipeline de Datos

Para procesar la información desde cero y entrenar el modelo, ejecute el script maestro:

python mainpipeline0.py



Este proceso generará los archivos transactions\_scored.csv y model\_best.pkl en el directorio de datos.



Inicio del Servidor de Inteligencia (API)

Para habilitar el monitoreo en tiempo real y los endpoints del dashboard, inicie el servidor:

uvicorn API4:app --reload



http://127.0.0.1:8000/docs



**Uso en Power BI Desktop**

Utilice el script scriptpowerbi.py dentro del entorno de Power BI para cargar las tablas de hechos y dimensiones procesadas por el modelo, permitiendo la creación de tableros de control para la toma de decisiones gerenciales

**Soporte y Ayuda**
Para dudas o errores, puedes abrir un issue en este repositorio o contactar directamente al desarrollador en: jsanchez.eco@outlook.com

**Contribuciones**
Este proyecto forma parte de un portafolio profesional, por lo que no está orientado a contribuciones externas. Sin embargo, se agradecen sugerencias o comentarios a través de issues.

**Mantenimiento**
Desarrollado y mantenido por Jose Luis Sanchez, economista enfocado en analítica y ciencia de datos.