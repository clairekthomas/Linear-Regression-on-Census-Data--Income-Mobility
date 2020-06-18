This notebook looks for correlations in income mobility and public (K-12) education spending. It uses income mobility data for people born in 1978-1983, and education spending data in a representative year for those subjects (1995). 

**Motivation**: 

Income mobility is the ability of an individual or family to improve (or lower) their economic status. The American Dream is that anyone, regardless of where they were born or what class they were born into, can attain their own version of success in a society where upward mobility is possible for everyone. Economic mobility is the bedrock of the American Dream. 

It is well understood that overall economic mobility in the US has declined over the past century. The American public expects that public education spending supports income mobility. This notebook studies variations in income mobility on the basis of race, gender, and zip code, and looks for correlations between income mobility and education spending.

**Goal**:

The goal of this study is to identify trends in education spending that correlate most strongly with a level playing field for all students. For example, the notebook identifies correlations between income mobility and per-pupil spending on particular education resources for zip codes throughout the US. It further explores differences in those correlations for students depending on their race and gender. 

It is a given that income mobility depends on more than public education, and that K-12 education financing will itself correlate with factors that impact mobility beyond education expenses (eg, policing policy and neighborhood wealth). The differences in the correlation between student outcomes and education spending for students in the same zip code but different races and genders are the most telling features of this data. 

**Observations**

Preliminary analysis shows a positive overall correlation between income mobility and education spending. That is, zip codes that spent more per pupil on education also saw a higher liklihood of income mobility. (That's great, it's the desired impact of a public education system.) 

The likelihood of income mobility varies across race and gender. Female students generally benefit more per dollar spent on their education, while male students have a higher overall baseline liklihood of income mobility. Male students of color do not statistically significantly benefit from per pupil education spending. Education spending doesn't correlate with their success. 

To establish causal connection, I include in a linear regression the fraction of school revenue obtained from local sources. This parameter relates to both regional wealth and tax policies in that area. For many of the datasets with clear dependence on per pupil spending, the inclusion improves the model but does not significantly reduce the coefficient that quantifies the dependence of income mobility on per pupil education spending.  I suggest additional possible confounding variables that may further improve the analysis.

A future aim is to identify types of spending that could have larger positive impact on POC and female students. The ideal is for all students to show the same benefit from education dollars that we currently observe in white students. This type of analysis may find application in education policy. 



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
