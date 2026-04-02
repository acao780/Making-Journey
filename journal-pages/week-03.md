---
layout: default
---

# Week 03

[← Back to Home](../index.md)

# Documentation 
## Activity 1: 

I started the week by using special commands in the computer terminal to get information from the internet without using a regular website. I practiced getting the weather for different cities like Tokyo and Auckland and I even learned how to see the weather in different languages or check the phase of the moon. I also used the terminal to find synonyms for words like dark and white which showed me how the computer can quickly pull data from big libraries online. These tasks helped me understand that data is everywhere and we can ask the computer to find it for us using simple text instructions.

## Images & Media
Following the guides at the first time:
![in class task](../assets/week-03/curl_wttr_in.png)

![in class task](../assets/week-03/curl_ascii.live:forest.png)

![in class task](../assets/week-03/curl_ascii.live:parrot.png)

![in class task](../assets/week-03/tokyo.png)

### Get the weather for a location using its GPS coordinates

![in class task](../assets/week-03/auckland_weather.png)

### Get the weather in a different language

![in class task](../assets/week-03/chinese_version.png)

### Get the current moon phase
![in class task](../assets/week-03/moon.png)

### Look up the synonyms and antonyms of a word

![in class task](../assets/week-03/dark.png)
![in class task](../assets/week-03/white.png)

### Find something else in the documentation that we haven't covered

![in class task](../assets/week-03/snow.png)


## Activity 2: Weather Visualisation

For this activity I used a coding tool called p5.js to turn live weather data into shapes and colors on the screen. I changed the code to look at the weather in Iceland instead of Auckland and I saw how the shapes moved and changed size based on the wind and temperature. 

1. Changing Location (Latitude and Longitude)

To change the city, I modify the url string. In this example, I’ve switched the coordinates from Auckland to Reykjavík, Iceland (64.14 ∘N,−21.90 ∘W), this is one of my favourite city. The numerical values for latitude and longitude in the url variable were updated. This forces the API to return data for a different geographic point, which would immediately change the values of your variables like temp or wind.
![in class task](../assets/week-03/image1.png)

2. Use the data to control different visual properties: colour, position, size, number of shapes.

I have updated the draw() function so that wind controls position, temperature controls size, and humidity controls color. I replaced static numbers (like 23.5 * 10 or 0) with your weather variables (temp, wind). Now the shapes move and grow based on the live data.
![in class task](../assets/week-03/image2.png)

3. Add more weather variables from the Open-Meteo documentationLinks to an external site. to the API URL.

I add is_day to the URL. This variable returns 1 for day and 0 for night. I updated the url to request is_day and used an if/else statement in draw() to change the background style based on that new variable.
![in class task](../assets/week-03/image3.png)
![in class task](../assets/week-03/image33.png)

4. Try using random() or noise() alongside or instead of the live data.
   
I use the wind speed to determine how much the circle "shakes" or "jitters." I added the random() function. If the wind is high, the "shake" range is larger, making the circle look like it is vibrating in the wind.
![in class task](../assets/week-03/image4.png)
   
5. Use vibe coding to try something more ambitious.
 
This version changes the whole "mood" by drawing different scenes based on the temperature.
Instead of just drawing shapes, the code now chooses an entire "visual theme" based on a data threshold (20 degrees). This makes the code feel more "aware" of the environment.

![in class task](../assets/week-03/image5_record.mp4)

6. Use print() in the console to check the range and scale of values before trying to visualise them.
 ![in class task](../assets/week-03/image6.png)  

### Activity 3: Design and Execute a Data Protocol

I created a "Data Protocol". The source was the live wind speed in Auckland from the Open-Meteo website. I decided on a Frequency of checking the numbers every 60 seconds. The Mapping rule was to draw one blue diagonal line for every 1 km/h of wind speed. When i swapped the rules with another group, they followed the instructions well, but they were surprised by how many lines they had to draw when the wind picked up. This experiment showed me that simple rules can turn live data into very busy and interesting art.

 ![in class task](../assets/week-04/week4_image.png)  
 
 ![in class task](../assets/week-04/week4_image2.png)  


