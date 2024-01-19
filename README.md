# Phone apps usage data and correlation with school deadlines
## 1. Reason for project and idea origin

This was the course project for Introduction to Data Science CS210 from Sabanci University, where we have to use personal data in order to create a project outcome using concepts learned throughout the course. The project is meant to challenge our learning and help us earn experience with the concepts we had to learn in order to complete it successfully.

My idea stemmed from the following: the thing I (and a lot of people) spend a considerable portion of their day on is their smartphone devices. A default app usage tracker already exists on android phones, Digital Wellbeing, but it does not offer customisation nor data exportation/extraction for the user. And so I thought why not use that data, which should already be readily available, to be able to derive my own insights.

## 2. Data collection

### 2.1 Access to usage data

With the use of Android Studio, I could create an android apk (application) that uses already-available java classes to aggregate data by day, then by week, per top 15 apps.
The following two resources were great starters:
1. A video about a basic tracker that only collects data while activated [here:](https://youtu.be/A8JfwDYCzfs?si=ZGl4vOiQ3h5Id7QQ)
2. An in-depth article about a more general app that [collects data in the background](https://medium.com/@afrinsulthana/building-an-app-usage-tracker-in-android-fe79e959ab26)

As seen above, the main java class from which you can collect data is UsageStatsManager

```java
UsageStatsManager mUsageStatsManager = (UsageStatsManager) context.getSystemService(Context.USAGE_STATS_SERVICE);
```

For more information on the class and its capabilities, refer to the [documentation](https://developer.android.com/reference/android/app/usage/UsageStats)

### 2.2 Actual creation of an android app (apk)

This is the step where I faced the most trouble: learning how to use android studio to effectively achieve what I aimed for. This step I was unable to complete while rushing through it due to the extremely high amount of details in a short time frame. This readme should be updated with the final apk whether it works or not for reference.

## 3. Data Analysis

I mean to use EDA to compare data patterns and guess where deadlines exist, then (manually) compare my guesses with the actual deadlines I've had during the queried time period. Using this I can form a null hypothesis and use p-values to decide whether to reject it or not.
