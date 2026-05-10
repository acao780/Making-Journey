---
layout: default
---

# Week 06

[← Back to Home](../index.md)

## Documentation 
During the Week 6 proposal consultation, I introduced my topic to the instructor. I explained my plan to create a food diary that tracks both my eating behavior and daily caloric intake. My purpose for recording this data is to remind myself to take care of my body. My motivation stems from an experience last year when a medication I was taking caused a loss of appetite and a dislike for meat. My weight dropped from 53kg to below 50kg, which left me feeling exhausted and unhealthy.

I began recording my data on April 16th. Through this process, I discovered that I often skip breakfast during holidays and occasionally skip lunch on school days. This pattern is a significant concern for my future health, especially since my grandfather suffered from a stomach disease caused by food scarcity during his childhood. By tracking my energy intake and monitoring my behaviors, I aim to create a visual data design that reminds me to prioritize my well-being and conveys the importance of taking care of one's body through healthy daily eating.

The purpose of my project is to remind people to take care of their bodies. By showing my own eating habits, I want to raise awareness about the importance of regular meals. I believe that small behaviors, like skipping breakfast, can add up to big health problems over time.

### Current Progress and Development 

I am using p5.js to design the visual interface. Below are the initial images and code from my Week 5 report, representing the rough data visualization from the planning stage. Following the proposal consultation, I am now focused on further developing this idea. The first step in the development phase is to find a usable API that can be integrated into my project. Currently, the nutritional data for my p5.js visualization does not come from a standard nutrition API; instead, I am using Google Gemini to query the energy content of foods. At this stage, I am collecting nutritional data manually, but my next step is to find a functional API to automate this process within the visualization.

### Video & Code

<iframe src="https://www.youtube.com/embed/ZtuKyqvnCUM" width="560" height="315"> </iframe>

Below are the P5.JS code: 

![Alt text](../assets/week-06/screenshot1.png) 

![Alt text](../assets/week-06/Screenshot2.png) 

![Alt text](../assets/week-06/Screenshot3.png) 

![Alt text](../assets/week-06/Screenshot4.png) 

## 1. Data Exploration 

In this phase of my research, I have been collecting personal dietary entries since April 16th. I began by establishing a structured dataset that includes dates, meal times, and specific food content. However, while auditing this data, I discovered that the records have significant limitations in terms of accuracy. Because I lack precise measurements for food quantities, my calorie estimations remain somewhat subjective. Additionally, I recognize that my current dataset is limited to my own experience and lacks broader social representativeness.
More importantly, this recording process has clearly revealed my long-standing "meal skipping" behavior. I noticed a consistent pattern of skipping breakfast on holidays and ignoring lunch during busy school days. For me, this data is more than just numbers; it represents a significant health risk, especially given my family history of gastrointestinal diseases.

Because of these findings, I want to shift the focus of my project. It is moving from being a simple "personal diary" to becoming a "social intervention tool." By revealing the behavioral vulnerabilities hidden within my own data, I aim to create a design that raises public awareness about the importance of regular eating habits and prioritizing one's well-being.

![Alt text](../assets/week-05/week5_image.jpg)

The data shows the food and dairy intakes of breakfast, lunch and dinner, began on 16th of April. 

| Data | Breakfast | Lunch | Dinner |
|-----|------|-------------------|------|
| 04/16 | NONE | Fried Rice |------|
| 04/17 | Eggs + Nibbles | Steak Noddle |------|
| 04/18 | NONE | Pie + Chocolate |------|
| 04/19 | Bread + Milk | Cheese Paste + Chocolate |------|
| 04/20 | Bread + Milk | NONE |------|
| 04/21 | Bread + Egg | Pie |------|
| 04/22 | Egg + Nibbles + Bread| NONE |------|
| 04/23 |------| NONE |------|
| 04/24 | Bread + Nibbles | NONE |------|
| 04/25 |------| Morning joke from roommate |------|
| 04/26 |------| Funny post on social media |------|
| 04/27 |------| Classmate's comment funny |------|
| 04/28 |------| Funny picture |------|
| 04/29 |------| Friend's story about their day |------|
| 04/30 |------| Party with friends - lots of laughing |------|
| 05/01 |------| Brunch with friends - funny conversations |------|
| 05/02 |------| Shopping - funny sign I saw |------|
| 05/03 |------| Comedy show on TV |------|
| 05/04 |------| Funny video from friend |------|

