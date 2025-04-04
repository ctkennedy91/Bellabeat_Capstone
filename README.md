# Google Data Analytics Capstone: Bellabeat Case Study

How Can A Wellness Technology Company Play It Smart?

## CASE STUDY DESCRIPTION 

Bellabeat is a high-tech manufacturer of health-focused products geared towards women. While small but successful, they have the potential of becoming a larger player in the global smart device market. To further expand their products and reach a larger number of consumers, analyzing smart device data to gain insight into how consumers are using their smart devices proves beneficial for research purposes as a means of unlocking new growth opportunities for the company.

## CASE STUDY GOAL 

The goal of this Bellabeat case study is to answer key business questions by following the steps of the data analysis process: ask, prepare, process, analyze, share, and act. Each step of the process incorporates unique questions and tasks designed to guide and heighten analysis.

<details>
  
<summary>1. ASK</summary>

The purpose of the ask phase of the data analysis process is to define and fully understand the problem presented by the stakeholders with the goal of being able to help the stakeholders resolve their questions.

Structured thinking is a major part of the ask phase. Structured thinking includes:

1. Recognizing the current problem or situation
2. Organizing available information
3. Revealing gaps and opportunities
4. Identifying my options

When it comes to asking questions, questions should be open-ended and effective. Open-ended questions allow for elaboration and valuable insight. Effective questions follow the **SMART** methodology:

1. **Specific:** simple, significant, and focused on a single topic
2. **Measurable:** can be quantified and assessed
3. **Action-oriented:** help me get to the end result
4. **Relevant:** matter, are important, and have significance to the problem I'm trying to solve
5. **Time-bound:** specify th etime to be studied, which limits the range of possibilities and enables me to focus on relevant data

**Questions to ask**

**1. Who are the key stakeholders?**

Urška Sršen – Bellabeat’s cofounder and Chief Creative Officer.

Sando Mur – Mathematician, Bellabeat’s cofounder, and a key member of the executive team.

**2. What is the problem I am trying to solve?**

Identify how consumers use non-Bellabeat devices to track their health and how this information is used to provide the best recommendation for Bellabeat marketing strategy.

**3. How can my insights drive business decisions?**

Discover what the primary goal for using a fitness tracker is. Is it to monitor changes in heartrate? Activity level? Menstrual cycle? Stress? Sleep? Weight loss or gain? Determining this can allow Bellabeat to use that information to drive sales by promoting the benefits of any given product.

***Key business questions***

1. What are some trends in smart device usage?
2. How could these trends apply to Bellabeat customers?
3. How could these trends help influence Bellabeat marketing strategy?</details>

<details>
<summary> 2. PREPARE</summary>  

