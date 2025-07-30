# Advanced Excel: Transportation Optimisation for Westvaco Logistics

This project tackles a **real-world transportation optimisation problem** for **Westvaco**, a major U.S. manufacturer of paper products. The focus is on minimising the shipping costs from its **Wickliffe paper mill** to six distribution destinations using six third-party truck carriers, while navigating complex business constraints.

---

## 🚚 Business Context

- **Company**: Westvaco  
- **Industry**: Paper and packaging manufacturing  
- **Production Sites**: 5 paper mills, 4 chemical plants  
- **Problem Origin**: Wickliffe, Kentucky Mill  
- **Distribution Task**: Assign daily truckloads to carriers to satisfy demand at 6 destinations  
- **Goal**: Minimise transportation costs while maintaining fairness, operational feasibility, and carrier commitment

---

## ❓ Problem Description

Every morning, transportation planners must allocate ~33 truckloads of paper. This involves:

- Choosing from 6 carriers with route availability, capacity, rates, and stop-off charges.
- Meeting delivery demands for six destinations over a five-day schedule.
- Honouring daily or weekly commitments to each carrier.
- Managing complexity by limiting the number of carriers used.

The challenge is to assign carriers to truckloads **at minimal cost** without violating constraints.

---

## 📊 Optimization Approach

We used **Integer Linear Programming (ILP)** with **Excel Solver (Simplex LP method)**.

### 🔁 Step 1: Data Preprocessing

- Replaced unavailable routes ("*") with high penalties (`999`) to exclude them.
- Calculated per-trip transportation costs:

### 🧩 Step 2: Model Formulation

#### Model 1: Cost Minimisation
- Minimise total cost while meeting destination demand and respecting carrier capacity.

#### Model 2: Fair Allocation
- Adds carrier commitment constraints to distribute truckloads fairly:
- **Model 2-1**: Daily commitment (0–5 trucks/day)
- **Model 2-2**: Weekly commitment (0–32 trucks/week)

#### Model 3: Carrier Reduction
- Adds binary decision variables to **minimise the number of active carriers** with minimal cost impact.

### ⚙️ Step 3: Excel Solver Setup

- Models are implemented on separate worksheets.
- Solver setup includes objective cell, variable ranges, and constraints.
- Visualisations created to analyse cost sensitivity.

---

## 💡 Key Insights

| Model     | Scenario            | Total Cost    | Notes                                      |
|-----------|---------------------|---------------|--------------------------------------------|
| Model 1   | Cost only           | $93,774.16    | Baseline, lowest-cost option               |
| Model 2-1 | Daily commitment    | Higher        | Cost increases with stricter commitments   |
| Model 2-2 | Weekly commitment   | Lower         | More flexible, cost-effective              |
| Model 3   | Carrier reduction   | ~$93,839.56   | Slight increase, simplifies operations     |

- **Weekly commitments** are more efficient than daily ones.
- **Reducing active carriers** slightly raises cost but lowers complexity.
- Visual trends shown in Figures 8–10 (in report) support strategic decision-making.

---

## 🛠 Tools Used

- Microsoft Excel with Solver Add-in
- Integer Linear Programming (Simplex LP)
- Scenario testing and cost visualisations

---

## 📂 Files Included

| File                                | Description                                                  |
|-------------------------------------|--------------------------------------------------------------|
| `Advanced_Excel_Transport_Report.pdf` | Full report: business context, modelling, results, visuals    |
| `Advanced_Excel_Transport_Model.xlsx` | Excel model: Solver setup, constraints, outputs, sensitivity |

---

## 🔍 Future Work

- Migrate to Python (e.g., `PuLP`, `Pyomo`) for larger datasets
- Add stochastic modelling for uncertain demand
- Automate scenario testing for faster planning

---

## 📈 Conclusion

This project shows how **advanced Excel techniques** can be applied to **real business challenges** in logistics. By transforming raw business data into optimization models, we helped Westvaco:

- Reduce shipping costs  
- Balance carrier usage  
- Improve operational efficiency  

This approach bridges theory and practice and provides a replicable solution for data-driven logistics management.



