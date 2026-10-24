# 📱 Telecom Device Selection Analysis

An Exploratory Data Analysis (EDA) and statistical filtering project built in Python. This project processes mobile phone specifications and filters candidate devices based on custom user requirements (screen size, resolution, camera quality, memory, battery life, and weight).

---

## 📋 Project Overview

The objective of this project is to analyze a dataset containing specifications of mobile phone models and systematically filter them using statistical thresholds (mean, median, and quartiles) to find the best-suited devices.

### Key Objectives:
1. **Data Inspection & Cleaning:** Load and explore telecom device attributes, shapes, missing values, and data types.
2. **Feature Engineering:**
   * Calculated **Total Screen Resolution** (`Px = Px_h * Px_w`).
   * Computed **Screen Diagonal Length** (`Scr_d = √(Scr_h² + Scr_w²)`).
3. **Statistical Filtering & Condition Matching:**
   * **`con1`:** Must have Bluetooth, Wi-Fi, Touch Screen, and External Memory.
   * **`con2`:** Screen Resolution (`Px`) $\ge$ Median.
   * **`con3`:** Screen Diagonal (`Scr_d`) $\ge$ Upper Quartile (75th percentile).
   * **`con4`:** Primary Camera (`PC`) & Front Camera (`FC`) $\ge$ Mean.
   * **`con5`:** Internal Memory (`Int_Mem`), Battery Power (`Bty_Pwr`), & RAM $\ge$ Mean.
   * **`con6`:** Device Depth (`Depth`) & Weight (`Weight`) $\le$ Median (Light & Slim).
4. **Subsetting & Recommendation:** Combined all logical conditions to output candidate models sorted by price in ascending order.
5. **Variability Analysis:** Calculated the Coefficient of Variation ($\sigma / \mu$) across numerical features to evaluate variance across models.

---

## 🛠️ Tech Stack & Libraries Used

* **Language:** Python 3.11
* **Environment:** VS Code / Jupyter Notebook
* **Data Manipulation:** `pandas`, `numpy`
* **Data Visualization:** `matplotlib`, `seaborn`

---

## 📂 Repository Structure

```text
├── Telecom Dataset.csv         # Dataset containing phone specs
├── telecome_dataset.ipynb      # Main Jupyter notebook with code & visualizations
└── README.md                   # Project documentation
