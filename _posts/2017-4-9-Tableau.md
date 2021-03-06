---
layout: post
title: Big Trouble in Little Chinatown
published: true
---

My introduction to Tableau and the horror that is Restaurant Inspection Health Grades

My third and final project at General Assembly didnt come with a topic but instead we were to look for our own data, get it approved and basically figure out what we want to do with it. It was quite an interesting experience seeing all the data that was publically available on the net and finding out what interested me. Originally I wanted to do AirBNB again except with the Tokyo market since I've used AirBNB in Tokyo but the data was either insufficient or was not publically available which led me to the frustration of not finding the data I wanted. Ultimately at the recommendation of the instructors, I decided to browse New York City's [own publically available database](https://opendata.cityofnewyork.us/) for interesting topics. Seeing our city full of looming skyscrapers deconstructed down into spreadsheets was very enjoyable. From transportation, to schools, to business and everything about zoning regulation you never cared about, it was all available at the click of my mouse. I settled on the thing thats been staring at me my entire life, which were all the restaurants with all the B Sanitary Inspection grades near my house. How bad is a B exactly and what does it mean? Does the city have a problem with Bs or is it certain areas or just certain restaurants? All these questions suddenly rushed into my head as I downloaded the data provided by the DOHMH in their New York City Restaurant Inspection Results report.

<p align="center">
<img src="http://newyork.seriouseats.com/images/20100728sanitation.jpg"/>
</p>

Sanitary Inspection Results are basically like having a driving test except you're driving a hotdog instead of a car. You start at zero points and as you gaint points as you fail to make a right turn into proper temperature control. If you rack up more than thirteen points, you get a B, and if you get more than twenty seven you get a C. Failure to get an A is essentially not passing and you are immediately signed up for another inspection at which point you either get an A or you are allowed to stick with the grade that you received, whether it be a B or a C. So it turns out when you see a B graded restaurant, they actually failed at least two inspections. Health violations are also similar to driving tests in that there are minor and major violations. Minor violations are things like not having food stored at the right temperature while major violations involves things like pest infestations or things that immediately endanger customers. Enough major violations can get you shutdown immediately until it has been resolved. As I read these all these rules for inspection the questions I had previously came storming back in. Just what does the map of health inspections look like and can I somehow visualize it?

Fortunately the tool we learned before this project was Tableau, a visualizing software which did exactly everything I wanted for this project. Tableau allows the instaneous generating of graphs and visualizations through simple drag and drops which were made interactive by allowing on the spot tweaking that were reflected immediately in the graphs. An amazing piece of software which made me dread all the time I spent making graphs and tables in Excel beforehand. Tableau then allows users to present them through its storybook mode which I like to think of as powerpoint slideshow but actually good or in expansive dashboards.

<img src="http://i.imgur.com/CAMqP3B.jpg">

Of course before I could inject my data into Tableau, I ran to run through the usual gauntlet of cleaning and sorting through the data I had obtained for this project and boy was it an endeavor. Fortunately the NY government does a pretty good job of keeping their sheets clean, the problem was loading the sheet itself was troublesome since it recorded every violation of every restaurant in the city for the last half decade. Since I had to narrow down my focus, I chose Chinese restaurants since I frequent them the most of course because I'm Chinese and that they're not exactly the cleanest of places. The goal of my analysis from this point on was to then find out if the scores were improving over time, and if not, what factors were preventing them from improving.

It was during my attempts at aggregating the data in SQL that I experienced my first greatest challenge that kept tripping me up all night. Scores for restaurants were recorded in their point form and not their letter form so I wanted to see the percent distribution of letters throughout the boroughs. You would think it would be as simple as just making a case statement for when the scores were above fourteen or above twenty eight but the restaurants were recorded with all their violations too. So a restaurant might have a fifteen score but be recorded five or six times for one inspection. This skewed the averages considerably and threw me off at how I would condense these violations to single inspections. Surprisingly, it wasnt because of my inability to aggregate what I was looking for, but the fact that I my approach was wrong but I was too deep to abandon what I had done. It was only when I decided to start from scratch did I realize that I could just consolidate the inspections by simply using the inspection dates. The lesson I learned here was that sometimes overworking isnt working at all and sometimes you just need to take a breather. 

After inserting the data into Tableau, I get this wonderful geomap that plots out health scores by Zipcode. The are multiple toggeable settings for it such as year and critera in the Tableau file but you'll have to live with a screenshot of the pdf.

<p align="center">
<img src="http://i.imgur.com/OxG5VQg.png">
</p>

To be continued!

For the pdf of my full presentation, click [here](https://github.com/bluufish/Restaurant-Nightmare/blob/master/Final%20Project%203%20Simon%20Chan%20Data%20Analysis.pdf)
