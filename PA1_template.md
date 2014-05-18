# Reproducible Research: Peer Assessment 1


## Loading and preprocessing the data

Start by unzipping the compressed file and reading the data into R.


```r
activity <- read.csv(unz(paste(getwd(), "/activity.zip", sep = ""), "activity.csv"), 
    header = TRUE, sep = ",")
```


## What is mean total number of steps taken per day?

![plot of chunk meandaily](figure/meandaily.png) 


The mean steps per day from this data set is 37.3826.
The median number of steps per day is 0.

## What is the average daily activity pattern?

![plot of chunk avgdaily](figure/avgdaily.png) 


This individual averaged 206.1698 steps during the 104th interval.

## Imputing missing values




Unfortunately, there are 2304 observations in the data that are missing the number of steps taken.

We compensate by substituting the average number of steps for a given five-minute interval across all days whenever data for an individual day does not exist.

![plot of chunk replace](figure/replace.png) 


The new mean steps per day from this data set is 37.3826.
The new median number of steps per day is 0.

## Are there differences in activity patterns between weekdays and weekends?




![plot of chunk avgdaily2](figure/avgdaily21.png) ![plot of chunk avgdaily2](figure/avgdaily22.png) 

