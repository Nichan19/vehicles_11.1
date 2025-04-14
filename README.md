## Vehicles_11.1  
# OVERVIEW  

In this application, we explore a dataset from Kaggle. The original dataset contained information on 3 million used cars. The provided dataset contains information on 426K cars to ensure speed of processing. My goal is to understand what factors make a car more or less expensive. As a result of the analysis, I will provide clear recommendations to client -- a used car dealership -- as to what consumers value in a used car. So, identify which features most influence used car prices, to help dealerships improve inventory and pricing strategies.   

Data Understanding  
After considering the business understanding, we want to get familiar with our data. Write down some steps that you would take to get to know the dataset and identify any quality issues within. Take time to get to know the dataset and explore what information it contains and how this could be used to inform your business understanding.  

Steps used in exploring the Data:  
Loading and inspecting the data by using pandas to load vehicles.csv, view head, dtypes, and basic statistics.  
Assessing completeness by checking missing values per column.  
Discovering distributions & outliers by plotting histograms for numeric features (e.g., price, mileage); identify extreme values.  
Configue categorical levels by listing unique brands, models, fuel types.  
Computing correlation matrix to see linear relationships with price if any.  
Date fields: if listing date is present, convert to datetime and extract age.  

Distributions Findings:  
Price is heavily right‑skewed, most listings under $50 k.  
Year clusters around recent model years (2010–2020), with a long tail to older vehicles.  
Odometer similarly skewed: most cars under 200 k miles.  

Evaluation  
With some modeling accomplished, we aim to reflect on what we identify as a high-quality model and what we are able to learn from this. We should review our business objective and explore how well we can provide meaningful insight into drivers of used car prices. Your goal now is to distill your findings and determine whether the earlier phases need revisitation and adjustment or if you have information of value to bring back to your client.  

Model Quality:  
Compare RMSE on log-price scale; back-transform for dollar error.  
Residual analysis: plot predicted vs. actual, histogram of residuals.  
Feature importance: for linear models, examine coefficients.  

Business Alignment:  
Do the drivers (age, mileage, brand premium) match dealership intuition?  
Are clusters meaningful segments (e.g., economy vs. luxury)?  

Deployment  
Now that we've settled on our models and findings, it is time to deliver the information to the client. You should organize your work as a basic report that details your primary findings. Keep in mind that your audience is a group of used car dealers interested in fine-tuning their inventory.  

Key Recommendations for Dealership Inventory:  
Focus on Newer, Low-Mileage Vehicles: Target cars no older than 5 years with under 60 000 miles. These consistently yield the highest margins.  
Prioritize Premium and Popular Brands: Allocate at least 30 % of stock to brands with proven price premiums (e.g., BMW, Mercedes, Toyota) to capture both luxury and reliable mid‑market demand.  
Maintain a Balanced Mix of Segments: Based on our clustering: 50 % economy (high-turnover, entry‑level), 30 % mid‑range (best seller models), and 20 % premium (higher-margin, lower-volume).  
Monitor Market Trends Monthly: Use simple time‑series dashboards to adjust acquisition and pricing by season, capitalizing on rising or falling price cycles.  
Leverage Data-Driven Pricing: Implement our Ridge regression model in your pricing tool to estimate optimal listing prices within a 10–15 % error margin, improving both competitiveness and profitability.  

