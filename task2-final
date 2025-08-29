# Task 2: Static Data Processing (Pre-Generated Dataset)

# Step 1: Store dataset as a list of dictionaries
dataset = [
    {"Farmer": "Ali", "Crop": "Wheat", "Acres": 5, "Yield": 12, "Region": "North"},
    {"Farmer": "Sana", "Crop": "Rice", "Acres": 8, "Yield": 18, "Region": "South"},
    {"Farmer": "Imran", "Crop": "Corn", "Acres": 4, "Yield": 9, "Region": "East"},
    {"Farmer": "Ayesha", "Crop": "Wheat", "Acres": 6, "Yield": 14, "Region": "West"}
]

# Step 2a: Print all farmers growing Wheat
print("Farmers growing Wheat:")
for record in dataset:
    if record["Crop"] == "Wheat":
        print("-", record["Farmer"])

# Step 2b: Calculate total yield across all farmers
total_yield = 0
for record in dataset:
    total_yield += record["Yield"]

print("\nTotal Yield (tons) across all farmers:", total_yield)

# Step 2c: Find farmer with maximum yield
max_record = dataset[0]  # assume first record is max initially
for record in dataset:
    if record["Yield"] > max_record["Yield"]:
        max_record = record

print("\nFarmer with Maximum Yield:")
print("Name:", max_record["Farmer"])
print("Crop:", max_record["Crop"])
print("Yield:", max_record["Yield"], "tons")
