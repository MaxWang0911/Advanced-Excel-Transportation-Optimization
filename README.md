# Advanced Excel: Transportation Optimization for Westvaco Logistics

This project applies advanced Excel techniques to optimize transportation costs and carrier allocation for a major U.S. paper product manufacturer, Westvaco. Using real operational constraints, three linear programming models are built to minimize costs, balance fairness, and reduce carrier dependency.

## 🚚 Business Context

- Company: Westvaco (paper products)
- Facilities: 5 paper mills and 4 chemical plants
- Problem: Transport goods from Wickliffe mill to 6 destinations via 6 carriers
- Objective: Minimize total cost while satisfying demand and respecting constraints

## 📊 Modeling Techniques

- Integer Linear Programming using Excel Solver (Simplex LP)
- Preprocessing of unavailable routes with penalty costs
- Multiple scenario modeling:
  - **Model 1**: Cost minimization only
  - **Model 2**: Fair allocation (daily and weekly commitments)
  - **Model 3**: Carrier reduction with minimal cost impact
- Sensitivity analysis on commitment strategies
- Data-driven visualization of cost changes (Figure 8–10)

## 💡 Key Outcomes

- Minimum achievable transportation cost: **$93,774.16**
- Weekly commitments are more cost-effective than daily ones
- Reducing carrier usage can lower complexity with minimal cost increase
- Excel becomes slow at scale—suggesting the future need for more robust optimization tools

## 📂 Files

- `Advanced_Excel_Transport_Report.pdf`: Full analysis of the optimization models
- `Advanced_Excel_Transport_Model.xlsx`: Model data, Solver setups, result testing, visual analysis

## 👨‍💻 Author

Zheng Wang  
Bachelor of Science in Analytics, University of Technology Sydney (UTS)  
Student ID: 14403000
