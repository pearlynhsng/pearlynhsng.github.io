---
title: "Reading data"
excerpt: "Importing and reading data in R"
collection: stats
---

The very first step in analyzing data is, well, opening and reading your data. If you collected your own data, then you probably have a pretty good idea of exactly which variables will be in your data. But if you're using a secondary data source (or if you're taking on a project from someone else) you might have no idea what you're walking into. Scary! Fun, but also kind of scary.

So in this tutorial, we'll go through the very basic steps of opening your data in R and poking around it to see what the data looks like.

## Necessary packages

In Psychology, your data files are most likely to be .csv .xlsx or .sav files. Base R can handle .csv and .xlsx files, but you will need the 'haven' package for .sav files and the 'readxl' package for .xlsx files. You will also need the 'dplyr' package for a number of handy functions that will allow you to check the structure of your data.

```r
install.packages("dplyr")
library(dplyr)
install.packages("haven")
library(haven)
install.packages("readxl")
library(readxl)
```

## Importing files

Great! Now we need to make sure your working directory is set to wherever your data file is. You can either do that the cool mouse-free way:
```r
getwd() #This will display your current working directory
setwd(dir = "/Users/me/Rprojects/data") #Set this to whatever you want your directory to be. 
```
Or the point-and-click method in RStudio by going to *Session > Set working directory > Choose directory* 

### Reading .csv files
```r
data<- read.csv('datafile.csv')
```
### Reading .xlsx files
```r
data<- read_excel('datafile.xlsx') #Method 1
data<- read_xlsx('datafile.xlsx') #Method 2
```
### Reading .sav files
```r
data<- read_sav('datafile.sav')
```

## Checking data structure
Coming soon!

