# First-Repo


---

### 📂 Data Loading and Preparation

#### Step 1: Import Libraries

```python
import pandas as pd
```

#### Step 2: Load the Dataset

```python
# Load index_1.csv into a DataFrame
df = pd.read_csv("index_1.csv")

# View the first few rows
print(df.head())
```

#### Step 3: Inspect the Data

```python
# Check basic info
print(df.info())

# Check summary statistics
print(df.describe())

# Check for missing values
print(df.isnull().sum())
```

#### Step 4: Basic Data Preparation

```python
# Drop duplicate rows if any
df = df.drop_duplicates()

# Handle missing values (example: fill with mean for numerical columns)
df = df.fillna(df.mean(numeric_only=True))

# Convert column names to lowercase for consistency
df.columns = df.columns.str.lower().str.replace(" ", "_")

# Example: convert date column (if exists) to datetime
# df['date'] = pd.to_datetime(df['date'])
```

#### Step 5: Save the Cleaned Data (Optional)

```python
# Save prepared data to a new file
df.to_csv("index_1_clean.csv", index=False)
```

---

