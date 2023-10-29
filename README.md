![Notebook](https://github.com/nogibjj/IDS706-Mini-Project-9-sp699/actions/workflows/CI.yml/badge.svg)
# IDS-706-Data-Engineering :computer:

## Mini Project 9 :page_facing_up: 

## :ballot_box_with_check: Requirements
* Set up a cloud-hosted Jupyter Notebook (e.g., Google Colab)</br>
* Perform data manipulation tasks on a sample dataset</br>

## :ballot_box_with_check: To-do List
* __Learn how to work with Rust__: To learn the concept of cloud-hosted notebooks and their application in data management.</br>

## :ballot_box_with_check: Dataset
`titanics.csv`
  - This dataset contains a list of passengers aboard the Titanic in 1912, including information on those who survived and those who did not. There are 891 samples with 14 different variables. In this repository, we will visualize the age of passengers in different classes using box plots.</br>
  - [titanics.csv](https://github.com/suim-park/Mini-Project-9/raw/main/titanic.csv)

## :ballot_box_with_check: Main Progress
#### Perform the data manipulation using a cloud-hosted notebook.
##### Cloud-Hosted Notebook Data Manipulation
`Step 1` __Import Libararies__ 
```Python
import os
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
import warnings
```

```Python
warnings.filterwarnings("ignore")
```

`Step 2` __Load the Data__
```Python
# Load the data
df = pd.read_csv("titanic.csv")
```

```Python
df.head()
```

`Step 3` __Data Summary__
```Python
# Summarize the data
summary = df.describe()
print(summary)
```

```Python
# Check the missing values
missing_values = df.isnull().sum()
print(missing_values)
```

`Step 4` __Visualize the Data__
```Python
# Create the boxplot
sns.boxplot(data=df, x="class", y="age", hue="alive", order=["First", "Second", "Third"])
```
![image](https://github.com/nogibjj/IDS706-Mini-Project-9-sp699/assets/143478016/6d1ea501-b814-4b6d-adfd-6401c20f14b3)


`Step 5` __Conclusion__
```
Based on the data summary and box plots, we observe that the first-class passengers who survived are the oldest in their class group. Conversely, those who did not survive in the first class are also among the oldest passengers. Notably, there are numerous outliers among the passengers in third class who didn't survive. Furthermore, there is a trend of decreasing age from first class to third class, with passengers in first class being older and those in third class being younger.
```

* Link
: The link provided is to a notebook that performs data manipulation.
[Google Colab](https://colab.research.google.com/drive/195osUytOXqXQv8XU6hvsPhv9KCw1FoL5?usp=sharing)
