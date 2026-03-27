# 📊 RiskGuard-León-2026: Stress Testing de Cartera Patrimonial
### Análisis de Resiliencia Financiera ante Choques Inflacionarios (DTI 40%)

Este proyecto simula un **escenario de estrés severo** para una cartera de **100,000 socios** en León, Gto. El modelo evalúa la capacidad de pago real frente a créditos de alto impacto (Hipotecario/Automotriz) en un entorno de inflación quincenal del **0.62%** (Marzo 2026).

## 🎯 Criterios de Clasificación de Riesgo
Para determinar la salud financiera de cada socio, el modelo calcula el **Excedente Libre de Supervivencia**, definido como:
`Excedente = Ingreso Total - Canasta Básica Ajustada - Cuota de Crédito`

Se establecieron los siguientes rangos de clasificación:

| Estatus | Criterio (Excedente Mensual) | Significado Técnico |
| :--- | :--- | :--- |
| **🟢 Sano** | > $1,000 MXN | El socio cubre sus necesidades básicas y deuda con un margen para imprevistos. |
| **🟡 Riesgo Crítico** | $0 a $1,000 MXN | Capacidad de pago al límite. Cualquier variación en precios (luz, gas, gasolina) detona el impago. |
| **🔴 Mora Técnica** | < $0 MXN | **Insolvencia Matemática.** El ingreso no alcanza para cubrir la canasta básica y la cuota simultáneamente. |

---

## 🛠️ Metodología y Parámetros
- **Población:** 100,000 registros (Distribución Log-Normal ajustada a la ENOE León).
- **Ingreso Integral:** Incluye sueldo nominal + **12% de vales de despensa** (ajuste por sector manufacturero).
- **DTI (Debt-to-Income):** **40%**. Escenario de crédito patrimonial (Hipoteca/Auto).
- **Costo de Vida:** Canasta básica **CONEVAL ($4,877.87)** ajustada por inflación proyectada a Marzo 2026.

---

## 📈 Visualización del Análisis

### 1. Distribución del Ingreso Integral
La mediana real se desplaza a **$10,308 MXN** al integrar las prestaciones. Sin embargo, el grueso de la población permanece en niveles operativos, lo que acentúa la sensibilidad al costo de los alimentos.

<img width="902" height="566" alt="image" src="https://github.com/user-attachments/assets/f2a617e5-fd2a-4a8f-a56c-86c59c8e84e4" />


### 2. Diagnóstico Global de la Cartera
Bajo un DTI del 40%, la cartera muestra un quiebre estructural. El **24.0% en Mora Técnica** representa una pérdida esperada masiva si no se ajustan las políticas de originación.

<img width="777" height="550" alt="image" src="https://github.com/user-attachments/assets/b45dde94-ca4a-4d6d-8eb4-f40579245f4d" />



### 3. Probabilidad de Default (PD) por Decil
El hallazgo más crítico es la **contaminación del Decil 2**. Mientras que en créditos de consumo el riesgo se limitaba a la base extrema, en créditos patrimoniales el **40.5% de los trabajadores especializados** entra en insolvencia.

<img width="854" height="565" alt="image" src="https://github.com/user-attachments/assets/bf10c837-a8ff-4f86-8fd5-b61b040f9bb8" />


---

## 💡 Conclusiones Estratégicas
1. **Inviabilidad del DTI Estándar:** El estándar bancario del 30-40% es inviable para los Deciles 0, 1 y 2 en León bajo este escenario inflacionario.
2. **Recomendación:** Implementar un **"Piso de Excedente de Supervivencia"** de al menos $1,500 MXN fijos mensuales como requisito de aprobación, independientemente del porcentaje de DTI.
3. **Alerta de Mercado:** Las promociones agresivas de la competencia para estos segmentos ignoran el costo de la canasta básica, lo que representa una oportunidad de captar socios mediante "Compra de Cartera" con plazos más flexibles.

---
**Tecnologías:** Python (Pandas, NumPy, Seaborn)  
