# TelecomX_parte2_Latam
Challenge Telecom X análisis de evasión de clientes - Parte 2 - Alura Latam


# Informe de análisis de cancelación de clientes (Churn)

## 1. Desempeño de los modelos

Para predecir la cancelación de clientes se utilizaron distintos modelos de clasificación:

- **Baseline (DummyClassifier)**: utilizado como referencia mínima, prediciendo siempre la clase más frecuente.
- **Regresión Logística**
- **Random Forest**
- Versiones **balanceadas** de ambos modelos para compensar el desbalance de clases.

Los resultados muestran que los modelos de **Regresión Logística y Random Forest superan claramente al modelo baseline**, lo que indica que las variables del dataset contienen información relevante para explicar la cancelación de clientes.

El modelo **Random Forest** tiene la capacidad de capturar relaciones no lineales entre variables, mientras que **Regresión Logística** permite interpretar con mayor claridad el impacto de cada variable en la probabilidad de cancelación.

---

## 2. Variables más relevantes en la predicción

### Regresión Logística

El análisis de los coeficientes del modelo permite identificar qué variables aumentan o disminuyen la probabilidad de cancelación.

**Factores que aumentan la cancelación:**

- **Contrato mensual (Month-to-Month):** los clientes con contratos mensuales presentan mayor probabilidad de cancelar el servicio.
- **Cargos mensuales altos (MonthlyCharges):** clientes con facturas más elevadas tienden a cancelar con mayor frecuencia.
- **Tipo de servicio de internet:** ciertos servicios con mayor costo pueden aumentar el riesgo de cancelación.

**Factores que reducen la cancelación:**

- **Antigüedad del cliente (Tenure):** cuanto mayor es el tiempo que un cliente permanece en la empresa, menor es la probabilidad de cancelación.
- **Contratos de largo plazo (One year / Two year):** los contratos más largos generan mayor fidelización.

---

### Random Forest

El modelo Random Forest permite analizar la **importancia de las variables**, es decir, cuánto contribuye cada variable a mejorar las predicciones del modelo.

Las variables más relevantes identificadas fueron:

- **Tenure (antigüedad del cliente)**
- **MonthlyCharges (cargo mensual)**
- **TotalCharges (gasto acumulado)**
- **Tipo de contrato**
- **Tipo de servicio de internet**

Esto indica que la duración de la relación con el cliente y el costo del servicio son factores determinantes en la cancelación.

---

## 3. Factores principales que afectan la cancelación

A partir del análisis de ambos modelos, los factores más influyentes en la cancelación de clientes son:

- Baja antigüedad del cliente.
- Contratos mensuales sin compromiso a largo plazo.
- Cargos mensuales elevados.
- Tipo de servicio contratado.
- Menor gasto acumulado en el servicio.

Estos resultados sugieren que los clientes nuevos, con mayor costo mensual y sin contratos a largo plazo, presentan mayor riesgo de cancelar el servicio.

---

## 4. Estrategias de retención recomendadas

En base a los resultados obtenidos se proponen las siguientes estrategias para reducir la cancelación de clientes:

**1. Incentivar contratos de largo plazo**

Ofrecer descuentos o beneficios a clientes que cambien de contratos mensuales a contratos de mayor duración.

**2. Programas de fidelización temprana**

Los primeros meses del cliente son críticos. Se recomienda implementar estrategias de acompañamiento, beneficios o promociones para clientes nuevos.

**3. Optimizar la estructura de precios**

Revisar los planes con cargos mensuales elevados para mejorar su competitividad y evitar cancelaciones.

**4. Identificación de clientes en riesgo**

Utilizar los modelos predictivos desarrollados para identificar clientes con alta probabilidad de cancelación y aplicar acciones de retención antes de que abandonen el servicio.

---

## 5. Conclusión

El análisis demuestra que es posible predecir la cancelación de clientes utilizando modelos de machine learning con resultados superiores al modelo baseline.

Las variables más influyentes están relacionadas principalmente con la **antigüedad del cliente, el tipo de contrato y los cargos mensuales**. Implementar estrategias orientadas a fortalecer la relación con clientes nuevos, incentivar contratos de largo plazo y optimizar los planes de servicio puede contribuir significativamente a reducir la tasa de cancelación.

