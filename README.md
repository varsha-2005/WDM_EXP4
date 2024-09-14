### EX4 Implementation of Cluster and Visitor Segmentation for Navigation patterns
### DATE: 14-09-2024
### AIM: To implement Cluster and Visitor Segmentation for Navigation patterns in Python.
### Description:
<div align= "justify">Cluster visitor segmentation refers to the process of grouping or categorizing visitors to a website, 
  application, or physical location into distinct clusters or segments based on various characteristics or behaviors they exhibit. 
  This segmentation allows businesses or organizations to better understand their audience and tailor their strategies, marketing efforts, 
  or services to meet the specific needs and preferences of each cluster.</div>
  
### Procedure:
1) Read the CSV file: Use pd.read_csv to load the CSV file into a pandas DataFrame.
2) Define Age Groups by creating a dictionary containing age group conditions using Boolean conditions.
3) Segment Visitors by iterating through the dictionary and filter the visitors into respective age groups.
4) Visualize the result using matplotlib.

### Program:
```
Developed by: VARSHA G
Register No: 212222230166
```
```
# read the data
import pandas as pd
visitor_df = pd.read_csv('/content/clustervisitor.csv')

# Perform segmentation based on characteristics (e.g., age groups)
age_groups = {
    'Young': visitor_df['Age'] <= 30,
    'Middle-aged': (visitor_df['Age'] > 30) & (visitor_df['Age'] <= 50),
    'Elderly': visitor_df['Age'] > 50
}

for group, condition in age_groups.items():  
    visitors_in_group = visitor_df[condition] 
    print(f"Visitors in {group} age group:")
    print(visitors_in_group)

``` 
### Output:
![311408525-779111d3-af52-4000-bf59-db3e094b823b](https://github.com/RuchithaReddy28/WDM_EXP4/assets/93427261/1818757d-748c-45f7-8f65-bbec00f75a1c)

### Visualization:
```
# Create a list to store counts of visitors in each age group
visitor_counts=[]

# Count visitors in each age group
for group,condition in age_groups.items():
  visitors_in_group=visitor_df[condition]
  visitor_counts.append(len(visitors_in_group))
    
# Define age group labels and plot a bar chart
age_group_labels=list(age_groups.keys())
plt.figure(figsize=(8, 6))
plt.bar(age_group_labels, visitor_counts, color='skyblue')
plt.xlabel('Age Groups')
plt.ylabel('Number of Visitors')
plt.title('Visitor Distribution Across Age Groups')
plt.show()
```
### Output:
![311408655-ad59f235-0222-469a-9742-1c9fcdbf4dd1](https://github.com/RuchithaReddy28/WDM_EXP4/assets/93427261/57521279-289f-4d38-9a40-6eee1090ef48)

### Result:
Thus, the Implementation of Cluster and Visitor Segmentation for Navigation patterns is executed successfully.
