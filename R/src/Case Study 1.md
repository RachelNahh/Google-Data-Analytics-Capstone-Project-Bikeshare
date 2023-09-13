Untitled
================

### Background information

Since 2016, Cyclistic has launched a successful bike-share programme.
Since then, the program has grown to a fleet of 5824 bicycles into a
network of 692 stations across Chicago. Until now, Cyclistic’s approach
has been relied on the flexibility of its pricing plans: single-ride
passes, full-day passes, and annual memberships. The management of
Cyclistic would like to improve overall market share of the bike-sharing
scene. The finance analysts have concluded that annual members are much
more profitable than casual riders. Rather than creating a marketing
campaign that targets all-new customers, there is a good chance to
convert casual riders into members. The marketing analyst team now needs
to better understand how annual members and casual riders differ, in
order to create effective marketing strategies.

This report is based on analysis of Cyclistic rider data for the past
year (August 2021 - July 2022).

### The Objective

The objective of this report is to look at past year Cyclistic rider
data to understand usage differences between member riders and casual
riders and thereafter develop effective marketing strategy.

### The Analysis

The table below lists the variables available for analysis.

┌────────────────────┬─────────────────────────┬─────────────────────────┐
│ Variable name │ Description │ Data available │
├────────────────────┼─────────────────────────┼─────────────────────────┤
│ ride_id │ random ride ID number, │ check data duplication │ │ │ not
tied to customer │ │ │ │ details │ │
├────────────────────┼─────────────────────────┼─────────────────────────┤
│ rideable_type │ bike type: │ differentiate bike type │ │ │
Classic/Docked/Electric │ usage │
├────────────────────┼─────────────────────────┼─────────────────────────┤
│ started_at │ start date time │ calculate ride │ │ │ │ duration,
ridership by │ ├────────────────────┼─────────────────────────┤ time/day
of the │ │ ended_at │ end date time │ week/month │ │ │ │ │
├────────────────────┼─────────────────────────┼─────────────────────────┤
│ start_station_name │ start station name │ identify stations with │
├────────────────────┼─────────────────────────┤ high usage │ │
start_station_id │ start station ID │ │
├────────────────────┼─────────────────────────┤ │ │ end_station_name │
end station name │ │ ├────────────────────┼─────────────────────────┤ │
│ end_station_id │ end station ID │ │
├────────────────────┼─────────────────────────┤ │ │ start_lat │ start
station latitude │ │ ├────────────────────┼─────────────────────────┤ │
│ start_lng │ start station longitude │ │
├────────────────────┼─────────────────────────┤ │ │ end_lat │ end
station latitude │ │ ├────────────────────┼─────────────────────────┤ │
│ end_lng │ end station longtidue │ │
├────────────────────┼─────────────────────────┼─────────────────────────┤
│ member_casual │ member type: │ differentiate member │ │ │
Member/Casual │ type │
└────────────────────┴─────────────────────────┴─────────────────────────┘

Column names: Variable, Description, Data

#### 1. Ridership Breakdown

##### 1.1 Ridership breakdown by rider type

![](Untitled_files/figure-gfm/pie%20chart%20of%20ridership%20rider%20type%20breakdown-1.png)<!-- -->

Based on the past year data, currently the Members make up 57% of the
riders, while Casual riders constitutes 43%.

 

##### 1.2 Bike type breakdown

<img src="Untitled_files/figure-gfm/biketype chart-1.png" width="50%" /><img src="Untitled_files/figure-gfm/biketype chart-2.png" width="50%" />

The choice of bikes between the 2 rider groups are similar. There were
slightly more take up for classic bikes (~50% range) compared to
electric bikes (~40% range) for both groups.  

<font size="1"> ^Casual riders have 3 categories of bike: Docked bike,
Classic bike and Electric bike. Docked bike and classic bike have been
grouped together, to simplify comparison across Member and Causal
riders.</font>

 

 

#### 2. Ridership breakdown by duration

<img src="Untitled_files/figure-gfm/rider duration pie chart-1.png" width="50%" /><img src="Untitled_files/figure-gfm/rider duration pie chart-2.png" width="50%" />

Duration breakdown for Member riders show 54% of Member riders cycle for
less than 10 minutes, 28% cycle between 10 to 20 minutes. Short commute
of up to 20 minutes total to 82% of Member ridership. This suggests that
Member riders use the bike mainly for short commute.

There is an equal mix of Casual riders riding for less than 10 minutes
(32%) and between 10 to 20 minutes (31%). The next 2 duration categories
“between 20 to 30 minutes” and “30 minutes up to an hour” makes up 15%
and 14% of Casual rider ridership. More Casual riders are riding for a
longer duration compared to Member riders, indicating that there are
more Causal riders cycle for leisure.

 

#### 3. Ridership grouped by Day of the Week

![](Untitled_files/figure-gfm/ridership%20breakdown%20by%20day%20chart-1.png)<!-- -->

The ridership of Member riders are generally more consistent throughout
the week compared to Casual riders, with more riders using the bike
during weekdays. Casual riders’ bike usage is significantly higher
during weekends.

 

#### 4. Ridership breakdown by Month

![](Untitled_files/figure-gfm/ridership%20breakdown%20by%20month%20chart-1.png)<!-- -->

 

Warmer months such as August to October 2021 and May to July 2022 have
higher higher ridership compared to colder months like Noverber 2021 to
April 2022, which is in line with the general trend
worldwide<sup>1</sup>. A steeper decrease is observed in ridership for
Casual riders when the climate transits to the colder months.

 

