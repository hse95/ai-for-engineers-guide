#################################
LLM to Write Code Hands-on
#################################


### Buggy code to paste:

```python
import pandas as pd
import numpy as np
from sklearn.linear_model import LinearRegression
import matplotlib.pyplot as plt

# Load data
df = pd.read_csv("steel_stress_strain.csv")

# Prepare features and target
X = df[["Strain"]].values          
y = df["Stress (MPa)"].values

# Fit linear regression
model = LinearRegression()
model.fit(X, y)

# Results
slope = model.coef_[0]
intercept = model.intercept_
r_squared = model.score(X, y)

print(f"Slope (Modulus of Elasticity): {slope:.2f} MPa per % strain")
print(f"Intercept: {intercept:.2f} MPa")
print(f"R² Score: {r_squared:.4f}")

# Plot
plt.figure(figsize=(8, 5))
plt.scatter(df["Strain"], y, color="steelblue", label="Data")
plt.plot(df["Strain"], model.predict(X), color="red", linewidth=2, label="Best fit")
plt.xlabel("Strain (%)")
plt.ylabel("Stress (MPa)")
plt.title("Steel Stress–Strain: Linear Regression")
plt.legend()
plt.tight_layout()
plt.show()
```

### Prompt to use:

```
I'm trying to run this Python script to perform linear regression on my steel stress-strain data, but I'm getting a KeyError. Here's the CSV header:

Strain (%),Stress (MPa)

And here's my code:

[paste the buggy code above]

Can you find and fix the bug?
```



#################################
Agentic Coding Hands-on
#################################


### Prompt to give the agent:

```
I have a CSV file called "cantilever_data.csv" with columns: P_N (load in Newtons), L_m (length in meters), and delta_m (deflection in meters).

Please do the following:
1. Load and explore the data (print shape, summary statistics, check for missing values)
2. Split the data into 80% train and 20% test sets (random_state=42)
3. Normalize/standardize the features appropriately
4. Build a simple feedforward neural network (FNN) in PyTorch to predict delta_m from P_N and L_m
   - Use 2–3 hidden layers with ReLU activations
   - Use MSE loss and Adam optimizer
   - Train for enough epochs to converge, and print the loss every 50 epochs
5. Evaluate on the test set: print MSE and R² score
6. Generate the following figures and save them:
   - Training loss curve (loss vs. epoch)
   - Predicted vs. Actual deflection scatter plot (test set) with a 45-degree reference line
   - Residuals plot (residual vs. predicted value)

Use clear axis labels with units on all plots.
```