# Task 5: Data Visualization (Graphs & Tables)

import matplotlib.pyplot as plt
import pandas as pd

# Dataset
dataset = [
    {"Farmer": "Ali", "Crop": "Wheat", "Acres": 5, "Yield": 12, "Region": "North"},
    {"Farmer": "Sana", "Crop": "Rice", "Acres": 8, "Yield": 18, "Region": "South"},
    {"Farmer": "Imran", "Crop": "Corn", "Acres": 4, "Yield": 9, "Region": "East"},
    {"Farmer": "Ayesha", "Crop": "Wheat", "Acres": 6, "Yield": 14, "Region": "West"}
]

# Convert dataset to Pandas DataFrame (for easy table + analysis)
df = pd.DataFrame(dataset)

# --- 1. Bar Chart: Average yield per crop ---
avg_yield_per_crop = df.groupby("Crop")["Yield"].mean()
avg_yield_per_crop.plot(kind="bar", color="skyblue", edgecolor="black")
plt.title("Average Yield per Crop")
plt.ylabel("Yield (tons)")
plt.xlabel("Crop")
plt.show()

# --- 2. Pie Chart: Percentage of farmers by region ---
region_counts = df["Region"].value_counts()
region_counts.plot(kind="pie", autopct="%1.1f%%", startangle=90, colors=["#ff9999","#66b3ff","#99ff99","#ffcc99"])
plt.title("Farmers by Region")
plt.ylabel("")  # remove default y-label
plt.show()

# --- 3. Scatter Plot: Acres vs Yield ---
plt.scatter(df["Acres"], df["Yield"], color="green", s=100, edgecolors="black")
plt.title("Acres vs Yield")
plt.xlabel("Acres")
plt.ylabel("Yield (tons)")
plt.grid(True, linestyle="--", alpha=0.7)
plt.show()

# --- 4. Show Table (Pandas DataFrame) ---
print("=== Farmers Dataset ===")
print(df)
