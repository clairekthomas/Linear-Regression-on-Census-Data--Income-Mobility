**Short Summary**: 

This work explores the connection between public (K-12) education spending reported in the US census and upward income mobility, as measured by the Opportunity Atlas. I account for fixed effects from gender and race and build a multivariate regression model that includes per-pupil spending and fraction of education revenue from local sources.

White male students have a higher baseline liklihood of income mobility than any other group. Female students across races benefit more per dollar spent on their education than their male counterparts, though none reach the baseline of white males. Male students of color do not benefit from per pupil education spending, suggesting that expenditures in education do not address the barriers to mobility for these students. A future aim is to understand what public expenditures do impact social mobility for male students of color, and to identify types of public spending that would have a larger positive impact on POC and female students.


**Motivation**: 

Income mobility is the ability of an individual or family to change their economic status from childhood. The American Dream is that anyone, regardless of where they were born or what class they were born into, can attain their own version of success in a society where upward mobility is possible for everyone. Economic mobility is the bedrock of the American Dream. 

It is well understood that overall economic mobility in the US has declined over the past century. The American public expects that public education spending supports income mobility. This study looks for correlations between income mobility and per-pupil spending in education. I account for fixed effects from gender and race and see significant differences in the impact of education funding based on population segmentation. This kind of analysis could support policymakers as they determine how to best allocate resources towards programs that level the playing field so that the American dream might be available to all. 

**Method**:

An Opportunity Insights analysis provides income mobility data for people born 1978-1983, broken down by location, gender and race. I use census data to determine education spending and revenue in 1995, a representative year when the subjects were in school. I use geopandas to generate heatmaps showing prominent features of each dataset.

I merge the datasets by county (FIPS) and plot correlations between income mobility and per-pupil spending on education for zip codes throughout the US for the subjects in question. 

To establish causal connection, I perform a multivariate regression that includes the fraction of school revenue obtained from local sources. This parameter relates to both regional wealth and tax policies in that area. For the population segments with clear dependence on per pupil spending, the inclusion improves the model but does not significantly reduce the coefficient that quantifies the dependence of income mobility on per pupil education spending. I suggest additional possible confounding variables that may further improve the analysis.


**Observation**

I observe a positive overall correlation between income mobility and education spending. That is, zip codes that spent more per pupil on education also saw a higher liklihood of income mobility. (That's great, it's the desired impact of a public education system.) 

The likelihood of income mobility varies across race and gender. Female students generally benefit more per dollar spent on their education, while white male students have a higher overall baseline liklihood of income mobility. Male students of color do not benefit from per pupil education spending, suggesting that expenditures in education do not address the barriers to mobility for these students. 

A future aim is to understand what public expenditures do impact social mobility for male students of color, and to identify types of public spending that would have a larger positive impact on POC and female students. The ideal is for all students to show the same benefit from education dollars that we currently observe in white students. 



**Data Sources**: 

Opportunity Insights provides income mobility analysis data:
>[Income mobility by commuting zone](
https://opportunityinsights.org/data/?geographic_level=0&topic=0&paper_id=0#resource-listing) for children born in years 1978-1983, based on census in 2000

>[Explanation of dataset](https://opportunityinsights.org/wp-content/uploads/2018/04/table_4.pdf)

>[Paper on Income Mobility by race and gender](https://opportunityinsights.org/wp-content/uploads/2018/04/race_paper.pdf)


US Census data:
> [Individual unit tables, 1995](https://www.census.gov/data/tables/1995/econ/school-finances/secondary-education-finance.html)

**Future Study**
It would be interesting to look at how student performance correlates with mobility. [This Kaggle dataset](https://www.kaggle.com/noriuk/us-education-datasets-unification-project?select=states_all.csv) merges student performance data with education spending data at the state level.
