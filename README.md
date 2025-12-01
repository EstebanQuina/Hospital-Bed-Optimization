# Optimizing Hospital Bed Utilization using Linear Programming

## 📌 Project Overview
This project applies **Operations Research (OR)** techniques to optimize bed allocation in a 136-bed hospital facing volatile demand. Using **Linear Programming (LP)**, we minimized patient refusals by **6%** in the baseline scenario and developed a "Velocity Strategy" (reducing Length of Stay) to handle a **600% demand surge** during a simulated pandemic.

## 🛠️ Tools & Technologies
* **Language:** Python (Pandas, Matplotlib, Seaborn)
* **Optimization:** ZIMPL (Modeling Language), SCIP (Solver)
* **Documentation:** LaTeX

## 📂 Key Components

### 1. Data Cleaning & Analysis
We analyzed historical data for 52 weeks. A critical finding was a **Staff ID mismatch** between the schedule and master list, which required data reconciliation to accurately calculate labor constraints.

### 2. Baseline Optimization (Scenario A)
We modeled the problem as a Minimization of Weighted Unmet Demand.
* **Objective:** Minimize penalties for refusing patients.
* **Priorities:** ICU ($10,000$) > Emergency ($100$) > Surgery ($10$) > GenMed ($1$).
* **Result:** Reduced annual refusals from **7,642** to **7,181**.

### 3. Pandemic Simulation (Scenario B)
We simulated a crisis starting in Week 12:
* **Constraint:** ICU demand skyrocketed by 600%.
* **Strategy:** Reduced ICU Length of Stay (LOS) from 7.6 days to 2 days.
* **Outcome:** The "High Velocity" strategy allowed 100% acceptance of infected patients but required the ICU to consume 55% of total hospital capacity, crowding out other services.

