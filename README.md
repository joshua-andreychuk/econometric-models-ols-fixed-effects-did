# econometric-models-ols-fixed-effects-did

# **Predictive Analytics: Fixed Effects and Difference-in-Differences (DiD) Models with Stata**

This project applies various **OLS-based econometric models** to analyze business data using **Stata**. The key objectives include estimating the **demand elasticity** for beer and evaluating the impact of Sunday store hours on profitability through **causal inference techniques** like **fixed effects** and **difference-in-differences (DiD)**.

---

## **Technologies Used**

- **Stata**:  
  Statistical software for data analysis, used to run **OLS-based regression models** (e.g., fixed effects and DiD). In this project, Stata is applied to estimate demand elasticity for beer and the impact of Sunday store hours on profits.

- **OLS (Ordinary Least Squares) Regression**:  
  The core statistical method across all models. Enhancements such as **fixed effects** and **DiD** build upon OLS by introducing controls for confounding factors.

- **Difference-in-Differences (DiD)** (Causal Inference Technique):  
  Applied to the **store profits analysis** to evaluate how Sunday hours affect profitability. This model uses interaction terms between treatment and time variables to isolate causal impacts.

- **Fixed Effects Models** (Causal Inference Technique):  
  Used to control for **unobserved, time-invariant factors**. In the **beer demand analysis**, fixed effects account for **brand-specific characteristics**. In the **store profits analysis**, they control for **state and time effects**, improving causal estimates by reducing confounding.

---

## **Project Overview**

### **1. Demand for Beer**
- **Goal**: Estimate the price elasticity of demand for beer by analyzing sales data.
- **Models Used**:
  - **OLS Regression**: Log(quantity) regressed on log(price) without brand controls to examine potential biases.
  - **Brand Fixed Effects**: Incorporates brand dummy variables to control for unobserved brand-specific factors (e.g., reputation, marketing).

- **Findings**:
  - Without brand controls, the price-quantity relationship shows a **positive bias of +0.63%**, indicating a misleading increase in demand with rising prices.
  - Adding brand controls yields a corrected price elasticity of **-2.87%**, indicating that a 1% price increase decreases demand by approximately 2.87%.

---

### **2. Impact of Sunday Hours on Store Profits**
- **Goal**: Assess how changes in store Sunday hours affect profitability.
- **Models Used**:
  - **Fixed Effects Model (State-Level)**: Controls for unobserved, state-specific factors such as regional business regulations.
  - **Fixed Effects with Time Controls**: Adds time fixed effects to account for national trends (e.g., seasonality).
  - **Difference-in-Differences (DiD)**: Uses interaction terms to compare profit trends between treated and control stores over time.

- **Findings**:
  - Without time controls, an additional hour of Sunday operations results in a **$33.68** decrease in profits.
  - With both state and time fixed effects, the decrease is estimated at **$68.42** per hour, isolating the effect of Sunday hours.

---

## **Data Overview**

The project uses two datasets:

1. **Beer Sales Data**:  
   Contains price, quantity, and brand information for various stores.

2. **Store Profits Data**:  
   Tracks profits, hours of operation, and state/time characteristics over multiple time periods.

---

## **Results Summary**

### **Beer Demand Analysis**
- Without brand controls, the model shows a **positive price-quantity bias of +0.63%**, suggesting omitted variable bias due to unobserved brand factors.
- Including brand fixed effects yields a corrected elasticity of **-2.87**, confirming that price increases reduce demand significantly.

### **Store Profits Analysis**
- Sunday hours reduce profits significantly:
  - **Without time controls**: Profits decrease by **$33.68** per additional hour.
  - **With time and state fixed effects**: Profits decrease by **$68.42**, accounting for broader seasonal and national trends.
