# Problem Set 1
Due January 31


## What to submit and how
Type your answers to the questions below. Write clearly, and format your tables and visuals appropriately. For full credit, paste the R code chunk you used directly below your answer. Submit your work in hard copy. 

## Gapminder analysis
Use the Gapminder data to extend analyses in sections 5.3-5.4 of Dr. Jenny Bryan's Stat545. Bryan relies on an abridged version of the dataset, `gapminder`. Your analysis must use the full `gapminder_unfiltered` data. To access the data, install and load the `gapminder` package. I recommend that you then assign the data to a new object (e.g., `df = gapminder_unfiltered`).

1. In a few sentences, describe the unfiltered Gapminder data frame. Be sure to note the number of observations, available years of data, and number of variables.
2. Plot life expectancy (`lifeExp`) by year. 
3. Present a table/tabulation of the number of observations in each continent. 
4. Recreate the plot at the end of section 5.5 using the unfiltered data. The plot shows the relationship between life expectancy and GDP per capita (`gdpPercap`) by continent. Present only the final plot. 


## Correct my code!
The script below doesn't work! I get error message after error message. For reference, this should work from a brand new session, and I'm using the hurricanes.csv dataset. 

```
# My bad code
# Jan 2023

# open my data
  hdata = read_csv(hurricanes.csv)

# summarize damage by "gender" of hurricane name
  hdata %>%
     group_by(gender)
     summarise(
       obs = n()
       median = median(damage),
       avg = mean(damage)
     )
```

5. Type the corrected code chunk into your problem set. For any line that you corrected, add a very brief annotation noting the fix (i.e. `# assign to object 'df'`). *Hint: there are at least four errors.*

## Alabama Senate postmortem
In December 2017, Alabama held a special election to fill the U.S. Senate seat vacated by the now former U.S. Attorney General Jeff Sessions. Doug Jones's (D) victory over Roy Moore (R) in one of the most Republican states in the nation surprised serious and casual observers alike.

Download a part of my election-night spreadsheet ("alspecial.csv", posted in this folder). This county-level dataset records projected turnout, observed vote totals for each candidate, and vote targets for Jones (i.e. the minimum votes or percentage of the vote he would need to win the election). Use the data to answer the questions below.

6. For how many counties do you have data?
7. In one or two sentences and with reference to appropriate summary statistics, describe the distribution of Moore's vote share in the 2017 special election.
8. In how many counties did Jones earn more votes than Moore?
9. Create a histogram of the difference between Jones’s vote total and his expected vote total. Note that you will need to create a new variable.
10. Create a scatter plot of observed vote total over expected vote total. 

**BONUS OPPORTUNITY**: Use color-coding to differentiate counties Jones won from counties where he lost. Then plot the data over log-transformed axes to improve readability.
