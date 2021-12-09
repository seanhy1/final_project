# final_project: Show changes over time with Mapbox GL JS

***Project title:***
Visualizing trends over change of time with collisions that have occurred in Seattle (2014-2020)


***Project description:***
This web application is designed to display a map that shows data change over time using Mapbox GL JS. The source data that I had decided to work with for my project is from NYC Seattle GeoData in which contains more than 235,000 records of all types of collisions which have occurred since 2004 to present day. The data was provided by the Seattle Police Department and recorded by Traffic Records. As I was filtering the original GeoJSON file that I had initially downloaded, I realized that the process was taking much longer than needed (QGIS desktop application wouldn’t respond after calculating one field for a whole column of data entries). This procedure was quite time consuming, and created a lot of frustration because of the minor setbacks that came along with wrangling the data in accordance to how I wanted to design my web application. Thus, rather than displaying all data records dating back to the year 2004, I decided to advance the time gap by ten years, making the data much smaller in download size. This also enhanced the performance speed of my application when configuring user input for filtering purposes. Furthermore, because the year 2021 is still in progress, I decided to declare the max range as 2020 in order for the web application to properly display all data when inputs are interacted with.

***Project goal (such as, what is the message you want to deliver through your project?):***
The goal of this project is to illustrate the trends in collisions occurring during the change of months and years. When carefully examining the various visualizations based on numerous combinations of filtering through the inputs provided on the application’s user interface, users can discern where exactly it is (geographically speaking) incidents occur the most, and for which seasons have had the most and least amount of collisions. The importance of this web application is to create a stronger awareness of collisions occurring in the greater Seattle area. As a Washingtonian who has resided outside of Seattle until attending the University of Washington, I have grown a stronger understanding of the lack of proper driving that happens within Seattle. Although this application does not necessarily give us a strong indication as to why such association between poor driving capabilities and vehicles within the Greater Seattle area exist, it was worth taking a deeper look into by being able to filter collision data through the aspects of change over time. On a more personal scale, this project carries significance to me as recently one of my closest family friends has dealt with paralysis in their lower body from a car crash that occurred two years ago near UW’s campus. Given a platform to engage in an interactive web application, I wanted to honor them and dedicate my studies to prevent such grievances/pain for locals around the area in hopes that such work can ultimately be examined to best prepare drivers and their safety when putting themselves out on the road where many uncontrollable factors can lead to a potential collision. For this exact reason, this is also why the variable be observed over change in time is specifically injuries suffered through motor vehicle collisions.


***The application URL (not the repository url):***
http://127.0.0.1:5500/index.html

***Screenshots:***
![Alt text](/geog495_final_project/assets/seattle_collisions.png?raw=true)

***Main functions:***
Some of the main functions include:
- map.on('load', () => 
This callback function tells your browser to wait until the map is finished loading before trying to add new things to it. Any code that adds layers should be inside of this callback function. 
- filterYear, filterMonth, filterDay
These functions are programmed to filter the fields found within the dataset. They are all hard-coded so that the selected fields (‘YEAR’, ‘MONTH’, and ‘DAY’) are equal or not equal to that exact value
(i.e.let filterYear = ['==', ['number', ['get', 'YEAR']], 2021];). It is worth noting that because the values within field ‘DAY’ are not string values, I decided not to hardcode a ‘placeholder’ value, but instead used the integer value 7. This is because the int array for days of the week start from 0 and end at 6. Thus, because 7 is never reached, it was a reasonable replacement for the ‘placeholder’ string value. 

***Data sources:***
The webpage from which I had obtained the dataset used for my web application comes from Seattle GeoData. The direct link can be found on my web application, but can also be accessed via this hyperlink: https://data-seattlecitygis.opendata.arcgis.com/datasets/5b5c745e0f1f48e7a53acec63a0022ab/explore?location=47.659640%2C-122.465023%2C12.65

***Applied libraries (e.g., mapbox gl js) and Web Services (e.g., github, basemap) in use:***
The applied library in use for the purpose of this project is Mapbox GL JS and the web service used in order to publicly publish my project was through GitHub. 

***Other things that are necessary to inform the audience:***
The template from this project directly comes from the material taught through Module 09 and the tutorial can be accessed here: https://docs.mapbox.com/help/tutorials/show-changes-over-time/#finished-product

***Acknowledgment:***

- Bo Zhao: taught concepts which I was able to utilize for the final project
- Steven Bao: responding to my emails efficiently and answering all my questions I had when errors occurred in my code
- Mapbox: providing their template tutorial
- Seattle GeoData: providing reliable and public dataset
