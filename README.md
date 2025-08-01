# Poultry Market Study: hierarchical clustering and PCA

## Table of Contents

 - [Project Description ](#project-description).
 - [Project Structure ](#project-structure)
 - [Dataset](#dataset)
 - [Tools and Libraries](#tools-and-libraries)
 - [Data Cleaning/Preparation](#data-cleaningpreparation)
 - [Analysis Methodologie](#analysis-methodologie)
   - [Hierarchical Clustering](#hierarchical-clustering)
   - [Principal Component Analysis (PCA)](#principal-component-analysis-pca)
   
 - [Key Results/Findings](#key-resultsfindings)
 - [Recommendations](#recommendations)

###   Project Description 

This project produces a market study for poultry exports in 2 stages:

- Targeting of different possible market areas using hierarchical classification (dendrogram). 

- Selection of poultry-consuming countries using principal component analysis.

The aim is to help the company target appropriate countries with high poultry consumption for international expansion.
 ###  Project Structure
- [data](./data) :
  
Contains the datasets used in the project as downloaded from the FAO website for the year 2018:

   _ [FAOSTAT_pop_18_08.csv](./data/FAOSTAT_pop_18_08.csv): Dataset of the population of each country.
   
   _ [FAOSTAT2018.csv](./data/FAOSTAT2018.csv): Dataset of protein and calorie availability for each country.
   
   _ [FAOSTAT_pib_sta_2018.csv](./data/FAOSTAT_pib_sta_2018.csv): Dataset of political stability and absence violence and gdp for each country.
     
   _ [FAOSTAT_volaille_18.csv](./data/FAOSTAT_volaille_18.csv): Dataset of poultry import and feed for each country.

   _ [df.csv](./data/df.csv): Cleaned and finalized database ready for exploration

- [notebooks](./notebooks):
  
contains the jupyter notebook used in the analysis:

  [P5_02_code.ipynb](./notebooks/P5_02_code.ipynb):data analysis and clustering.

- [visualizations](./visualizations):

Contains graphical outputs:

   _ [cercle.png](./visualizations/cercle.png): PCA visualization of the first two components.
    
   _ [dendrogram.png](./visualizations/dendrogram.png): Dendrogram showing hierarchical clustering.
    
   _ [acp.png](./visualizations/acp.png): the projection of individuals onto the first two components.

- [PowerPoint Presentation](./PowerPoint-Presentation) :
  
   _ P5_présentation: The PowerPoint file used during the final presentation of the project.


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
   
### Analysis Methodologie 
####  Hierarchical Clustering
   
The dendrogram revealed 5 main clusters:

Cluster 1: Countries facing food shortages are located mainly in Africa, in areas marked by conflict and war, and are often exposed to natural disasters.

Cluster 2: developing countries at risk of instability due to their geographical and political situation

Cluster 3/4:  Rich and relatively stable countries.

Cluster 5: Countries with low population growth.

####  Principal Component Analysis (PCA)

PCA reduced the dataset to two main components, explaining 70.9% of the variance.

Component 1: The possibility of buying and consuming the animal proteins.

Component 2:  Shortage of poultry production in relation to demand.


### Key Results/Findings

- The centroids of the groups obtained by the hierarchical clustering indicate that countries in groups 3 and 4 consume more protein than other countries.
- The PCA revealed that Group 3 and 4 countries are poultry consumers, but that Group 3 countries suffer from a shortage of poultry production.

### Recommendations

Based on the findings, we recommend the following actions:

- Prioritize poultry exports to the Netherlands, the UK and Germany.
  
- In a second phase, extend exports to the rest of Europe.







