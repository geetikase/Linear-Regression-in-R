# Linear-Regression Internship Project

## EP001 by Geetika Sethi

### Setup: IN CD V VECI

1. Sign up for an account on Posit cloud, https://posit.cloud/
2. Create a workspace and name it workspace2
3. Create a project and name it p1
4. Reach the R studio console
5. Start you work at the terminal

### Linear Regression:
Linear regression on a dataset called as Advertising.csv.

Downloaded the dataset tot he local machine from the reference:https://www.kaggle.com/code/natigmamishov/linear-regression-from-scratch-on-advertising-data/input)

Upload the downloaded Advertising.csv file through the upload tab under Files. 

##Import data into R STUDIO
Type `advert <- read.csv("/cloud/project/Advertising.csv")` into the console.

## examine the top few rows of the data

```
head(advert)
```


## View the data and generate the summary

```
View(advert)
summary(advert)
```
https://github.com/geetikase/Linear-Regression-in-R/blob/main/images/salespredictions



##Install packages ISLR, MASS, ggplot.multistats and import library ggplot2

```
install.packages("ISLR")
install.packages("MASS")
install.packages("ggplot.multistats")
library(ggplot2)
```


##Examining the relationship between the TV budget and Sales using scatterplots

```
ggplot(advert, aes(TV, Sales)) + geom_smooth(method="lm") +
geom_point() + ggtitle("linear fit")
```
https://github.com/geetikase/Linear-Regression-in-R/blob/main/images/scatterplot_TVbudget_Sales.png



##Examining the relationship between the TV budget and Sales using scatterplots

```
ggplot(advert, aes(TV, Sales)) + geom_smooth(method="lm") +
geom_point() + ggtitle("linear fit")
```
https://github.com/geetikase/Linear-Regression-in-R/blob/main/images/scatterplot_TVbudget_Sales.png


## Use lm() function to create (and estimates) a linear model with the TV budget data and sales data

```
lm.TV = lm(Sales~TV, data=advert)
```


## Create a dataframe for new values of TV budgets to be able to use predict( function)
```
TV_budget <- data.frame(TV = c(11,11,12,12,12,12,13,13,13,13))
```

##predict the Sales
```
predict(lm.TV, newdata = TV_budget)
```
https://github.com/geetikase/Linear-Regression-in-R/blob/main/images/salespredictions


References
https://mdporter.github.io/ST597/lectures/16-regression.pdf
https://nicklyz.github.io/R-Studio-Tutorial/




