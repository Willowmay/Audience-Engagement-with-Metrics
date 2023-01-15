# Audience-Engagement-with-Metrics

Developing a quantitative measure of audience engagement using real transactional data from televesion essentials product.

In order to find a true metric of engagement index and explore the relationship with circumstantial factors, I constructed a Linear Regression Model, and found the coefficient for the runtimes. In order to define an engagement index which doesn’t depend on runtimes, I deducted the runtime variable from the Avg % Viewed (response, dependent variable) after multiplying its coefficient. The result which generated a new column was named as Adjusted APV, the metric of engagement has been isolated from the length of program.

I developed the engagement index for every entry in the dataset and also for grouped data for each program. Since we would have the value of 1 for a program that performs exactly average, and is more or less than 1 commensurate with the program's APV. I found the median and then added 1, so the new column of data would have 1 as median number (performs exactly average).

I aggregated data by series using groupby in Python and calculated weighted arithmetic mean in order to get true engagement index for each series. I multiplied Adjusted APV with Unique HHs, calculated the sum of them with each series and divided by the sum of Unique HHs.
