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
- **Core Metric Formula:**
  $$\text{Personal Living-Space Proxy (sq ft/person)} = \frac{\text{Annual Median Home Size (sq ft)}}{\text{Average Household Size (persons)}}$$
- **Analytical Methods:**
  - Data cleaning and time-series transformation (aggregating quarterly housing observations into annual means).
  - Pearson correlation analysis (in levels and annual percentage changes).
  - Segmented linear regression (Pre- and Post-2015 trend break analysis).
  - Sequential change decomposition.
## 4. Key Findings and One Limitation
- **Key Findings:** 
 1. **Long-Term Growth:** The personal living-space proxy rose from **658.8 sq ft/person** in 1987 to **857.9 sq ft/person** in 2025, representing a net **+30.2%** increase.
  2. **Structural Turning Point:** Per-person living space reached a historical peak in **2015 at 973.6 sq ft/person**, followed by an **11.9% contraction** from 2015 to 2025.
  3. **Drivers of Change:** Long-term growth was primarily driven by larger new homes and shrinking household sizes, whereas the post-2015 decline was overwhelmingly driven by a reduction in new-home floor area.
- **Limitation:** The metric is a constructed macro-proxy (dividing median home size by average household size) rather than directly observed occupied space, and regression results describe historical patterns without establishing direct causality.

## 5. Instructions for Running the Analysis
1. **Environment Setup:**
   Ensure Python 3 and the required data science packages are installed:
   ```bash
   pip install pandas numpy matplotlib seaborn scipy