(end when week 7 task open)

## 2. Visual Research and Precedent Study 

During Week 6, I spent 45 minutes collecting visual references related to my project. I used Google Gemini to help me search for examples of data visualization, physical data design, and nutrition tracking projects.

![Alt text](../assets/week-06/idea2.jpg)

The first reference I found was Hangjie Cai's final project called "Noisy Factory." This project uses laser cut to cut each data point into a separate piece. When all the pieces are stacked together, they reveal the relationship between environmental noise and economic disparities in London. What attracts me most is how physical the piece feels. By stacking laser-cut layers, you can actually see the pattern emerge. I want to use a similar method in my project, where each meal or skipped meal becomes a physical layer. 

The second reference is "Dear Data" by Giorgia Lupi and Stefanie Posavec. This is a famous project where they hand-drew small data points on postcards every day for a year. They recorded tiny details like what they ate, how they felt, and their complaints. What I love most is the handmade feel. Each drawing is personal and unique. I will use their idea of different shapes and colors to represent different types of food or meals. 

The third reference is "The Quantified Self" and Nicholas Felton's annual reports. This project shows how people track their own data over months or years. I like how Felton organizes long timelines and clearly shows the difference between weekdays and weekends. Since my data starts from April 16th, I can use a similar timeline structure to compare my school days and holidays. 

The fourth reference is Giorgia Lupi's project "Bruises: The Data We Don't See." This project visualizes a girl with an immune disease. Instead of simple charts, she uses flowing shapes that look like cells or petals. What I learn from this is that feelings like "tiredness" or "not feeling well" are hard to measure with numbers. I can use brush stroke thickness or color depth to show these feelings, not just calorie counts. 

The fifth reference is from "Domestic Data Streamers," a design team from Barcelona. They turn boring data into physical installations that let audiences "feel" the weight and volume of data. What attracts me is how they use weight and liquids to represent energy. I could use a leaking container to show energy loss, or different weights of sand to represent my daily intake.

After seeing these references, I decided to move in a clearer direction. I want to combine digital visualization with handmade physical elements. The laser cut will show the patterns, and the colors will show the feelings. This approach feels more meaningful than just numbers on a screen.

## 3. Project Planning and Skills Roadmap

### 3.1 What do I need to make?

I plan to create a project that combines a laser-cut physical piece .
The physical part will be made with laser cut. Each layer will represent a day. The size of each layer will show how much I ate. If I skipped a meal, that layer will be smaller or missing. When all layers are stacked together, viewers will see the pattern of my eating habits.

I will first draw the design on paper. This helps me see the idea before cutting expensive materials. I will iterate with paper many times until the design looks good. Then I will use the laser cut machine to make the final piece.

### 3.2 What do I need to learn?

| Priority | Skill/Tool | Why I Need It |
|----------|-----------|--------------|
| 1 | Drawing / Sketching | To visualize my idea before making |
| 2 | Laser Cut Machine | To create the physical layers |
| 3 | Data Collection | To record and organize my food data |
| 4 | Photography | To document my final project |

### 3.3 What are my next steps?

My next step is to finish the data collection. I need to add the "reason" column to my table. This means recording why I skipped a meal. Was I busy? Was I not hungry? Did I sleep late? Understanding the "why" behind my behavior is important. I also need to calculate the calories for each meal. There are two ways to do this. First, I can use the USDA FoodData Central API, which is free and accurate. Second, I can search on Google Gemini for estimated values. Either way, I need to finish this before I start designing.

After the data is ready, I will start drawing the first sketch on paper. I want to try 2-3 different designs. Each design will show the data in a different way. I will ask my classmates for feedback on these sketches. This will help me choose the best direction. While waiting for feedback, I will begin to make a simple version first. I will add colors and more details later.

Finally, I will book time at the laser cut workshop. I need to practice on cheap paper before using the final material. This helps me reduce waste and save money. I will iterate 3-4 times until the design looks good.

## Independent Study

### 1. Consultation Reflection


### 2. Technical Skill Building


### 3. Initial Concept Sketch

![Alt text](../assets/week-06/brainstorm.jpg)







## AI Usage Statement

*Document any use of AI tools under an AI Usage Statement heading. Explain which tools you used and describe how you used them. Reference any AI-generated content (see [QuickCite](https://auckland.libguides.com/referencing-generative-ai-tools) for guidance).*
