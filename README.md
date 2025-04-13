# 🏀 NBA Seasons Data Analysis with Pandas (Jupyter Notebook + VS Code)

This repository contains an exploratory data analysis (EDA) project focused on **NBA player statistics across multiple seasons**, using **Pandas** in a **Jupyter Notebook environment** inside **VS Code**, powered by **Python 3.13.1**.

The notebook demonstrates how to read, clean, analyze, and manipulate NBA data using real-world techniques that can be applied to any structured dataset.

---

## 📌 Project Overview

This project walks through several foundational Pandas operations, including:
- Viewing and navigating data columns and rows
- Filtering player stats by name or condition
- Creating new columns based on performance metrics
- Dropping and reordering columns for cleaner formatting
- Iterating through datasets to extract specific values

Great for beginners or anyone looking to brush up on their Pandas skills using NBA data.

---

## ⚙️ Tools & Technologies

- **Python 3.13.1**
- **Pandas**
- **Jupyter Notebook** (via **VS Code**)

---

## 🗂️ Key Features & Examples

### 📖 Reading Data

```python
# View column headers
print(df.columns)

# Preview specific columns
print(df['player_name'][0:5])
print(df[['player_name', 'season', 'team_abbreviation']][0:5])

🔍 Accessing Rows
python
Copy
Edit
# Access a specific row
print(df.iloc[1])

# Access multiple rows
print(df.iloc[1:5])

# Iterate through rows and print player names
for index, row in df.iterrows():
    print(index, row['player_name'])
🎯 Filtering Player Data
python
Copy
Edit
# Find all rows for Stephen Curry
df.loc[df['player_name'] == 'Stephen Curry']
🧮 Creating and Editing Stats Columns
python
Copy
Edit
# Add a combined stat column
df['Combined Stats'] = df['pts'] + df['reb'] + df['ast']

# Drop a redundant column
df = df.drop(columns=['Total Stats'])

# Combine weight and height columns
df['Combined Weight & Height'] = df.iloc[:, 4:6].sum(axis=1)
🧾 Reordering Columns
python
Copy
Edit
# Move the last column to a specific location
cols = list(df.columns.values)
df = df[cols[0:6] + [cols[-1]] + cols[6:22]]

🚀 Getting Started
Clone the repository

bash
Copy
Edit
git clone https://github.com/your-username/your-repo-name.git
Install dependencies

bash
Copy
Edit
pip install pandas jupyter
Open the notebook in VS Code or Jupyter Lab/Notebook

bash
Copy
Edit
jupyter notebook
📌 Dataset Notes
The dataset contains player-level statistics by season.

Includes points, rebounds, assists, team info, physical attributes, and more.

Ideal for sports analytics projects or data visualization exercises.

📃 License
This project is licensed under the MIT License.

🙌 Contributing
Feel free to fork the repo, suggest features, or submit pull requests if you'd like to contribute!

vbnet
Copy
Edit

Let me know if you'd like to include a preview image of the notebook or instructions for uploading a CSV/Excel file.
