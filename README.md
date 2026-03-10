# TelecomX-LATAM-An-lisis-de-Evasi-n-de-Clientes-Churn-# 📊 TelecomX LATAM – Análisis de Evasión de Clientes (Churn)

## 📌 Descripción del Proyecto

Este proyecto analiza la **evasión de clientes (Churn)** en la empresa ficticia de telecomunicaciones **TelecomX LATAM**. El objetivo es identificar los factores que influyen en la cancelación del servicio y proponer estrategias para mejorar la **retención de clientes**.

En la industria de telecomunicaciones, **retener clientes existentes es significativamente más rentable que adquirir nuevos**, por lo que comprender las causas del churn permite diseñar acciones preventivas que mejoren la estabilidad del negocio.

---

## 🎯 Objetivos del Proyecto

- Analizar los factores asociados a la **cancelación de clientes**.
- Realizar **limpieza y transformación de datos** para mejorar su calidad.
- Desarrollar un **análisis exploratorio de datos (EDA)**.
- Crear **visualizaciones** que faciliten la interpretación de los resultados.
- Generar **recomendaciones estratégicas** basadas en los hallazgos del análisis.

---

## 🧹 Limpieza y Preparación de Datos

Los datos originales se encontraban en formato **JSON**, por lo que fue necesario realizar un proceso de **ETL (Extract, Transform, Load)**.

### Procesos realizados

**1. Normalización de datos**

Se expandieron las columnas:

- `customer`
- `phone`
- `internet`
- `account`

Esto permitió convertir los diccionarios en **variables independientes** para facilitar su análisis.

**2. Corrección de valores faltantes**

Se detectaron valores en blanco en la variable:

`Charges.Total`

Estos valores correspondían a clientes nuevos (`tenure = 0`). Se realizaron las siguientes acciones:

- Reemplazar valores vacíos por **0**
- Convertir la variable a formato **numérico (float)**

**3. Estandarización de variables**

Las variables categóricas como:

- PhoneService
- Dependents
- OnlineSecurity
- TechSupport

fueron transformadas a valores **binarios (1 y 0)** para facilitar el análisis y la posible aplicación de modelos predictivos.

**4. Ingeniería de variables**

Se crearon nuevas variables:

- **Cuentas_Diarias**  
  `Cargo mensual / 30`

- **Servicios**  
  Número total de servicios contratados por cliente.

---

## 📊 Análisis Exploratorio de Datos (EDA)

Durante el análisis se exploraron diferentes variables para entender el comportamiento del churn.

### Principales análisis realizados

- Distribución general de clientes que cancelan el servicio.
- Relación entre **tipo de contrato y churn**.
- Impacto del **método de pago** en la cancelación.
- Relación entre **antigüedad del cliente (tenure)** y churn.
- Influencia del **número de servicios contratados**.

Las visualizaciones incluyeron gráficos como:

- **Gráficos de barras**
- **Gráficos circulares**
- **Histogramas**
- **Gráficos comparativos**

---

## 📈 Principales Hallazgos

Del análisis realizado se identificaron varios patrones importantes:

- Los **clientes con contratos mensuales (Month-to-Month)** presentan la mayor tasa de cancelación.
- La mayoría de cancelaciones ocurre durante los **primeros meses de relación con la empresa**.
- Los clientes que utilizan **Electronic Check** como método de pago tienen mayor probabilidad de churn.
- Los clientes con **mayor número de servicios contratados** presentan mayor fidelización.

---

## 💡 Recomendaciones

A partir de los resultados obtenidos, se proponen las siguientes estrategias:

### Incentivar contratos a largo plazo
Ofrecer descuentos o beneficios para clientes que migren de **Month-to-Month** a contratos de **1 o 2 años**.

### Programa de fidelización temprana
Implementar estrategias de seguimiento durante los **primeros 3 a 6 meses**, etapa donde ocurre la mayor tasa de cancelación.

### Incrementar la contratación de servicios
Promover servicios adicionales como:

- Online Security  
- Tech Support  
- Backup en la nube  

Esto puede mejorar significativamente la retención.

### Optimizar métodos de pago
Promover métodos automáticos como:

- Débito automático
- Tarjeta de crédito

para reducir el uso de **Electronic Check**.

---

## 🛠 Tecnologías Utilizadas

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Google Colab / Jupyter Notebook

---

## 📂 Estructura del Proyecto