## Live Moon Phase Visualisation

### Introduction
Shutterstock
People have looked at the moon for a very long time because it helps us understand the tides and the passing of days while also inspiring many old stories. Even though we see the moon almost every night many people do not really know which phase it is in or how the cycle of the moon works. This project is called the Live Moon Phase Visualisation and it uses math to create a digital picture of the moon that changes in real time to show exactly what is happening in the sky. By using computer code to show the current phase of the moon we can turn complicated numbers into a simple and beautiful experience that helps people feel more connected to the world around them.

Instead of just showing a normal picture that stays the same, my project uses live data to show the moon as it changes in real time. The moon moves around the Earth in a very steady circle that takes about twenty-nine days and it goes through eight different shapes which include the new moon and the crescent and the full moon. My computer code takes the math from this cycle and turns it into things you can see like the size of the shadow or the bright light on the surface. This process takes boring numbers from a calendar and turns them into something solid and beautiful that helps people understand the sky.

This project is part of my digital work using a coding tool called p5.js to create a live moon that changes every second. While most pictures of the moon just stay the same, my project is different because it uses the real time and date to show exactly what the moon looks like in the sky right now. This makes the viewer feel more connected to the natural world because they can see the same rhythm that humans have followed for thousands of years.

# video and image

 ![in class task](../assets/week-03/week3_image.png)  
 
In my first version the moon was sitting on a plain black background which looked a bit empty. I decided to add many small white dots to the back of the screen to represent the stars in the night sky. I also made these stars move across the background so that the whole scene feels more alive and three-dimensional. This change helps the viewer feel like they are looking through a telescope at the real universe instead of just looking at a flat computer drawing.

 ![in class task](../assets/week-03/video1.mp4)  

When I first added the stars they were moving way too fast across the screen and it looked a bit distracting. For my second version I went back into the code and changed the speed to make them much slower. I realized that the stars in the sky should feel very calm and steady so I adjusted the numbers in my p5.js script. Now the background is peaceful and it does not take the attention away from the moon which is the most important part of my project.

 ![in class task](../assets/week-03/video2.mp4)  

In the third version I made the stars even better by giving them a gentle flashing effect. Instead of just staying the same brightness the stars now slowly get brighter and then dimmer which looks like the real twinkling we see at night. This makes the project feel very realistic and artistic because it captures the quiet beauty of the dark sky. By combining the slow movement with this soft twinkling I have created a space that feels deep and natural for my digital moon to live in.

 ![in class task](../assets/week-03/video3.mp4)  

## Reference
Tutorials Page: p5.js. (n.d.). Tutorials. Retrieved October 24, 2023, from https://p5js.org/tutorials/

Reference Page: p5.js. (n.d.). Reference. Retrieved October 24, 2023, from https://p5js.org/reference/

Free Dictionary API
MeetDeveloper. (2024). freeDictionaryAPI (Version 2.0.0) [Computer software]. GitHub. https://github.com/meetDeveloper/freeDictionaryAPI

curl
Stenberg, D., & curl contributors. (2024). curl (Version 8.7.1) [Computer software]. GitHub. https://github.com/curl/curl

ascii-live
Rawat, H. (2024). ascii-live [Computer software]. GitHub. https://github.com/hugomd/ascii-live

wttr.in
Chubin, I. (2024). wttr.in [Computer software]. GitHub. https://github.com/chubin/wttr.in

Open-Meteo Documentation
Open-Meteo. (n.d.). Open-Meteo weather API documentation. Retrieved April 2, 2026, from https://open-meteo.com/en/docs

## AI Usage Statement

I used vibe coding (Google Gemini) to help generate both iterations of the p5.js sketch. I described my requirements in plain language, reviewed the generated code, and made adjustments as needed.
