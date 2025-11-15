# Case Study - Understanding Smart Device Usage to Guide Marketing Strategy

Google Data Analytics Capstone – Bellabeat Smart Device Case Study (R + Tableau) - 
Make data driven desicions to improve the marketing strategy of the welness technology company Bellabeat

### ▶️ Open the full Notebook in Google Colab  
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/CarlosKunze/Case-Study---Smart-Device-Fitness-Data-Analysis/blob/main/notebook/CaseStudyBellabeat.ipynb)

### 📊 Open the Interactive Tableau Dashboard  
[![Open Tableau Dashboard](https://img.shields.io/badge/Tableau-View%20Dashboard-blue?logo=tableau)](https://public.tableau.com/app/profile/jan.carlos.kunze/viz/CaseStudy_17627063383140/Dashboard12)

## 📌 Overview  
Bellabeat wants to understand how users engage with smart wellness devices to improve their marketing strategy.  
This case study uses Fitbit Fitness Tracker data to analyze user behavior patterns and identify opportunities for  
Bellabeat’s product positioning, messaging, and customer engagement.

## 🧩 Process
1. **Ask** - Defined the the Business Task and Formulated some guiding questions. 
2. **Prepare** – Loaded and explored Fitbit data (`dailyActivity`, `sleepDay`, `calories`, `intensities`).  
3. **Process** – Cleaned data, removed duplicates, converted dates, merged datasets.  
4. **Analyze** – Identified trends by weekday, hour, and activity intensity.  
5. **Share** – Created Tableau dashboard and summarized insights.  
6. **Act** – Formulated marketing recommendations for Bellabeat.

## 🛠 Tools  
- **R (tidyverse, lubridate, janitor)** – data cleanup & processing  
- **Google Colab** – execution environment ("runtime type" R)  
- **Tableau Public** – visualization dashboard  
- **GitHub** – project versioning & documentation 

## 📊 Summary 
**Business Task and guiding Questions**
The goal of this analysis is to identify trends in smart device usage using publicly available FitBit fitness tracker data.
By understanding how users track their daily activity, sleep, and calorie expenditure, we aim to uncover patterns that can inform Bellabeat’s marketing strategy

**Some questions that could be answered with the data could be:**

1.  When are users most active during the day or week?
2.  How much sleep do users get, and when?
3. What’s the relationship between steps, calories, activity level, and sleep?
4. Are users more active on weekdays or weekends?
5. What times or habits correlate with better consistency?
6. What are the seasonal or monthly activity trends?

**These questions could help us with our marketing strategy in the following way:**

1. Send motivational app notifications before high-activity hours. Schedule social media posts or email campaigns during users’ most active hours.
2. Promote sleep-related products (like the "Leaf" product).
3. Design targeted campaigns for each profile: motivational messages for low-activity users, mindfulness content for sleep-deprived users, or performance-focused challenges for high-activity users.
4. Tailor marketing campaigns for weekends and weekdays.
5. Reward consistent users with loyalty badges; send reminders to less consistent users to re-engage them with Bellabeat’s app or membership program.
6. Seasonal Campaigns—Launch “Winter Wellness” programs or discounts during low-activity months. Promote app challenges in spring/summer when users are more active.

**Insights and possible Marketing Strategies**

![Dashboard Preview](visuals/Bellabeat_Case_Study_Dashboard.png)

Some insights of our average user: Average user weighs 73,4 kg, has an BMI of 25,7 sleeps 7 hours, walks 6500 steps a day and burns 2190 kcal per day. 
The standard derivations are very high across all analyzed parameters. This is partly due to the very small sample amount (~30). The very high standard derivations for the activity types (fairly active, very active, etc...) and the steps could also reveal the fact that there generally are different user types. I.e., some users tend to prefer "very active" activity at all times they get engaged in activity, while others tend to prefer light activity. This again means that the different user types continue behaving and using the smart device equipment for different purposes.

First, I identified the average user. As seen in the first pie chart, the average user spends most of his time sedentary. When physical activity is performed, light activity (could be yoga, jogging etc…) is preferred. Over the week, there are no clear patterns in activity engagement. Only for "Fairly Active" minutes spent, there is a peak on Friday. This could mean users like to engage in activities like jogging or other types of sport after work before the weekend. For the average steps walked, and average calories burned, we can see a sudden decrease on Tuesdays. In addition, we can't identify significant differences for these parameters during the week vs. on the weekend.

To intensify the analysis when users tend to engage in physical activity, I analyzed the calorie consumption per hour to look for patterns at which time on each day users tend to get active. The heatmap shows us in red when users are most active. Here we can see tendencies that during the week, users tend to engage in activities between 3–7 pm. This could show us for example behavior patterns where users engage in sports after work. On the weekend, the time slot of physical engagement shifts slightly to earlier hours.

Before analyzing the sleeping habits, it is important to keep in mind that we have data of fewer users and therefore a high standard derivation of our measurements (to demostrate more analysis and insights we ignore this fact for now). For the data that we have, the sleep is evenly distributed over the whole week, with Sunday being the day when users get most sleep and Thursday the day when they get less. However, the differences are not significant. When analyzing the sleep distribution during the day we can see some habits of users to take naps after work (between 3–7 pm) especially on Tuesdays, Thursdays and Fridays.

Ultimately, we plotted the total daily steps against the burned calories. The US National Institute of health (NIH) recommends about 8000 steps per day as it is linked with a reduced risk of death. Looking at our diagram and analyzing the average steps per weekday, we can clearly see that most of our users do not achieve this number. Furthermore, we see a statistical significant linear correlation (p< 0,0001) between steps and calories burned. However, it should be noted that the measurement points are widely distributed from our straight line. The R² value of 0.30 suggests that daily steps account for roughly one-third of the variation in calories burned. This indicates a noticeable but not strong linear relationship.

## 🎨 Marketing Strategy

Due to the small amount of data available, these are rather rough recommendations or ideas or areas in which further resources could be invested. We have throughout the low statistical significance. However, as this is a case study, we are still providing strategy recommendations based the insights we could uncover with the available data.

The following advice now counts for the average user of our 30 participants. Generally I would recommend separating the users into "activity engagement" types and tailor marketing for each type (e.g. for active users --> performance based, for lightly active users --> mindful based marketing)

***1. Understanding the user:***

The average smart device user spends 83 % percent of his time in sedentary position and when sport/ activity is done most users prefer light activity.

***Marketing implication***

Bellabeat’s messaging should focus on balance and well-being, not athletic performance.

* Promote Bellabeat products as tools for daily motivation (e.g. stand up in between sedentary time), mindfulness, and gentle activity tracking.

* Example campaigns:
* “Small steps toward a healthier you.”
* Challenges and rewards to achieve daily goals

* Seeing a small peak in fairly intensive activity engagement on Fridays could be interesting to continue investigating. For example user types could be categorized and for said "fairly active" users push up notifications or challenges could be sent on Friday afternoons --> more research needs to be done here.

***2. Time marketing hours:***

Our heatmap (calories) shows us that the most active parts of the day fall in the afternoon (probably after work)

***Marketing implication:***

* Schedule app notifications or social media posts in these time windows to maximize visibility and gain attention.
* Collaborate with fitness influencers to post at those high-engagement hours.

***3. Time marketing days:***

We see a drop in daily steps and burned calories on Tuesdays (We should dig deeper into why !). For know some marketing insights could be:

* Promote Tuesdays as recovery days; sending mindful messages or reminders that recovery is necessary for consistency
* Or offer special motivation like: “You burned 20% fewer calories on weekends — take a mindful walk today!”

***4. Sleep patterns and marketing for sleep related products***

The sleep per day is pretty evenly distributed over the week and on average users get between 6-8 hours of sleep.

***Marketing implication***

* Here we need to dig deeper to isolate users with worse sleeping patterns and then offer personalized advertisement or offer generalized advertisement to really achieve 8 hours + of sleep. This way we can promote Bellabeat’s sleep and recovery features (Time watch, Leaf tracker).
E.g.
Create awareness campaigns about how better sleep improves energy and focus.
Example: “Better rest, better balance — track your sleep with Bellabeat.”

***5. Daily steps***

The scatter plot shows a clear positive relationship: more steps → more calories burned. Even moderate increases in activity can significantly impact calorie expenditure.

***Marketing implication***

Encourage users to reach small, achievable daily goals (also see 1.).

Integrate gamified challenges in the Bellabeat app (e.g., “Take 1,000 extra steps today”).

Reinforce Bellabeat’s brand as a supportive wellness partner, not a performance tracker.


***Further analysis***

Some questions from the Ask phase could not be answered due to the small amount of data. Some more interesting open questions could be:

Are there seasonal trends?
This way seasonal campaigns could be tailored.
--> More data (at least over 1 year) is needed

Which behavior creates patterns?
Which user type (very active, lightly active mindful) are most consistent?
Promote/ reward consistent users
More data and categorization of users is needed.

Gain more data on sleep to promote sleep related products (like "Leaf" and "Time" products)

Gather additional data on drinking/ hydration behavior to promote "Spring" (Bellabeat's own water bottle) product

***Summary***

The Fitbit dataset reveals that users are moderately active, routine-driven, and focused on balanced wellness rather than performance.
This positions Bellabeat perfectly to market its products as lifestyle companions — supporting consistent movement, sleep, hydration, and mindfulness for long-term well-being.



## 🧠 Skills Demonstrated
Data cleaning • R programming • Exploratory analysis • Data visualization • Business insight generation
