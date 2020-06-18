# AMU/AMR KAP+ Excel Tool Tutorial

## Introduction 

This is a tutorial guide for the AMU/AMR KAP+ Excel Tool, which is designed to accompany surveyors in the field. 

The tool is designed for light *exploratory data analysis*, but its data tables are designed to be compatible (and efficient) with more robust statistical programming languages/software such as SPSS, SQL, R etc. 
However, the naming conventions are optimized for data wrangling in the "tidyverse" R package.

### How does the Excel tool work?

In a nutshell, the Excel tool automatically codes, processes, and analyzes raw data. Survey data is manually inputted with the corresponding codebook answers in the **raw_data** sheet. 

Data in the **raw_data** sheet are automatically coded into their corresponding numerical codes in the **coded_data** sheet. 

Coded data is summarized both as individual items in the **survey_answers** sheet and as variables in the **processed_data** sheet. 

The variable scores in the latter are further processed into parameters in the **summary** sheet and tested for significant correlations in the **correlations** sheet.

![How the Excel tool works](https://drive.google.com/file/d/1vqtBkTQLO220Ea0PBtLU0x_FkaXo0VOB/view?usp=sharing)

### Anatomy of the Data Table
The KAP+ Excel Tool contains three data tables: 
- **raw_data** which contains strings (text) data, 
- **coded_data** which codes the string data in *raw_data* into numeric data, and 
- **processed_data** which groups the codes in the *coded_data* by variable and takes the variable scores. 

Each data table can be found in separate **sheets** of the same names in the bottom part of the Excel interface. 

The tables have an identical layout. The first 3 rows of the data tables are the **indicator rows** showing the **variable category rows**, **variable rows**, and **item rows**

#### Variable category rows/ Survey Parts
Variable category rows indicate which part of the survey a group of columns belong to. 

The survey is divided into four or five main parts. Each part is uniformly color-coded in all iterations of the Excel tool for easy identification. 


#### Variable rows
Variable rows indicate what variables a group of columns belong to. As we will see later in this tutorial, variable scores are computed in the **processed_data* sheet by summing up the columns that belong to specific variable rows. 

#### Item rows
Item rows indicate the individual items of the survey. Each item row cell follows the naming convention:

 

    #(surveypart|sd,k,a,p,s,i,c) + item no. + "_" + item description
for example:

> k1_ab 
> (Knowledge item no. 1_antibiotics)
> "Knowledge about antibiotics

#### Observation rows

Observation rows contain the answers of the survey respondents. 

Each data table contains a respondent ID column in the leftmost part of the data table. 

## Navigating the Excel tool sheets

### Intro sheet
The intro sheet contains tables 
#### Survey Information

#### Document Links
#### Repository Link
#### Sheet links

### Data tables
#### raw_data
#### coded_data
#### processed_data
		
### Summary tables
#### survey_answers
#### summary
#### correlation

## Inputting data

### Using the Codebook

## Updating new observations

## Importing to .csv


