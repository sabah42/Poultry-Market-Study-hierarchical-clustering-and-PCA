# Poultry Market Study: hierarchical clustering and PCA

## Table of Contents

 - [Project Description ](#project-description).
 - [Project Structure ](#project-structure)
 - [Dataset](#dataset)
 - [Tools and Libraries](#tools-and-libraries)
 - [Data Cleaning/Preparation](#data-cleaning/preparation)
 - [Key Results/Findings](#key-results/findings)
 - [Recommendations](#recommendations)

###   Project Description 

This project produces a market study for poultry exports in 2 stages:

- Targeting of different possible market areas using hierarchical classification (dendrogram). 

- Selection of poultry-consuming countries using principal component analysis.

The aim is to help the company target appropriate countries with high poultry consumption for international expansion.
 ###  Project Structure
- data/ :
Contains the datasets used in the project as downloaded from the FAO website for the year 2018:
 - FAOSTAT_pop_18_08.csv : Dataset of the population of each country.
 - FAOSTAT2018.csv : Dataset of protein and calorie availability for each country.
 - FAOSTAT_pib_sta_2018.csv : dataset of political stability and absence violence and gdp for each country.
 - FAOSTAT_volaille_18.csv : dataset of poultry import and feed for each country.

- notebooks/ :
  
contains the jupyter notebook used in the analysis:

P5_02_code.ipynb : Analyse des données et clustering.

-visualizations/:

Contains graphical outputs:

cercle.png: PCA visualization of the first two components.
dendrogram.png: Dendrogram showing hierarchical clustering.
acp.png: the projection of individuals onto the first two components.

### Dataset

The dataset includes the following key variables:

Zone: Geographic sales area.

Disponibilité alimentaire (kcal/personne): Food availability in calories per person.

Disponibilité de protéines en quantité (g/personne): Protein availability per person.

proportion_protéines_animal %:  proportion of protein of animal origin to the total amount of protein in the country's food supply.

Stabilité: Political stability and absence of violence in the country.

Importation - volaille: poultry import and feed in the country.

Croissance_population%: country population growth as a percentage.

PIB: measure of a country's economic performance (GDP).

### Tools and Libraries

This project is implemented using Python with the following libraries:

 _ Pandas: Data manipulation and cleaning.

 _ NumPy: Numerical computations.

 _ Scikit-learn: PCA and clustering analysis.

 _ Scipy: Hierarchical clustering and dendrograms.

 _ Matplotlib & Seaborn: Data visualization.
 
### Data Cleaning/Preparation

In the initial data preparation phase, we performed the following tasks:
1. Data loading and inspection.
2. Handling missing values.
3. Data cleaning and formatting.
   
### Key Results/Findings

#### 1. Hierarchical Clustering:
   
The dendrogram revealed 5 main clusters:

Cluster 1: Countries facing food shortages are located mainly in Africa, in areas marked by conflict and war, and are often exposed to natural disasters.

Cluster 2: developing countries at risk of instability due to their geographical and political situation

Cluster 3/4:  Rich and relatively stable countries.

Cluster 5: Countries with low population growth.

From the centroids of each cluster we find that cluster 3 and  4 countries consume more the protéin than other  countries.

#### 2. Principal Component Analysis (PCA):
PCA reduced the dataset to two main components, explaining 70.9% of the variance.

Component 1: The possibility of buying and consuming the animal proteins.

Component 2:  Shortage of poultry production in relation to demand.

After projecting the individuals onto the first factorial plane, we find that:

_ clusters 3 and 4 countries are poultry consumers.

_ cluster 3 countries have a shortage of poultry production.

### Recommendations

Based on the analysis, we recommend the following actions:

- Prioritize poultry exports to the Netherlands, the UK and Germany.
- In a second phase, extend exports to the rest of Europe.







