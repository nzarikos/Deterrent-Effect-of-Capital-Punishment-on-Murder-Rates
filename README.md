# Capital-Punishment-Analysis

This is an ongoing project and files will be updated as the project progresses. 

Capital punishment in the United States has a long and controversial history. Some states have never had the death penalty, others have had it for over 100 years, and others have relatively recently adopted capital punishment. In 1972 the Supreme Court in Furman v Georgia passed a _de facto moratorium_ on capital punishment throughout the United States. Since then, some states have reinstated capital punishment as an appropriate ruling to violent crimes. 

There are many factors for or against capital punishment. As such, the debate continues, and there is no clear conclusion to be drawn on the subject. In my analysis, I will investigate the **deterrent** effect of capital punishment; In other words, does capital punishment change the rate of violent crime committed, specifically Murder Rates? There are many analyses about capital punishment that could be asked - such as an economic analysis - but for the time being I will focus only on deterrence. In the future I will expand the analysis to include other types of crime, and an analysis of the economic impact.  

This question is not a novel one, in fact the inspiration for this project comes from reading an [academic paper](https://cjlf.org/deathpenalty/DezRubShepDeterFinal.pdf) published in Emory University's Journal Department of Economics asking the same question in 2002, as well as UC Berkeley's Foundations of Datascience class projects. 

This paper inspired me for two main reasons:

 * As a mathematician, I wanted to understand more about the models for inference used, particularly in such a sensitive and serious issue. 
 * The conclusion was that capital punishment deters 8 future murders. In 16 years time since this publication, are we able to analyze the data better, and reach a better conclusion?
 
 
 My analysis follows 5 sections:
 
 * **Section 1:** Identifying the dataset and giving historical context to help understand the data itself, as well as what specific data is necessary and which is unecessary for this analysis. 
 * **Section 2:** Creating the tools necessary for the analysis and clearly stating the hypothesis and null hypothesis 
 * **Section 3:** *Hypothesis testing*. What are the control groups, what type of experiment is this (is it a natural experiment, controlled experiement, field experiment)?. 
 * **Section 4:** Simulation testing. Is the analysis due to chance?
 * **Section 5** Discussion of results, and limitations. Further discussion of what can be done to improve the analysis. 
 
  ## How to run capital_punishment Python Notebook 
 
 > 1) Download CrimeRates.csv and capital_punishment.ipynb
 > 2) Open terminal and run jupyter notebook (requires Anaconda) to open localhost. Run capital_punishment.ipynb
 > 3) In top cell, make sure your computer directory is set to where the CrimeRates.csv is located. For example if csv is saved in a folder called Crime located on desktop: cd User/Desktop/Crime 
 
 ## What can be done with the current version of the project
 
 Currently, users have access to a few functions and tables:
 
1) `murderous` function takes input values _year_ and _n_. The output is a graph of the _n_ states with the highest murder rates for the specified _year_. For example, Here are the 5 states with the highest murder rates for the year 1986: 
![5 states with the highest murder rates for the year 1986](murderous1986.png)

2) `murders_df` can be modified to include any number of columns from `crimes` DataFrame. To do this, just add/remove from the list of `murders_df`. 

3) There are 5 states chosen in this analysis that act as the control group. `control_1960_to_1963` is a DataFrame which. Running this cell produces a line graph visualization: 
<img width="432" alt="1960_1963" src="https://user-images.githubusercontent.com/46054540/50400412-59a59700-073b-11e9-9f1b-9bdf6b16f78b.PNG">


## What will be added in future updates

1) `murderous` will be updated to also include an average line in the bar graph. This average line will show the average murder rate across all states for that year.

2) A `simulation` funtion will be added to simulate the experiment under the null hypothesis.

3) More analytic functions will be added. These include `difference` functions to calculate changes in murder rates over a specified number of years (whether there was an increase or decrease in murder rates), a `other_crimes` function where users can expand the analysis to investigate other types of crimes, and a `cost` function to analyze the average cost of administering capital punishment for particular years.


4) A more explicit statement of which crimes are punishable by capital punishment. 

## Current state of project, and what is left to do 

Currently, the relevant DataFrame is accessible and basic analysis of murder rates is available. In the future, what needs to be done is to clearly state the hypothesis that will be tested - capital punishment causes a **decrease** in murder rates. Once this is done, what will follow is an analysis of the hypothesis, as well as a simulation under the null hypothesis to show if our conclusions are due to random chance, or if our alternative hypothesis is true. To do this, I will clearly state the test statistic that will be measured so that a corresponding p-value can be calculated to test for signifance. 


 
 
 
Specific documentation of what can be done with the capital_punishment Jupyter notebook can be found in the project wiki, as well as in capital_punishment.ipynb. 
 
 


 

Project inspired by UC Berkeley's Data 8 project https://github.com/data-8/data8assets/tree/gh-pages/materials/fa16/project/project2. 
