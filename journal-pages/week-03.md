---
layout: default
---

# Week 03

[← Back to Home](../index.md)

## Documentation 

*Include your documentation for the week. Devise your own structure of headings relevant to the required tasks and your process.*

## Images & Media
following the guides:
![in class task](../assets/week-03/curl_wttr_in.png)
![in class task](../assets/week-03/curl_ascii.live:forest.png)
![in class task](../assets/week-03/curl_ascii.live:parrot.png)
![in class task](../assets/week-03/tokyo.png)


Get the weather for a location using its GPS coordinates
![in class task](../assets/week-03/auckland_weather.png)

Get the weather in a different language
![in class task](../assets/week-03/chinese_version.png)

Get the current moon phase
![in class task](../assets/week-03/moon.png)

Look up the synonyms and antonyms of a word
![in class task](../assets/week-03/dark.png)
![in class task](../assets/week-03/white.png)

Find something else in the documentation that we haven't covered
![in class task](../assets/week-03/snow.png)


Activity 2: Weather Visualisation

Experiment with the sketch:
1. Changing Location (Latitude and Longitude)
To change the city, we modify the url string. In this example, I’ve switched the coordinates from Auckland to Reykjavík, Iceland (64.14 ∘N,−21.90 ∘W). The numerical values for latitude and longitude in the url variable were updated. This forces the API to return data for a different geographic point, which would immediately change the values of your variables like temp or wind.

2. Use the data to control different visual properties: colour, position, size, number of shapes.
I have updated the draw() function so that wind controls position, temperature controls size, and humidity controls color. I replaced static numbers (like 23.5 * 10 or 0) with your weather variables (temp, wind). Now the shapes move and grow based on the live data.


3. Add more weather variables from the Open-Meteo documentationLinks to an external site. to the API URL.
We will add is_day to the URL. This variable returns 1 for day and 0 for night. I updated the url to request is_day and used an if/else statement in draw() to change the background style based on that new variable.
   
4. Try using random() or noise() alongside or instead of the live data.
Let’s use the wind speed to determine how much the circle "shakes" or "jitters." I added the random() function. If the wind is high, the "shake" range is larger, making the circle look like it is vibrating in the wind.
   
5. Use vibe coding to try something more ambitious.
This version changes the whole "mood" by drawing different scenes based on the temperature.
Instead of just drawing shapes, the code now chooses an entire "visual theme" based on a data threshold (20 degrees). This makes the code feel more "aware" of the environment.

6. Use print() in the console to check the range and scale of values before trying to visualise them.

Activity 3: Design and Execute a Data Protocol

In pairs, design a data protocol: a set of rules for translating a live data source. This is the analogue equivalent of an API: a defined set of rules for requesting and receiving data.

Your protocol must specify:

Source: what live data to observe (e.g. sounds in the room, a live transport tracker on your phone)
Frequency: how often to check (e.g. every 10 seconds, every minute)
Mapping: how to record each observation as a mark, shape, or action
Write your protocol as a clear set of instructions on a sheet of paper. Someone who wasn't in your pair should be able to follow them without explanation.

Swap your protocol with another pair and follow their instructions for 10 minutes. Don't ask any clarifying questions, just interpret the rules as written.

When time is up, compare your output with what the designers intended. Did you interpret the rules as they expected? Where was the protocol ambiguous? What surprised you about the result?



## AI Usage Statement

*Document any use of AI tools under an AI Usage Statement heading. Explain which tools you used and describe how you used them. Reference any AI-generated content (see [QuickCite](https://auckland.libguides.com/referencing-generative-ai-tools) for guidance).*
