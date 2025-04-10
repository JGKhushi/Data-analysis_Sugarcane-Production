# 🌾 Sugarcane Production Data Analysis Project

This project explores global **sugarcane production** by analyzing key metrics like production volume, land usage, and yield efficiency across different countries and continents. Through **comprehensive Exploratory Data Analysis (EDA)**, we derive insights that can support agricultural strategies and optimize resource management in the sugarcane industry.

---

## 📌 Objectives
- Clean and preprocess sugarcane production data.
- Perform univariate and bivariate analysis.
- Visualize relationships between land usage, yield, and production.
- Understand continental trends and identify top producers.
- Draw actionable insights from the data.

---

## 🧹 Data Cleaning

### ✅ Remove Unwanted Characters
- Removed **periods (.)** from `Production (Tons)` and `Acreage (Hectare)`.
- Replaced **commas (,)** with **periods (.)** in `Production per Person (Kg)` to fix decimal formatting.

### ✅ Drop Unnecessary Columns
- Dropped `"Unnamed: 0"` using `df.drop("Unnamed: 0", axis=1)`.

### ✅ Rename Columns for Consistency
| Old Column Name              | New Column Name            |
|-----------------------------|----------------------------|
| Production (Tons)           | Production(Tons)           |
| Production per Person (Kg)  | Production_per_person(Kg)  |
| Acreage (Hectare)           | Acreage(Hectare)           |
| Yield (Kg/Hectare)          | Yield(Kg/Hectare)          |

---

## 🧩 Handling Missing Values
| Column             | Missing Values |
|--------------------|----------------|
| Acreage(Hectare)   | 1              |
| Yield(Kg/Hectare)  | 1              |

- Rows with missing values were **dropped**.
- Index was reset for a clean DataFrame.

---

## 🔁 Data Type Conversion
All numerical columns were converted to `float` type for smooth computation:
- `Production(Tons)`
- `Production_per_person(Kg)`
- `Acreage(Hectare)`
- `Yield(Kg/Hectare)`

---

## 📊 Univariate Analysis

### 🌍 Countries Producing Sugarcane by Continent
| Continent       | Countries |
|----------------|-----------|
| Africa         | 38        |
| Asia           | 25        |
| North America  | 22        |
| South America  | 11        |
| Oceania        | 4         |
| Europe         | 2         |

> Visualized using a bar chart to understand global participation.

### 📈 Distribution of Key Variables
Used **histograms (`sns.distplot()`)** to visualize:
- `Production(Tons)` — Skewed due to Brazil, India, China.
- `Production_per_person(Kg)` — Skewed.
- `Acreage(Hectare)` — Less skewed.
- `Yield(Kg/Hectare)` — Varies significantly by country.

### 📦 Outlier Detection: Boxplots
- Countries like **Brazil, India, China** are outliers in `Production(Tons)`.
- High efficiency countries stand out in `Yield(Kg/Hectare)`.

### 🎻 Violin Plot
Used to show distribution + outliers for `Production(Tons)`.

---

## 🔁 Bivariate Analysis

### 🌱 Top 15 Countries by Acreage
- Bar chart shows **Brazil, India, China** use the most land.

### 🧪 Top Yielding Country
- **Guatemala** has the highest yield per hectare → efficient farming.

### 🧍‍♂️ Highest Production per Person
- **Paraguay** leads in per-person production efficiency.

### 🔗 Correlation Analysis
| Variables                            | Correlation |
|-------------------------------------|-------------|
| Production(Tons) vs Acreage(Hectare) | **0.997** (Strong) |
| Production(Tons) vs Yield(Kg/Hectare) | 0.132 (Weak) |

> Visualized using a **heatmap**.

### 📈 Scatter Plots
- **Acreage vs Production**: Larger land = more production.
- **Yield vs Production**: High yield ≠ always high total production.

---

## 🌍 Continental Trends

### 🚜 Total Sugarcane Production by Continent
| Continent       | Insights                        |
|----------------|----------------------------------|
| South America  | Highest production (mainly Brazil) |
| Asia           | Second largest producer           |
| Africa         | Third in line                     |

> Visualized via bar plot.

### 🔢 Does Country Count Matter?
Even continents with **fewer countries** can lead in production due to **dominant producers** like Brazil in South America.

---

## ✅ Conclusion

This project provided deep insights into **global sugarcane production trends**, highlighting:
- The impact of land usage on production.
- Countries with the highest efficiency and scale.
- Disparities between yield and total output.
- Continental patterns and their key players.

By understanding these dynamics, stakeholders can develop **smarter farming strategies, optimize resources**, and focus on **high-yield sustainable practices**.

---

## 📁 Tech Stack
- **Python**, **Pandas**, **NumPy**
- **Matplotlib**, **Seaborn** for data visualization
- **Jupyter Notebook** for EDA and reporting

---

