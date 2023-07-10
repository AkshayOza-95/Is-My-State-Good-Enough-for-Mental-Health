# Is My State Good Enough for Mental Health

## Background 

Mental health issues have long held stigmas, despite the fact that one-in-five US adults will suffer from a mental health condition during his or her lifetime, and countless family members and friends will be affected in the process.  Whether you suffer from mild depression or anxiety, or you’re helping a loved one cope with a more serious condition such as schizophrenia or bipolar disorder, you probably realize that it is not only the condition that’s difficult to live with, but also the social isolation. 
Mental health illness is not a wound we can see, hence it often becomes difficult for family and friends to empathize with the patient. Another major challenge: mental illness is incredibly heterogeneous, encompassing both mild and severe symptoms, and including everything from social anxiety to schizophrenia. The journey towards healing in such cases is often a lonely one, as people do not understand what it is like to have a mental health concern. 

States have significant power in making decisions about their mental health systems so mental health regulations and available services can look very different from state to state and even from county to county. State mental health systems must meet certain standards set by the federal government, but they are free to expand beyond what exists at the federal level and improve services, access, and protections for consumers. This project seeks to provide multi-layered analysis for the average number of unhealthy mental days faced by people in each state over the years 2009-2018 and further differentiate it by race and gender. External factors in these states which might have an impact on the mental health of its residents and how they have changed over time, are also taken into consideration.

## Data 

The primary data source for this project is the <a href= https://chronicdata.cdc.gov/Chronic-Disease-Indicators/U-S-Chronic-Disease-Indicators-Mental-Health/ixrt-gnsg> Centre for Disease Control </a> data about mental health across all the state in the US between year 2009-2018. The total number of rows in our dataset is 6960 and number of columns is 16.

The data for well-being index and access to mental health care were present in PDF format which were converted using this python package called tabula and camelot-py. 

**Some of the major attributes in the data are:**
- `state` : Name of the State
- `year` : Year of the record
- `location_id` : FIPS State ID
- `mean` : average number of unhealthy mental days for the overall population
- `age_adjusted_mean`: average number of unhealthy mental days to compare different age group structures
- `upper_CI`: Upper limit of 95% confidence interval for the `mean` or `age_adjusted_mean`
- `lower_CI`: Lower limit of 95% confidence interval for the `mean` or `age_adjusted_mean`
- `stratification`: stratification by gender, race or overall (There are many columns/features for stratification) 

*The primary data source is unclean and would need to be cleaned before merging with the other tables*

<br>For understanding the correlation between number of unhealthy mental days and other factors, various data sets such as insurance statistics from <a href =https://www.kff.org/other/state-indicator> KFF </a>, mental health care rankings from <a href= https://www.mhanational.org/issues/mental-health-america-all-data> Mental Health America </a>, and Well-Being Index for States in the US (2014-2018) by <a href= https://wellbeingindex.sharecare.com/download-reports/> Gallup </a> will be used. This data would provide nuanced insights and enable factoring external causes to paint a more comprehensive picture.

## Required Libraries

```python
!pip pandas
!pip numpy
!pip install seaborn
!pip install plotnine
!pip install plotly 
!conda install -c conda-forge nodejs 
!pip install jupyterlab "ipywidgets==7.5" 
!jupyter labextension install jupyterlab-plotly@4.11.0
```
## Watch the Presentation

You can watch the team present some major findings from the project by clicking <a href= https://youtu.be/nqzl_qpnw9g > here </a>


