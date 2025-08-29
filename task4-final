# Task 4: Statistical Analysis

import statistics
import numpy as np   # optional but great for correlation & std

# Dataset (from Task 2, removing faulty record for clean stats)
dataset = [
    {"Farmer": "Ali", "Crop": "Wheat", "Acres": 5, "Yield": 12, "Region": "North"},
    {"Farmer": "Sana", "Crop": "Rice", "Acres": 8, "Yield": 18, "Region": "South"},
    {"Farmer": "Imran", "Crop": "Corn", "Acres": 4, "Yield": 9, "Region": "East"},
    {"Farmer": "Ayesha", "Crop": "Wheat", "Acres": 6, "Yield": 14, "Region": "West"}
]

# Extract yield and acres data
yields = [record["Yield"] for record in dataset]
acres = [record["Acres"] for record in dataset]

# --- Statistical Measures ---
mean_yield = statistics.mean(yields)
median_yield = statistics.median(yields)
mode_yield = statistics.mode(yields)   # if no repeated value, may raise StatisticsError
stdev_yield = statistics.stdev(yields)

# --- Correlation between Acres and Yield ---
correlation = np.corrcoef(acres, yields)[0, 1]

# --- Output ---
print("=== Statistical Analysis of Yields ===")
print(f"Mean Yield = {mean_yield:.2f} tons")
print(f"Median Yield = {median_yield:.2f} tons")

try:
    print(f"Mode Yield = {mode_yield} tons")
except statistics.StatisticsError:
    print("Mode Yield = No unique mode (all values different)")

print(f"Standard Deviation = {stdev_yield:.2f}")
print(f"Correlation (Acres vs Yield) = {correlation:.2f}")
