# Distribution Analysis Using Python & Pandas

## 📌 Project Overview

This project focuses on analyzing the distribution of employee ages using Python, Pandas, NumPy, and Matplotlib.

The main objective is to understand how numerical data is distributed using histograms and statistical measures such as mean, median, mode, standard deviation, and skewness.

This project was completed as **Task 27** of the Veda Technology AI & ML Internship.

## 🎯 Project Objectives

- Load and explore the Employee dataset.
- Select a numerical variable for distribution analysis.
- Create histograms to visualize employee age distribution.
- Experiment with different histogram bin sizes.
- Calculate statistical measures.
- Identify the distribution pattern using skewness.
- Compare mean and median values visually.
- Draw observations from the histogram.

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Google Colab
- Jupyter Notebook

## 📂 Dataset Information

**Dataset Name:** Employee.csv

**Selected Column:** Age

The Employee dataset contains information about employees, including education, joining year, city, payment tier, age, gender, and work experience.

The `Age` column is selected for understanding the distribution of employee ages.

## ⚙️ Project Workflow

### 1. Import Libraries

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
```

### 2. Load Dataset

```python
df = pd.read_csv('/content/Employee.csv')

display(df.head())
```

### 3. Explore Dataset

```python
df.info()
display(df.describe())
```

### 4. Select Numerical Column

```python
age = df['Age'].dropna()

print("Total Records:", len(age))
print("Minimum Age:", age.min())
print("Maximum Age:", age.max())
```

### 5. Create Histogram

```python
plt.figure(figsize=(10, 6))

plt.hist(age, bins=10, edgecolor='black')

plt.title('Distribution of Employee Age')
plt.xlabel('Age')
plt.ylabel('Frequency')

plt.show()
```

### 6. Experiment with Different Bin Sizes

```python
plt.figure(figsize=(12, 5))

plt.hist(age, bins=15, edgecolor='black')

plt.title('Employee Age Distribution (15 Bins)')
plt.xlabel('Age')
plt.ylabel('Frequency')

plt.show()
```

### 7. Calculate Statistical Measures

```python
print("Mean Age:", age.mean())
print("Median Age:", age.median())
print("Mode Age:", age.mode().tolist())
print("Standard Deviation:", age.std())
print("Skewness:", age.skew())
```

### 8. Analyze Skewness

```python
skewness = age.skew()

if skewness > 0.5:
    print("Distribution is Positively Skewed")

elif skewness < -0.5:
    print("Distribution is Negatively Skewed")

else:
    print("Distribution is Approximately Symmetrical")
```

### 9. Compare Mean and Median

```python
plt.figure(figsize=(10, 6))

plt.hist(age, bins=10, edgecolor='black')

plt.axvline(age.mean(), linestyle='--', label='Mean Age')
plt.axvline(age.median(), linestyle=':', label='Median Age')

plt.title('Employee Age Distribution with Mean and Median')
plt.xlabel('Age')
plt.ylabel('Frequency')

plt.legend()
plt.show()
```

## 📊 Visualizations

The project includes:

1. **Employee Age Histogram:** Shows the frequency distribution of employee ages using 10 bins.
2. **Histogram with 15 Bins:** Provides a more detailed view of the age distribution.
3. **Mean and Median Histogram:** Displays the mean and median age using vertical reference lines.

## 💡 Key Observations

1. The histogram shows the frequency distribution of employee ages.
2. Mean and median help understand the central tendency of employee ages.
3. Skewness indicates whether the age distribution is symmetrical or skewed.

## 📚 Key Learnings

- Understanding numerical data distribution.
- Creating histograms using Matplotlib.
- Experimenting with histogram bin sizes.
- Calculating mean, median, and mode.
- Understanding standard deviation.
- Identifying positive and negative skewness.
- Interpreting statistical visualizations.

## 📁 Project Structure

```text
Distribution-Analysis/
│
├── Employee.csv
├── Distribution_Analysis.ipynb
└── README.md
```

## 🚀 How to Run the Project

1. Clone the repository:

```bash
git clone https://github.com/satya77713/Distribution-Analysis.git
```

2. Navigate to the project folder:

```bash
cd Distribution-Analysis
```

3. Install the required libraries:

```bash
pip install pandas numpy matplotlib
```

4. Open the notebook:

```bash
jupyter notebook Distribution_Analysis.ipynb
```

5. Make sure `Employee.csv` is available in the working directory. If using Google Colab, upload the dataset to `/content/Employee.csv`.
6. Run all notebook cells.

## 🎓 Internship Details

- **Organization:** Veda Technology
- **Program:** AI & ML Internship
- **Task Number:** 27
- **Project:** Distribution Analysis

## 👨‍💻 Author

**Satya**

GitHub: [@satya77713](https://github.com/satya77713)

## 📝 Conclusion

This project provided practical experience in understanding numerical data distributions using Python and Matplotlib. By creating histograms and calculating statistical measures, I learned how to analyze data concentration, spread, central tendency, and skewness.

These techniques are useful for exploratory data analysis and preparing datasets for machine learning.

---

⭐ If you find this project useful, feel free to star the repository!
