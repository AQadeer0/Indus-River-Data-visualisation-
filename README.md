# Indus-River-Data-visualisation-
Sindh 6 canals Data visualisation 

import matplotlib.pyplot as plt
import seaborn as sns

# Set the style for the plots
sns.set(style="whitegrid")

# 1. Plotting Operational Status
plt.figure(figsize=(8, 6))
status_count.plot(kind='bar', color=['skyblue', 'salmon'])
plt.title('Operational Status of Canals')
plt.xlabel('Status')
plt.ylabel('Count')
plt.xticks(rotation=0)
plt.tight_layout()
plt.show()

# 2. Plotting Construction Duration in Months
plt.figure(figsize=(10, 6))
sns.barplot(x=canal_df['Canal Name'], y=canal_df['Construction Duration (Months)'], palette='viridis')
plt.title('Construction Duration (in Months) for Each Canal')
plt.xlabel('Canal Name')
plt.ylabel('Construction Duration (Months)')
plt.xticks(rotation=45, ha='right')
plt.tight_layout()
plt.show()

# 3. Plotting Water Flow (Discharge)
plt.figure(figsize=(10, 6))
sns.barplot(x=canal_df['Canal Name'], y=canal_df['Water Flow (Discharge in cubic feet per second)'], palette='coolwarm')
plt.title('Water Flow (Discharge in Cubic Feet per Second) for Each Canal')
plt.xlabel('Canal Name')
plt.ylabel('Water Flow (Cubic Feet per Second)')
plt.xticks(rotation=45, ha='right')
plt.tight_layout()
plt.show()

# 4. Plotting Average Water Flow
plt.figure(figsize=(8, 6))
plt.barh(['Average Water Flow'], [avg_water_flow], color='mediumseagreen')
plt.title('Average Water Flow of Canals')
plt.xlabel('Cubic Feet per Second')
plt.tight_layout()
plt.show()

# 5. Plotting Average Construction Duration
plt.figure(figsize=(8, 6))
plt.barh(['Average Construction Duration'], [avg_construction_duration], color='steelblue')
plt.title('Average Construction Duration of Canals')
plt.xlabel('Months')
plt.tight_layout()
plt.show()
