1. Overview:
This project is focused on building a machine learning model to predict laptop prices based on various features such as company, RAM, weight, processor, GPU, etc. We performed data cleaning, exploratory data analysis (EDA), and built multiple machine learning models for regression, including linear models, tree-based models, and ensemble techniques.

2. Dataset:
The dataset consists of laptop specifications and their corresponding prices. It includes features like Company, TypeName, Ram, Weight, ScreenResolution, Cpu, Gpu, OpSys, Price, and more.

3. Steps:
3.1 Data Cleaning:
Removing unnecessary columns: We dropped columns like 'Unnamed: 0', which were irrelevant.
Cleaning text columns: We cleaned text-based columns like Ram (removing 'GB') and Weight (removing 'kg') and converted them to numeric types for analysis.
Handling Screen Resolution: Extracted x_res and y_res from the ScreenResolution column to calculate the ppi (pixels per inch), which can influence price.
Categorical transformations: Converted categorical columns into meaningful categories:
Extracted processor from the Cpu column, grouped into 'Intel', 'AMD', and 'Other Intel'.
Grouped the OpSys column into 'Windows', 'Mac', and 'Other' based on operating system types.
3.2 Exploratory Data Analysis (EDA):
Distribution of Price: The price distribution was skewed, which was visualized using a histogram.
Variation of Price by Company: We plotted a bar chart to observe how prices vary across different laptop manufacturers.
Touchscreen & IPS Analysis: We identified whether the laptop has a touchscreen or an IPS display and studied their effects on price.
Correlation of RAM and Price: We explored how the amount of RAM impacts the laptop price through a bar plot.
3.3 Feature Engineering:
Screen Resolution Features: Extracted x_res, y_res, and calculated the pixel density ppi for each laptop.
Processor Categorization: Grouped different processors into meaningful categories (Intel Core, AMD, Other Intel).
Memory Categorization: Created a new feature Memory_type to categorize laptops into SSD, HDD, and hybrid memory systems.
GPU Feature: Simplified GPU names by extracting the first word, which usually represents the manufacturer (Nvidia, Intel, AMD).
3.4 Model Building:
We experimented with multiple machine learning models:
Linear Regression
Ridge Regression
Lasso Regression
K-Nearest Neighbors (KNN)
Decision Tree Regressor
Random Forest Regressor
Extra Trees Regressor
Each model was built using a Pipeline, with OneHotEncoder used for encoding categorical variables and the model-specific regressor as the final step.

3.5 Performance Evaluation:
The models were evaluated using the R^2 score, which measures how well the predicted values match the actual values.
We trained the models on 80% of the data and tested them on 20%.
