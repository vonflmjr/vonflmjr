---
title: "Codebook for Coffee Analysis Dataset"
author: "Your Name Here"
date: "The Date Here"
output:
  html_document:
    keep_md: yes
---

## Project Description
This project examines precursor compounds in green and decaffeinated coffee and volatile aroma compounds in roasted coffee. The primary goal is to understand how different processing stages influence the flavor and aroma profiles in coffee.

## Study Design and Data Processing

### Collection of the Raw Data
- **Green Coffee Analysis**: Green and decaffeinated coffee samples were analyzed using Liquid Chromatography-Mass Spectrometry (LC-MS).
- **Roasted Coffee Analysis**: Roasted coffee samples were analyzed for volatile aroma compounds using Gas Chromatography-Mass Spectrometry (GC-MS).

### Notes on the Original (Raw) Data 
- **Green Coffee Data**: The raw data from LC-MS analysis was processed using MassHunter software. Calculations for precursor concentrations were conducted in RStudio, ensuring precise measurements of each compound.
- **Roasted Coffee Data**: GC-MS analysis was used to detect aroma compounds in roasted coffee. MassHunter software processed the data, and subsequent data analysis and visualization were completed in RStudio.

## Creating the Tidy Data File

### Guide to Create the Tidy Data File
1. Collect and organize raw data from MassHunter outputs for both green and roasted coffee.
2. Structure the data by separating green coffee (precursor data) and roasted coffee (aroma compound data).
3. Standardize variable names across both datasets to maintain consistency.

### Cleaning of the Data
Data cleaning steps included:
- Removing inconsistent values and standardizing units of measurement (mg/g for green coffee and μg/g for roasted coffee).
- Filtering and normalizing data to ensure comparability.
- Processing the data through scripts in RStudio to calculate concentrations and clean the final dataset.
- [Link to the README document that describes the code in greater detail]()

## Description of the Variables in the Dataset
General description of the file:
 - Dimensions of the dataset: 5 rows, 7 columns
 - Summary of the data: Contains information on coffee types, processing stages, and concentrations of precursor and aroma compounds.
 - Variables present in the dataset: Sample_ID, Coffee_Type, Process, Precursor_Level, Aroma_Compound, Roast_Level, Processing_Temperature

### Variable 1: Sample_ID
Short description: Unique identifier for each coffee sample.

Some information on the variable:
 - Class of the variable: Integer
 - Unique values: Each sample has a unique identifier
 - Unit of measurement: None
 - Construction: Assigned as a sequence (e.g., 1, 2, 3)

#### Notes on Sample_ID:
N/A

### Variable 2: Coffee_Type
Short description: Specifies whether the coffee sample is green (unroasted) or roasted.

Some information on the variable:
 - Class of the variable: Categorical
 - Unique values: Green Coffee, Roasted Coffee
 - Unit of measurement: None

#### Notes on Coffee_Type:
Differentiates samples based on analysis type (LC-MS for green coffee, GC-MS for roasted coffee).

### Variable 3: Process
Short description: Indicates if the coffee is decaffeinated or regular.

Some information on the variable:
 - Class of the variable: Categorical
 - Unique values: Regular, Decaffeinated
 - Unit of measurement: None

#### Notes on Process:
Used to distinguish decaffeinated samples from regular ones, impacting precursor levels.

### Variable 4: Precursor_Level
Short description: Concentration of precursor compounds in green coffee, relevant for flavor development during roasting.

Some information on the variable:
 - Class of the variable: Continuous
 - Unit of measurement: mg/g
 - Values: Non-negative values

#### Notes on Precursor_Level:
Calculated from LC-MS data processed through MassHunter, with calculations in RStudio.

### Variable 5: Aroma_Compound
Short description: Concentration of volatile aroma compounds in roasted coffee.

Some information on the variable:
 - Class of the variable: Continuous
 - Unit of measurement: μg/g
 - Values: Non-negative values

#### Notes on Aroma_Compound:
Derived from GC-MS data, processed with MassHunter, and analyzed in RStudio for quantification and visualization.

### Variable 6: Roast_Level
Short description: The level of roasting applied to the coffee beans.

Some information on the variable:
 - Class of the variable: Categorical
 - Unique values: Light, Medium, Dark
 - Unit of measurement: None

#### Notes on Roast_Level:
Affects the concentration of aroma compounds; darker roasts often have higher aroma compound levels.

### Variable 7: Processing_Temperature
Short description: Temperature at which the coffee sample was processed, particularly relevant for roasted coffee.

Some information on the variable:
 - Class of the variable: Continuous
 - Unit of measurement: °C
 - Values: Non-negative values, typically ranging from 80°C to 250°C

#### Notes on Processing_Temperature:
Relates to the degree of roasting and extraction conditions for green coffee analysis.

## Sources
- **MassHunter Software**: Used for processing raw data from LC-MS and GC-MS analyses.
- **RStudio**: Used for data cleaning, concentration calculations, and further analysis.

## Annex
If any code used in the codebook was suppressed, include it here with `echo=FALSE` to avoid displaying the results again.
