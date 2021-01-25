# Zebin Wang's BST270 Project

This document is a brief README file to summarize what I have done for the BST270 final project. In the project, I aim to reproduce two figures and two tables given by NYTimes website about the current COVID-19 situation in the United States. 

The tasks for the final project includes reproducing the following plots and tables:

1. New cases as a function of time with a rolling average plot - the first plot on the page
2. Table of cases, hospitalizations and deaths - the first table on the page
3. The county-level map for previous week ('Hot spots') - the second plot on the page
4. Table of cases by state - the second table on the page

Data for cases and deaths are downloaded from the website [NYT GitHub repository](https://github.com/nytimes/covid-19-data) (use `us-counties.csv`). Data for hospitalizations would be downloaded from [The COVID Tracking Project](https://covidtracking.com/data) (use `national-history.csv`). Data for (estimated) US population would be downloaded from [US Census Bureau](https://www2.census.gov/programs-surveys/popest/datasets/2010-2019/counties/totals/co-est2019-alldata.csv) (use `co-est2019-alldata.csv`). All the data would be uploaded to GitHub for reproducibility. All these dataset are accessed at Jan. 19, 2021.

`nyt1.png`, `nyt2.png` and `nyt3.png` are the original plots given by NYTimes at Jan. 17, 2021. `georgia.png` is one bad example of data visualization.

`reproduced_nyt1.png` is a reproduction of the plot of `nyt1.png`. `reproduced_nyt1_deaths.png` reproduces the death data. `reproduced_nyt1_table.png` and `reproduced_nyt1_table_raw.png` reproduces the table of `nyt1.png`. `reproduced_nyt2.png` reproduces `nyt2.jpg`. `reproduced_nyt3_table.png` reproduces `nyt3.png`. Please notice that the plot `reproduced_nyt1_table.png` is only available when knitted to .html. So I take a screenshot at it and attach it to my response. Removing `eval = F` on the code chunk yields the table shown by the .png file.

The file `BST270_Final.Rmd` is the RMarkdown source code, which knits (through package `knitr`) to html (`BST270_Final.html`) and pdf (`BST270_Final.pdf`) files.

The data would be reproduced when the data repository is cloned, and clicking on the "knit" icon would yield the result. I set `eval = F` for .png generators to reduce the time of running the code. The following packages are required to run my R Markdown file and quoted in `BST270_Final.Rmd`.

`ggplot2`

`tidyverse`

`stringr`

`zoo`

`lubridate`

`kableExtra`

`formattable`

`sparkline`

`magick`

`urbnmapr`

`urbnthemes`

I use `R 3.6.2`, and the computer should support LaTeX in order to knit R Markdown into .pdf. R Studio is used to reproduce the data.

The result is given by RMarkdown file with knitted PDF and HTML file. Some ad-hoc adjustments and data transforming tricks have been explained in detail (please see the .Rmd file). 