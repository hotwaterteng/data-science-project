# data-science-project
# Peak House, Shrinking Household: Are Americans Actually Gaining or Losing Personal Living Space? (1987–2025)

## 1. The Problem or Research Question
The project investigates a common claim: *Are American homes being built smaller, forcing people into more crowded conditions?* Instead of accepting this at face value, this project combines national housing construction data with household-size data over a 38-year timeline (1987–2025) by constructing a personal living-space proxy to test the claim.

## 2. Dataset Source and Usage Permissions
- **FRED Dataset:** Federal Reserve Bank of St. Louis, series COMPSFLAM1FQ (New Privately Owned Housing Completions, Median Square Feet for One-Family Units).[Source Link](https://fred.stlouisfed.org/series/COMPSFLAM1FQ)
- **Census Dataset:** U.S. Census Bureau, Table HH-6 (Average Population Per Household and Family). [Source Link](https://www.census.gov/data/tables/time-series/demo/families/households.html)
- **Usage Permissions:** Open public data from U.S. government statistical agencies, permitted for academic and portfolio demonstration use under fair use guidelines. No restricted or confidential personal data is involved.

## 3. Methods and Tools Used
- **Programming Language:** Python 3
- **Libraries:** Pandas, NumPy, Matplotlib, Seaborn
- **Methods:** 
  - Data cleaning, validation, and multi-frequency dataset integration (aggregating quarterly housing observations to annual means).
  - Derived metric calculation (personal living-space proxy: home square feet divided by household size, indexed trends, annual percentage changes).
  - Time-series visualization, correlation analysis, and sequential change decomposition.

## 4. Key Findings and One Limitation
- **Key Findings:** 
  - The personal living-space proxy rose from 659 sq ft per person in 1987 to a peak of 974 in 2015, before settling at 858 in 2025 (a net 30.2% increase over 1987).
  - Long-term growth was primarily driven by larger homes (+147.5 sq ft effect) and smaller households (+51.6 sq ft effect). Conversely, the post-2015 contraction was driven chiefly by shrinking home sizes (-129.2 sq ft effect).
- **Limitation:** The metric is a constructed macro-proxy (dividing median home size by average household size) rather than directly observed occupied space, and regression results describe historical patterns without establishing direct causality.

## 5. Instructions for Running the Analysis
1. Clone this repository:
   ```bash
   git clone [https://github.com/hotwatertemp/data-science-project.git](https://github.com/hotwatertemp/data-science-project.git)
