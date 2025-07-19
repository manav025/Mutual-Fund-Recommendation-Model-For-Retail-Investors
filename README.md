Mutual Fund Recommendation Model
This project provides a Python-based model for recommending mutual funds based on user-defined risk tolerance. The model processes mutual fund NAV (Net Asset Value) data, calculates risk profiles for each fund, and suggests top-performing funds for low, medium, and high-risk categories. Additionally, it computes and visualizes Key Performance Indicators (KPIs) to offer a comprehensive analysis of the mutual fund landscape.

📋 Key Features
Data-driven Recommendations: Utilizes the latest mutual fund NAV data to provide timely and relevant fund suggestions.

Dynamic Risk Profiling: Calculates a unique risk score for each fund by combining a base risk score with the fund's NAV volatility.

Customizable Recommendations: Allows users to specify their risk tolerance (Low, Medium, or High), plan type (Direct or Regular), and investment option (Growth).

Comprehensive Analysis: Generates and visualizes key performance indicators (KPIs), including risk distribution by category, NAV statistics, and plan type distribution.

Easy to Use: The model is structured into clear, modular functions, making it easy to understand, use, and extend.

⚙️ Methodology
The model follows a systematic approach to generate recommendations:

Data Loading and Preprocessing:

Loads the mutual fund NAV data from an Excel file.

Filters the data to retain only the latest NAV records.

Categorizes funds (e.g., Liquid, Overnight, Gilt) and plan types (Direct, Regular) based on their scheme names.

Risk Profiling:

Assigns a base risk score to each fund category.

Calculates the NAV volatility (Coefficient of Variation) for each category.

Computes a final risk score for each fund by adjusting the base risk with the NAV volatility.

Fund Recommendation:

Defines dynamic risk ranges (Low, Medium, High) based on the quartile distribution of risk scores.

Filters funds based on the user's risk tolerance, plan type, and investment option.

Ranks the filtered funds using a quality score, calculated as Net Asset Value / (Risk + 1).

Returns the top 5 funds for the selected risk profile.

KPI Calculation and Visualization:

Risk Profile by Category: Computes the average risk and risk volatility for each fund category.

NAV Statistics: Calculates the mean, median, standard deviation, and range of NAV for each category.

Risk-NAV Correlation: Determines the correlation between fund risk and NAV.

Distributions: Analyzes the distribution of funds across different risk levels and plan types.

The calculated KPIs are then visualized using bar charts, box plots, and pie charts for intuitive analysis.

🚀 Installation and Usage
To run the model, you need to have Python and the following libraries installed:

pandas

numpy

matplotlib

seaborn

You can install the required libraries using pip:

Bash

pip install pandas numpy matplotlib seaborn
Running the Model:

Place your data file (mutual_fund_nav.xlsx) in the specified path within the script.

Execute the script. The model will perform the analysis and print the KPIs and fund recommendations to the console.

📊 Output
The model generates the following outputs:

Risk Distribution Summary: A statistical overview of the calculated risk scores.

Key Performance Indicators:

Risk Profile by Category

NAV Statistics by Category

Risk-NAV Correlation Matrix

Risk Level Distribution

Plan Type Distribution

Visualizations: A series of plots to help you understand the fund landscape visually.

Fund Recommendations: Top 5 recommended funds for Low, Medium, and High-risk appetites.
