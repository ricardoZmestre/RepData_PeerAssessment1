# Reproducible Research: Peer Assessment 1



## Loading and preprocessing the data

Loading from dataset **activity.zip**. The file can be found in [forked Git repo for the assignment](https://github.com/ricardoZmestre/RepData_PeerAssessment1).



## What is mean total number of steps taken per day?

Histogram of the number of steps taken per day.

![](PA1_template_files/figure-html/question_1-1.png) 

The overall total number of steps taken per day is 570608.

The mean of the steps taken per day is 10766.19.

The median of the steps taken per day is 10765.00.

## What is the average daily activity pattern?

![](PA1_template_files/figure-html/question 2-1.png) 

The maximum mean number of steps per day is 206.17.

The corresponding period is 835.

## Imputing missing values

NA imputations using overall mean.





![](PA1_template_files/figure-html/question 3-1.png) 

The number of Nas in the original dataset is 2304.

The mean of the steps taken per day, corrected for Nas, is 10766.19.

The median of the steps taken per day, corrected for Nas, is 10766.19.

## Are there differences in activity patterns between weekdays and weekends?

![](PA1_template_files/figure-html/question 4-1.png) 

Indeed: on weekends, the number of paces is more evenly distributed across the day, and overall there is less walking on weekdays than on weekends.

---