Preparing data includes addressing potential issues of bias and credibility and determining if the data is good and reliable. Urška Sršen has encouraged me to use public data that explores smart device users’ daily habits. She provided me with a specific data set on Kaggle called [FitBit Fitness Tracker Data](https://www.kaggle.com/datasets/arashnic/fitbit). This dataset, created by Kaggle user Möbius, was generated by respondents to a distributed survey via Amazon Mechanical Turk between 03.12.2016-05.12.2016. Thirty eligible Fitbit users consented to the submission of personal tracker data, including minute-level output for physical activity, heart rate, and sleep monitoring. This data also includes information about daily activity, steps, and heart rate that can be used to explore users’ habits. The data is stored in 29 CSV files and is organized in a wide format.

**Questions to ask**

**1. Are there issues with bias, integrity, or credibility in this data?**

As the description of the dataset stated, there are only thirty eligible Fitbit users that consented to the submission of personal tracker data. These participants may have been chosen at random, but it is uncertain if all parts of the population have an equal chance of being included. The ratio of female to male participants, people with disabilities or health concerns, age, etc. are all unknown demographics. The only identifying factor within the dataset are thirty unique ID numbers linked to each participant. While the privacy of the participants was upheld, the dataset still displays sample bias because of its low number of participants. The limitations caused by sample size bias can be easily addressed by adding another dataset possibly found in other sources of public data. 
While the sample size is an issue, the integrity of the Fitbit dataset is solid. It contains consistent data, relatively few errors (such as duplications), a wide variety of data, and is generally accurate and trustworthy. Ultimately, this dataset provides a good starting point for analyzing trends with people who use fitness trackers.

**2. How am I addressing licensing, privacy, security, and accessibility?**

As stated in Kaggle, the dataset is under `Public Domain`.

One way to help identify a good data source is to use the **ROCCC** process. **ROCCC** stands for reliable, original, comprehensive, current, and cited.

**1. Reliable:** The numerous spreadsheets provided include very few errors. Duplications are minimal and null values are indicative of when users did not wear their watches or watches weren’t charged. However, the dataset includes of small sample size of only 33 users, which indicates sample bias. There is no way of knowing if the sample sizes is inclusive of age, sex, ethnicity, health, etc. The reliability of this data is __low__.

**2. Original:** The dataset comes from a third-party survey system called Amazon Mechanical Turk where participants can get paid for completing simple tasks. There is no original data source. The originality of this data is __low__.

**3. Comprehensive:** The dataset includes basic fitness tracking information, such as weight loss/gain, heartrate, calories, step counting, sleep duration, and intensity level. The gathered data does align with Bellabeat’s business goal. The comprehensiveness of this data is __high__.

**4. Current:** This dataset is no longer current. The data was originally collected in the spring of 2016, making this data 8 years old. The age of this dataset makes how current it is __low__.

**5. Cited:** This dataset was gathered from a third-party source and is therefore not cited, which indicates **low** in terms of good data.</details>

<details>
<summary> 3. PROCESS</summary>

One of the first obstacles that I faced when beginning to process my chosen data was the data being kept in two separate folders, titled `mturkfitbit_export_3.12.16-4.11.16` and `mturkfitbit_export_4.12.16-5.12.16`, and contained multiple CSV files that had identical titles, such as `hourlySteps_merged`. To conduct my analysis, I focused on three datasets: `sleepDay_merged.csv`, `dailyActivity_merged.csv`, and `weightLogInfo_merged.csv`. The activity and weight datasets have identical names between the two main file folders. To overcome this, I decided to use RStudio to process my data because of its ease of use and convenience. I started off by uploading spreadsheets to RStudio. Check column names and summaries of each spreadsheet. Merge datasets if needed.

Once merged, I counted rows, checked to see if there were duplicates, and then remove duplicates if needed. I also separated date and time if necessary. Once these steps were completed, I viewed the data tables and determined if all columns were needed. I excluded columns that were not necessary. 

**Questions to ask**

**1. What tools am I choosing and why?**

I cleaned my data using RStudio because of the ease of use. I can easily manipulate my data with using various codes and a few lines of simple code. 

**2. Have I ensured my data’s integrity?**

Yes, I have ensured my data’s integrity by constantly saving my work, being consistent between datasets, and being accurate with my cleaning. 

**3. What steps have I taken to ensure that my data is clean?**

For each dataset, I checked column names, summaries, counted rows, checked for duplicates, separated dates and times if needed, and removed unnecessary columns.

**4. How can I verify that my data is clean and ready to analyze?**

It is consistent and accurate and maintains integrity.

**5. Have I documented my cleaning process so I can review and share those results?**

Throughout the cleaning process, I have made documentations about the steps that I have taken. In RStudio, I would use '#' before a section of code to explain what I was doing, such as checking for duplicates. I also wrote my markdown report as I was cleaning my data. 

### Setting up my RStudio environment

I started off by installing the 'tidyverse' package and used the library function to load 'tidyverse', 'readr', and 'dplyr':

```{r - loading packages}
library(tidyverse)

library(readr)

library(dplyr)
```

Note: 'dplyr' is needed for data manipulation. 'readr' is needed to download .csv files to my laptop.

### Begin uploading CSV files

```{r - uploading CSV files and assigning datasets}
activity_1 <- [dailyActivity_merged_Sec2.csv](https://github.com/user-attachments/files/19495855/dailyActivity_merged_Sec2.csv)

activity_2 <- [dailyActivity_merged_Sec1.csv](https://github.com/user-attachments/files/19495853/dailyActivity_merged_Sec1.csv)

sleep <- [sleepDay_merged.csv](https://github.com/user-attachments/files/19495868/sleepDay_merged.csv)

weight1 <- [weightLogInfo_merged_Sec1.csv](https://github.com/user-attachments/files/19495874/weightLogInfo_merged_Sec1.csv)

weight2 <- [weightLogInfo_merged_Sec2.csv](https://github.com/user-attachments/files/19495906/weightLogInfo_merged_Sec2.csv)
```

Once CSV files have been uploaded and assigned to an easier to work with variables, I went through each table using 'summary', 'head', and 'colnames'.

```{r - viewing and summarizing functions}
summary(activity_1)

summary(activity_2)

head(activity_1)

head(activity_2)

colnames(activity_1)

colnames(activity_2)

summary(sleep)

head(sleep)

colnames(sleep)

summary(weight1)

summary(weight2)

head(weight1)

head(weight2)

colnames(weight1)

colnames(weight2)

```

### Merging datasets

The daily activity and the weight log info CSV files were originally kept in two seperate CSV files. The files needed to be merged. I used the 'rbind' function to do this. After merging, I got a summary of each new dataset by using 'summary', 'head', and 'colnames'.

The sleep data was only kept in a singular CSV file, so no merging was needed.

```{r - merging data into one dataset}
combined_activity <- rbind(activity_1, activity_2)

summary(combined_activity)

head(combined_activity)

colnames(combined_activity)

weight <- rbind(weight1,weight2)

summary(weight)

head(weight)

colnames(weight)
```

### Cleaning datasets

After merging the two datasets, I determined that there were some columns that I did not need. I started my cleaning process by excluding these columns.

```{r - column deletion and view tables}
combined_activity <- subset(combined_activity, select = -c(TrackerDistance,LoggedActivitiesDistance,VeryActiveDistance,ModeratelyActiveDistance,LightActiveDistance,SedentaryActiveDistance))

weight <- subset(weight,select = -c(Time,WeightKg,Fat,IsManualReport,LogId))
```

Note: c() is used for creating a list of items. However, -c() does the opposite and omits a list of chosen items. 

After deleting unnecessary columns from tables, I used 'nrow' and 'duplicated' to count the number of rows and to determine if there were duplicated rows in each table. I also changed the date/time format from 'm/dd/yyyy hh:mm' to just 'm/dd/yyyy/' by using the 'as.Date' function and specifying '%m%d%Y'. Using '%Y' returned a four digit year. If I were to use a '%y', it would have returned a two digit year.

```{r counting rows, finding duplicates, and changing date/time format}
nrow(combined_activity)

nrow(combined_activity[duplicated(combined_activity),])

combined_activity$ActivityDate = as.Date(combined_activity$ActivityDate, "%m/%d/%Y")

nrow(sleep)

nrow(sleep[duplicated(sleep),])

sleep <- sleep %>%
  separate(SleepDay, c("Date", "Time"), " ")

sleep <- subset(sleep,select = -c(Time,TotalSleepRecords))

sleep$Date = as.Date(sleep$Date, "%m/%d/%Y")

nrow(weight)

nrow(weight[duplicated(weight),])

weight <- unique(weight)

weight$Date = as.Date(weight$Date, "%m/%d/%Y")
```

combined_activity has 1397 rows and 0 duplicates found. 

The sleep table has 410 rows with 3 duplicates found. After removed the duplicates, 407 unique rows remain.

The weight table has 100 rows with 2 duplicates found. After removing the duplicates, 98 unique rows remain. 

### Export datasets as CSV files

After cleaning my data, I exported my work as CSV files. I used the 'write.csv' function.

```{r - export tables}
write.csv(combined_activity, "combined_activity.csv")

write.csv(sleep, "sleep.csv")

write.csv(weight, "weight.csv")
```

### Setting up a pie chart

I created a majority of my visualizations using Tableau. However, I had issues creating a pie chart. I wanted to use a pie chart to quickly visualize the differences in activity levels. To do this, I first focused on the minutes spent in the four different activity levels and then combined those minutes into its own variable: sedentary, lightly active, fairly active, and very active.

```{r - creating variables for activity minutes}
sedentary <- sum(combined_activity$SedentaryMinutes)

lightly <- sum(combined_activity$LightlyActiveMinutes)

fairly <- sum(combined_activity$FairlyActiveMinutes)

very <- sum(combined_activity$VeryActiveMinutes)

activity_minutes <- c(sedentary,lightly,fairly,very)

list(activity_minutes)
```

I used the 'list' function to quickly understand which activity level would have the most accumulated amount of time. I used 'activity_minutes' to create a formula to determine the percentage breakdown of each activity level.

```{r determining percentages}
activity_percent <- round(activity_minutes/sum(activity_minutes)*100,1)

list(activity_percent)
```

Running the 'list' function will provide me with a list of the percentages that I will later use as labels in the code for my pie chart.</details> 

<details>
<summary> 4. ANALYZE</summary>

The three data tables that I used were `combined_activity`, `weight`, and `sleep`. To quickly analyze the data, I used the 'summary' function.

```{r data table summaries}
combined_activity %>%
    select(TotalSteps,
          TotalDistance,
          VeryActiveMinutes,
          FairlyActiveMinutes,
          LightlyActiveMinutes,
          SedentaryMinutes,
          Calories) %>%
    summary()

weight %>%
    select(WeightPounds,
          BMI) %>%
    summary()

sleep %>%
    select(TotalMinutesAsleep,
          TotalTimeInBed) %>%
    summary()
```

### The combined activity dataset

1. The average number of total steps the FitBit participants tooks was 7281 a day. The average total distance was 5.219 miles. The Center of Disease Control (CDC), recommends that adults aim for a goal of 10,000 steps a day, or roughly 5 miles a day.

2. FitBit user activity levels were broken down into four different categroies: Very active, fairly active, lightly active, and sedentary. This was tracked in minutes, with the average minutes for each activity level being: 19.68, 13.4,185.4, 992.5, respectively. 

3. 992.5 minutes of sedentary activity is roughly 16.5 hours. 

4. The CDC recommends 30-40 minutes of moderate- to vigorous-intensity (fairly to very active) of physical activity to help offset an excessive sedentary lifestyle that includes sitting for 10 or more hours a day.

5. FitBit users burned an average of 2266 calories a day. The recommended number of daily calories burned is dependent on age, sex, height, weight, and activity level. 

### The weight dataset

1. The average weight of FitBit participants is 159.8 pounds.

2. The average BMI 25.37. According to the CDC, a BMI of 25 classifies someone as overweight.

3. There is very limited insight on weight. There is no historic weight data to give a starting weight for users.

4. Because the FitBit users are anonymous, there is no way of knowing their age, height, and sex, which are factors that are used when calculating BMI.

5. BMI does not take into account people with high muscle mass, high bone density, or people who have lost muscle mass.

6. The weight dataset had the fewest number of participants.

### The sleep dataset

1. FitBit users spent an average of 458.6 minutes, or 7.64 hours, in bed.

2. FitBit users spent got an average of 419.5 minutes of sleep, or about 7 hours. The CDC recommends 7 to 9 hours of sleep for adults.

3. The difference between the total time spent in bed and the total amount of sleep is 39.1 minutes. It takes the average person 10 to 20 minutes to fall asleep, with some falling asleep within minutes and others taking longer than 30 minutes.</details> 

<details>
<summary> 5. SHARE</summary>

### Combined activity pie chart

First, I created two vectors: one for establishing color choices and the other for the names in the legend.

```{r vectors}
myColors <- c("skyblue","green","yellow","purple")

legend_names <- c("Sedentary","Lightly Active","Fairly Active","Very Active")
```

Creating a vector for my color choices saves on time for writing the code for my pie chart.
    
As previously mentioned, the list of percentages used with `labels =` was determined using `list(activity_percent)`. `main =` is used to establish the main title of the chart, `border =` is used to create a border around each wedge of the chart, `col =` followed by my color vector to establish the color for each wedge, and `radius =` to increase the size of my pie chart.
    
I did not include the legend in my pie chart code, because I kept running into an error every time I did. Instead, I ran my legend code separately.
`x=` determines the position of the legend, `cex=` determines the size, `title=` to create a title name for the legend, `fill =` to use the same color vector that I used in my pie chart code to keep the colors consistent. The vector legend_names was created earlier and lists the activity levels.

```{r base R pie chart}
pie(activity_percent,
    labels = c("82%","15.3%","1.1%","1.6%"),
    main = "Breakdown of Activity Levels by Minutes",
    border = "white",
    col = myColors,
    radius = 1)

legend(x="bottomleft",cex=.55,title="Activity Levels",legend_names,fill = myColors)
```

!![Activity_levels_piechart](https://github.com/user-attachments/assets/e02182c3-754b-4f2a-ae92-eac251f77a77)

During the analysis phase, I knew that sedentary was the activity level of a majority of participating FitBit users. However, I wanted to see a comparative breakdown of the activity levels. I decided that the quickest and most efficient way to view this information was with a pie chart. The pie chart shows that sedentary takes the majority of the total time with 82%, lightly active takes up 15.3%, fairly active is at 1.6%, and very active is only 1.1% of the total time spent being active. 

### Total steps to sedentary minutes scatterplot

[total_steps_sedentary_minutes](https://github.com/user-attachments/assets/7c01ba69-bec6-4a61-a1aa-2796cdfbbee0)

The first thing I had to do when creating this scatterplot was to exclude data points that equalled 0 sedentary minutes or exceeded 1440 minutes because that is how many minutes there are in 24 hours. The scatterplot shows that there is a high concentration of data points in the upper left quadrant going towards the vertical average line, which indicates that FitBit users spend a majority of their time being sedentary and walking less than the recommended daily goal of 10,000 steps.

### Total steps per day of week column chart

![total_steps_week](https://github.com/user-attachments/assets/745e6d25-682a-4fbc-bbbd-fa9efd25e491)

The column chart shows that FitBit users took the most steps on Tuesdays. The second busiest day of the week was Saturday, followed by Wednesday. The least busiest day of the week was Sunday. 

### Weight line chart

![weight](https://github.com/user-attachments/assets/61a4b972-de1d-4def-8c69-c142d2bd48be)

Only 13 FitBit users contributed data that had to do with their weight. At a quick glance, this line graph shows that the participating users maintained fairly consistent weights. Upon a closer look, most users only contributed a few data points. Only two users inputted multiple data entries to keep track of their weight fluctuations. 

### Time asleep to time in bed scatterplot

![time_asleep_time_in_bed](https://github.com/user-attachments/assets/41aa99c1-3576-4897-bf1f-363a018f05da)

The average total time asleep is 419 minutes, or about 7 hours, and the average total time in bed is 458.48 minutes, or 7.5 hours. The difference between the two is 39.5 minutes. In this amount of time that is spent awake, the data cannot determine why FitBit users take so long to fall asleep on average. The scatterplot shows a positive correlation between the total time asleep and the total time spent in bed. As shown, a majority of the data points are clustered around the intersection of the average lines in the scatterplot, which shows that most FitBit users were getting 7 hours of sleep while wearing their activity tracking device. Very few data points were less than 200 minutes of sleep and only four outliers exceeded 950 minutes (15.83 hours) of total time in bed.

The provided data also cannot tell us any underlying medical conditions that may be impacting quality of sleep, such as insomnia and untreated sleep apnea. For FitBit users that spent an excessive amount of time asleep, such as the user that got 800 minutes of sleep, it is unknown what factors in their life (age, employment, health, etc.) influenced this.

### Sleep per day of week column chart

![sleep_per_day_of_week](https://github.com/user-attachments/assets/66b211ec-5af1-4b08-95c6-2fd04b667ccd)

According to the column chart, FitBit users got the most amount of sleep on Wednesday nights at 16.693%, followed by Tuesday nights at 15.3%, and the third most well-rested night was Thursday at 14.944%. Monday night received the least amount of total sleep at 11.228%.</details> 

<details>
<summary> 6. ACT</summary>

The goal of this case study is to answer key business questions that can help provide the best recommendation for Bellabest marketing strategy. 

**1. What are some trends in smart device usage?**

a. While analyzing my datasets, I noticed multiple trends within the `combined_activity` data table. The biggest trend I noticed was that FitBit users predominately used their devices as a means to track the number of steps they took. This in turn tracked the total distance they walked/ran in a day. The next trend in smart device usage was to track activity level. As mentioned, 82% of users were sedentary, 15.3% were lightly active, 1.6% were very active, and 1.1% were fairly active. 

b. To break that down into minutes (hours): total sedentary time is 992.5 minutes (16.5 hours), total lightly active minutes is 185.4 (3.09 hours), total very active minutes is 19.68, and total fairly active minutes is 13.4.

c. Another passive trend that I noticed within this dataset was calorie tracking. Whatever device FitBit users wear (information we are not given), it tracks calorie output of said user. There were multiple daily inputs where total steps, total distance, and data about the various activity levels were a null value, but there was still a caloric value of, for example, 1347. It is possible that the watch has died, but will still log a base number of calories burned for the user. 

d. Visualizations helped identify trends as well. I was surprised that Tuesday was the day of the week where FitBit users were walking the most. Saturday came in second, whereas Sunday is the day that FitBit users chose to take the least amount of steps. 

e. Only 13 FitBit users submitted their weight data, which does not give much insight into smart device usage trends. From the limited data that I worked with, it appears as if the participating FitBit users logged their weight primarily to ensure that they were simply maintaining their weight. Beginning and ending weights were within a 3 pound difference, which is a normal daily weight fluctuation for someone.

f. Tracking sleep was also one of the main trends with smart device usage. The data showed that the participating FitBit users got an average of about 7 hours of sleep and spent a total average time of 7.5 hours in bed. These FitBit users get an appropriate amount of sleep.

g. Of course, sleep fluctuates from night to night. My column chart visualization showed that FitBit users got the most sleep on Wednesday nights, second was Tuesday night, and Monday night provided the least amount of sleep to users. 

**2. How could these trends apply to Bellabeat customers?**

a. Health and fitness is the primary goal of anyone that decides to invest in a fitness tracking device, such as a watch.

b. Bellabeat customers would still follow the same smart device usage trends of step counter/distance, calories, activity level, weight, and sleep tracking being the primary focuses of users.

c. It is uncertain if Bellabeat users would be as sedentary as the participating FitBit users were.

**3. How could these trends help influence Bellabeat marketing strategy?**

a. There are many ways that the Bellabeat marketing team can use their devices to promote a healthy lifestyle to their users. To help their users avoid a sedentary lifestyle, allow the device to sense when the user has been inactive for a given amount of time and to send the user an alert to remind them to move. 

b. To avoid interruption in data tracking, an alert can be sent to the user letting them know that their device is about to die and needs to be charged. Maybe a low battery icon could replace the primary display until an adequate charge is achieved. 

c. Alerts could also be more reward based. For example, if a user accomplishes a minimum of 30 fairly to very active minutes they could receive an alert saying they received a 'trophy'. Positive encouragement is important. 

d. A cooresponding smartphone app would be greatly beneficial to Bellabeat users as well. It would allow Bellabeat users to customize their experience. They can control what their primary focus is. Is it total number of steps? Is it total distance? Is it calories burned? Is is sleep? Is it water intake? Is it nutrition? 

e. This app could also allow for menstrual and menstrual symptom tracking, a food diary section, an exercise log that is broken down into categories and allows users to select what they did and for how long, but also provides helpful resouces, such as stress relief, nutrition, recipes, etc.

f. To account for potential customers that may be wheelchair bound, possibly incorporate a toggle switch in the app settings to disable step counting. Instead, create a way to replace a step counter with an odometer. This would allow for more inclusion and would reach a wider population who still care about health and fitness. 

g. To help encourage healthy sleeping habits, providing a visual graph of sleeping start and end times would be very beneficial information for users. Also, sending users an alert that it is approaching bedtime may be a helpful way to help maintain or begin healthy sleeping habits. Another helpful tool within the Bellabeat app could be to introduce a sleep calculator, which can allow the user to input when they need to wake up and the output will be recommended times they should fall asleep to achieve at least one REM cycle.</details> 
