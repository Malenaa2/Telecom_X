# Telecom_X
# 📊 Proyecto Telecom X - Análisis de Evasión de Clientes (Churn)

## 📌 Descripción General
Este proyecto forma parte del desafío *Telecom X - Alura Latam, cuyo objetivo es analizar la evasión de clientes (*churn) a partir de datos históricos.  
Se busca identificar patrones y factores asociados a la pérdida de clientes, para luego proponer estrategias de retención.

El análisis incluye:
- Limpieza y normalización de datos.
- Tratamiento de valores nulos y duplicados.
- Conversión de variables a formatos adecuados.
- Análisis exploratorio con visualizaciones.
- Conclusiones y recomendaciones estratégicas.

---

## 🗂 Estructura del Proyecto
1. *Configuración Inicial*  
   - Importación de librerías necesarias.
   - Configuración visual para gráficos.
   - Supresión de advertencias innecesarias.

2. *Extracción de Datos*  
   - Importación desde archivo JSON provisto por el desafío.
   - Carga de datos en un DataFrame de pandas.

3. *Inspección Inicial*  
   - Tipos de datos y vista rápida (df.info(), df.sample()).
   - Resumen estadístico de variables numéricas y categóricas.
   - Conteo de valores únicos por columna.

4. *Comprobación de Incoherencias*  
   - Detección de registros duplicados.
   - Detección de valores nulos.
   - Revisión de valores en variables categóricas.

5. *Limpieza y Tratamiento de Datos*  
   - Renombrado de columna Churn si viene con nombre distinto (ej: customer.Churn).
   - Normalización de Churn a formato binario (0 = Se queda, 1 = Se va).
   - Conversión de columnas numéricas (tenure, MonthlyCharges, TotalCharges) a tipo numérico.
   - Manejo de valores fuera de rango y nulos.

6. *Análisis Exploratorio de Datos (EDA)*  
   - *Distribución Global de Churn*  
     Gráfico de barras para visualizar clientes que se quedan vs. se van.  
   - *Análisis por Variables Categóricas*  
     - Contrato.
     - Método de pago.
     - Servicios contratados.  
     Se usan countplot y porcentajes.
   - *Análisis por Variables Numéricas*  
     - tenure, MonthlyCharges, TotalCharges.  
     Histogramas con separación por churn y boxplots comparativos.

7. *Resultados y Hallazgos Clave*  
   - Mayor churn en contratos *Month-to-month*.
   - El método de pago *Electronic check* presenta mayor tasa de bajas.
   - Los clientes con menor antigüedad (tenure bajo) tienen más probabilidad de irse.

8. *Recomendaciones Estratégicas*  
   - Incentivar contratos de mayor plazo con beneficios escalonados.
   - Revisar la experiencia de clientes que pagan con *Electronic check*.
   - Implementar programas de fidelización temprana.

---

## 📈 Principales Métricas
- *Tasa de churn*: ~26.54%
- *Clientes analizados*: N registros finales (luego de limpieza).
- *Variables clave*: Contract, PaymentMethod, tenure, MonthlyCharges, TotalCharges.

---

## 📊 Visualizaciones Incluidas
- Distribución global de churn.
- Churn por contrato.
- Churn por método de pago.
- Histogramas de variables numéricas separadas por churn.
- Boxplots comparativos.

---

## 🛠 Tecnologías Utilizadas
- *Python 3.10+*
- *Pandas* → manipulación de datos.
- *NumPy* → operaciones numéricas.
- *Matplotlib / Seaborn* → visualización de datos.
- *Requests* → extracción de datos desde fuente online.

---

## 🚀 Cómo Ejecutar el Proyecto
1. Clonar el repositorio:
   ```bash
   git clone https://github.com/usuario/telecom-x-churn.git
   cd telecom-x-churn
