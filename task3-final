# Task 3: Data Analysis (Beginner Level)

# Sample dataset (same as before, but we’ll also add one faulty record to test exception handling)
dataset = [
    {"Farmer": "Ali", "Crop": "Wheat", "Acres": 5, "Yield": 12, "Region": "North"},
    {"Farmer": "Sana", "Crop": "Rice", "Acres": 8, "Yield": 18, "Region": "South"},
    {"Farmer": "Imran", "Crop": "Corn", "Acres": 4, "Yield": 9, "Region": "East"},
    {"Farmer": "Ayesha", "Crop": "Wheat", "Acres": 6, "Yield": 14, "Region": "West"},
    {"Farmer": "Test", "Crop": "Wheat", "Acres": 7, "Region": "North"}  # missing Yield!
]

# Function 1: Calculate average yield per crop
def average_yield_per_crop(data):
    crop_totals = {}
    crop_counts = {}

    for record in data:
        try:
            crop = record["Crop"]
            yield_value = record["Yield"]   # may throw KeyError if missing
            crop_totals[crop] = crop_totals.get(crop, 0) + yield_value
            crop_counts[crop] = crop_counts.get(crop, 0) + 1
        except KeyError:
            print(f"⚠️ Skipping record for {record.get('Farmer', 'Unknown')} (missing yield).")

    # Calculate averages
    averages = {}
    for crop in crop_totals:
        averages[crop] = crop_totals[crop] / crop_counts[crop]

    return averages


# Function 2: Count farmers in each region
def count_farmers_per_region(data):
    region_counts = {}
    for record in data:
        try:
            region = record["Region"]
            region_counts[region] = region_counts.get(region, 0) + 1
        except KeyError:
            print(f"⚠️ Skipping record (missing region).")
    return region_counts


# --- Main Program Execution ---
print("=== Analysis Results ===")

# Average yield per crop
avg_yields = average_yield_per_crop(dataset)
print("\nAverage Yield per Crop:")
for crop, avg in avg_yields.items():
    print(f"{crop}: {avg:.2f} tons")

# Farmer count per region
region_counts = count_farmers_per_region(dataset)
print("\nNumber of Farmers per Region:")
for region, count in region_counts.items():
    print(f"{region}: {count} farmers")