#### 5. Ridership breakdown by Time

![](Untitled_files/figure-gfm/ridership%20breakdown%20by%20time%20chart-1.png)<!-- -->
 

The Member riders dataset has 3 peak period that stands out:

- 7 - 8am, which coincides with the morning rush hour
- 12pm, the lunch hour
- 3-7pm , which overlaps with the evening rush hours

Member riders are using the bike for short commute to-and-fro
work/school and during lunch hour.

The Casual riders dataset shows ridership increases through the day from
10 am on and peak at 5pm, suggesting that Casual riders are using the
bike for leisure and/or running errands.

 

#### 6. Summary of Rider Behaviour

Below is a table that summarises and compares rider behaviour:

┌──────────────────────────────────────┬──────────────────────────────────────┐
│ Member │ Casual │
├──────────────────────────────────────┼──────────────────────────────────────┤
│ 57% of riders are Members. 82% of │ 32% of riders cycle for \<10
minutes, │ │ members uses the bike for 20 minutes │ 31% ride for 10~20
minutes │ │ or less │ → a mix of short and medium duration │ │ → short
commute │ commute │
├──────────────────────────────────────┼──────────────────────────────────────┤
│ Highest ridership occur during │ Highest ridership occur during │ │
weekdays │ weekends │ │ → mainly for commute to work/school │ → mainly
for leisure │
├──────────────────────────────────────┼──────────────────────────────────────┤
│ 3 peak period for rides: 7-8am, │ Ridership increases steadily from │
│ 12pm, 3-7pm │ 10am and peak at 5pm │ │ → commute to-and-fro │ →
running errands/possibly tourist │ │ workplace/school and lunch │ │
└──────────────────────────────────────┴──────────────────────────────────────┘

Column names: Member, Casual  

#### Limitations

Below is a table that summarises limitations of the dataset:

┌─────────────────────────┬─────────────────────────┬─────────────────────────┐
│ Limitation │ Consequence │ Action │
├─────────────────────────┼─────────────────────────┼─────────────────────────┤
│ Data-privacy prohibits │ -Unable to determine if │ Additional data │ │
the team from using │ users are residents or │ required to enable the │
│ riders’ personally │ tourists │ team to develop better │ │
identifiable │ -Unable to identify │ targeted strategies │ │ information
│ multiple trips on the │ │ │ │ same day │ │
├─────────────────────────┼─────────────────────────┼─────────────────────────┤
│ 2.2% of the data │ Unable to determine the │ Additional data │ │
contained rides with │ cause of these rides, │ required to ascertain │ │
less than 1 minute │ thus unable to rectify. │ faulty bikes. For this │
│ duration, which equates │ │ analysis, data with │ │ to a travel
distance of │ │ ride duration under 1 │ │ ~0.3km -\> possibly │ │ minute
has been │ │ faulty bikes? │ │ excluded │
└─────────────────────────┴─────────────────────────┴─────────────────────────┘

Column names: Limitation, Consequence, Action  

### Recommendation

As a refresher, the finance team has concluded that annual members are
much more profitable than casual riders. Thus the management are looking
to maximise the number of annual memberships.

Before designing a new marketing strategy to convert casual riders to
annual members, we need to understand the bike usage behaviour
difference between the 2 groups. Through the analysis, we have learnt
that Member riders use the bike mainly for daily commute: weekday rides,
duration within 10 minutes, peak period of morning rush hours, lunch
hour and evening rush hours. Casual riders mainly use the bike for
leisure purpose or running errands: weekend rides, duration of up to 20
minutes, riding between time period of 10am to evening. It has been
determined that the bike usage pattern of Member riders and Casual
riders are different. Therefore, it might take more than marketing
strategies to entice Casual riders to commit to subscription.

Firstly, there is a need to take a closer look at Casual riders. There
is a need to differentiate Casual riders who resides in Chicago from
Tourists, as it is plausible for residents to commit to an annual
subscription. As the frequency of Casual riders riding the bikes are
lower than Member riders, the existing annual subscription package may
be deemed as uneconomical for their usage. A suggestion would be to
devise a new shorter ride subscription pass for these Casual riders.
Another group of people who may use the Single Ride options are the
Tourists. A subscription plan may not be enticing to Tourist, it might
be worthwhile to explore multi-day short commute pass for Tourist. An
important next step would be to conduct a survey to hear directly from
the users themselves: what would entice them to commit to subscription
plan, what features do they want, how can we improve the user
experience, in order to better understand their needs.

### Summary

┌─────────────────────────┬─────────────────────────┬─────────────────────────┐
│ Objective │ Analysis │ Recommendation │
├─────────────────────────┼─────────────────────────┼─────────────────────────┤
│ \* Understand usage │ \* Member riders use the │ \* Deeper analysis on
│ │ differences between │ bike mainly for daily │ Casual riders
required: │ │ Member riders and │ commute │ \* Resident Casual │ │
Casual riders │ \* Casual riders use the │ riders -\> devise new │ │ \*
Develop effective │ bike mainly for │ shorter ride │ │ marketing
strategy │ leisure/running errands │ subscription │ │ │ │ pass/weekend │
│ │ │ subscription pass │ │ │ │ \* Tourist Casual riders │ │ │ │ -\>
multi-day pass │ │ │ │ \* Conduct survey: │ │ │ │ \* What would entice │
│ │ │ Casual riders to commit │ │ │ │ to subscription? │
└─────────────────────────┴─────────────────────────┴─────────────────────────┘

Column names: Objective, Analysis, Recommendation
