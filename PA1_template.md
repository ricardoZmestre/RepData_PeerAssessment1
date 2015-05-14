# Reproducible Research: Peer Assessment 1



## Loading and preprocessing the data

Loading from dataset **activity.zip**. The file can be found in [forked Git repo for the assignment](https://github.com/ricardoZmestre/RepData_PeerAssessment1).



## What is mean total number of steps taken per day?

Histogram of the number of steps taken per day.

![](PA1_template_files/figure-html/question_1-1.png) 

The overall total number of steps taken per day (which is the same as the overall number of steps *tout court*) is 570608.

The mean of the steps taken per day is 10766.19.

The median of the steps taken per day is 10765.00.

## What is the average daily activity pattern?

![](PA1_template_files/figure-html/question 2-1.png) 

The maximum mean number of steps per interval is 206.17.

The corresponding interval is 835.

These are the mean steps and interval for which a maximum is reached.

## Imputing missing values

NA imputation is done separately per interval, i.e. each interval with NA is imputed the same number of steps as the mean for that same interval. For instance, an NA appearing in (say) interval 1800 will be replaced by the mean of all intervals 1800 in the dataset for which data are available. This imputation is simple enough but at the same time takes into account that some periods in the day have specificities, such as NA or zero steps during most of the night.




![](PA1_template_files/figure-html/question 3-1.png) 

The number of Nas in the original dataset is 2304.

The mean of the steps taken per day, corrected for Nas, is 10766.19. Note that the mean has not changed: this is the consequence of the fact that NAs are evenly distributed by intervals, with 8 NAs per interval, and that each imputed interval  has by construction the same mean as the same interval with observations. This implies that the numbers introduced into the data frame have the same overall mean as the original numbers (barring NAs), hence the resulting mean is also not changed.

The median of the steps taken per day, corrected for Nas, is 10766.19. Note now that the median has changed and is now similar to the mean. This is because we have, in the NA imputation, added numbers which are by construction closer to the centre of the distribution (because of the law of large numbers), bringing the median closer to the mean.

Just to check, the deciles of the original data (averaged per day) were:


-----  --------
0%         41.0
10%      5102.6
20%      8342.4
30%      9867.6
40%     10279.8
50%     10765.0
60%     11830.0
70%     12796.6
80%     13571.6
90%     15107.6
100%    21194.0
-----  --------

<br>And they are now:


-----  ---------
0%         41.00
10%      5441.00
20%      8821.00
30%     10119.00
40%     10571.00
50%     10766.19
60%     11162.00
70%     12426.00
80%     13452.00
90%     15098.00
100%    21194.00
-----  ---------

<br>Note that the 50% percentile corresponds to the median.

## Are there differences in activity patterns between weekdays and weekends?

![](PA1_template_files/figure-html/question 4-1.png) 

Indeed: on weekends, the number of paces is more evenly distributed across the day, and overall there is less walking on weekdays than on weekends.

---
