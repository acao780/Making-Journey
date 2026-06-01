---
layout: default
---

# Week 06

[← Back to Home](../index.md)

## Documentation 
During the Week 6 proposal consultation, I introduced my topic to the teacher. I explained my plan to create a food diary that tracks both my eating behavior and daily caloric intake. My purpose for recording this data is to remind myself to take care of my body. My motivation stems from an experience last year when a medication I was taking caused a loss of appetite and a dislike for meat. My weight dropped from 53kg to below 50kg, which left me feeling exhausted and unhealthy. From the article, "Gastic Health - how Overating or under eating can impact your stomach" it mentions "when you do eat enough food, your body goes into starvation mode. This can cause gastric pain, constipation, and other digestive problems. Skipping meals can also make you feel weak, tired, and irritable, which can affect your overall wellbeing." This made me realize the vital importance of eating well—it's the foundation for growth and vitality. I want to use this micro-perspective to observe my eating habits, analyze and uncover my dietary issues, and ultimately use data as a daily reminder for myself. 

Therefore, I began recording my data on April 16th, at the start of the school break. After a few days, I discovered that I often skip breakfast during holidays and occasionally skip lunch on school days. This pattern is a significant concern for my future health, especially since my grandfather suffered from a stomach disease caused by food scarcity during his childhood. Thus, I have a strong motivation to track my energy intake and monitor my behavior. Through this, I aim to create a visual data design that reminds me to prioritize my well-being and conveys the importance of caring for one's body through healthy daily eating.

The purpose of my project is to remind people to take care of their bodies. By showing my own eating habits, I want to raise awareness about the importance of regular meals. I believe that small behaviors, like skipping breakfast, can add up to big health problems over time.

## 1. Data Exploration 
In this phase of my research, I have been collecting personal dietary entries since April 16th. I began by establishing a structured dataset that includes dates, meal times, and specific food content. However, while auditing this data, I discovered that the records have significant limitations in terms of data visualization and depth. Currently, my data is strictly confined to logs of what I eat for each meal, lacking any supporting metrics or deeper quantitative evidence. Furthermore, I realized that my current findings are limited to my personal experience and lack broader social representation. If only collecting my dietary, it would have limited sample size. One limitation of this project is that the data only comes from one person. Since the food diary records my own eating habits, it does not represent the experiences of a wider group of people. This makes it difficult to draw broader conclusions about eating behaviours in society. Therefore, I will simultaneously track the dietary data of my family members and friends, which will allow the project to better reflect the diverse habits of my target personas.
![sketch data](../assets/week-05/week5_image.jpg)

Based on my secondary research and the behavioral patterns observed so far—specifically, my habit of frequently skipping breakfast or lunch—I have decided to add two new measurement metrics to my tracking sheets. Therefore, I need to incorporate the measurement of both total calories and daily energy levels.

From the article - “How Many Calories Should You Eat in a Day?”
| Gender | Age Group | Sedentary (Low) | Moderately Active (Mid) | Active (High) | Total Intake Range |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Female** | 21–25 | 2,000 Calories | 2,200 Calories | 2,400 Calories | **2,000–2,400 Calories** |
| | 26–50 | 1,800 Calories | 2,000 Calories | 2,400 Calories | **1,800–2,400 Calories** |
| | 51–60 | 1,600 Calories | 1,800 Calories | 2,200 Calories | **1,600–2,200 Calories** |
| | 61+ | 1,600 Calories | 1,800 Calories | 2,000 Calories | **1,600–2,000 Calories** |
| **Male** | 21–25 | 2,400 Calories | 2,800 Calories | 3,000 Calories | **2,400–3,000 Calories** |
| | 26–35 | 2,400 Calories | 2,600 Calories | 3,000 Calories | **2,400–3,000 Calories** |
| | 36–40 | 2,400 Calories | 2,600 Calories | 2,800 Calories | **2,400–2,800 Calories** |
| | 41–45 | 2,200 Calories | 2,600 Calories | 2,800 Calories | **2,200–2,800 Calories** |
| | 46–55 | 2,200 Calories | 2,400 Calories | 2,800 Calories | **2,200–2,800 Calories** |
| | 56–60 | 2,200 Calories | 2,400 Calories | 2,600 Calories | **2,200–2,600 Calories** |
| | 61–65 | 2,000 Calories | 2,400 Calories | 2,600 Calories | **2,000–2,600 Calories** |
| | 66–75 | 2,000 Calories | 2,200 Calories | 2,600 Calories | **2,000–2,600 Calories** |
| | 76+ | 2,000 Calories | 2,200 Calories | 2,400 Calories | **2,000–2,400 Calories** |

Another limitation of this project is the calorie calculations are based on estimated food portions rather than exact measurements. Because I did not weigh every meal, some calorie values may be inaccurate. Unfortunately, I don't have a food scale to weight every meals。 And I have no way to weigh myself when eating at restaurants. However, the data is still useful for identifying overall patterns and trends.

I also rate my energy level between 1 and 10; this represents my overall physical and mental state for the day, capturing how my body actually feels in response to what I eat. In this design project, while Calories serve as the objective, quantitative input (measuring the raw energy consumed), the Energy Level acts as the subjective, qualitative output (tracking holistic vitality, cognitive focus, and physical fatigue). By juxtaposing these two metrics, the data visualization highlights the critical correlation between food intake and daily performance. More importantly, it maps the behavioral chain reaction—such as the severe energy drops (levels 1–3) that directly follow skipped meals—thereby transforming personal intuition into a visible, data-driven warning system for self-care.

In conclusion, an audit of my dietary logs from April 16th to June 1 revealed a chronic pattern of missing meals—specifically skipping breakfast on holidays and lunch on busy school days. Recognizing that simple food logs lacked data depth, I upgraded my tracking methodology by introducing two critical metrics: total calories and daily energy levels (1–10) to map the physical and psychological impact of these habits. However, I soon realized that focusing solely on my own experience created a severe limitation in social representation, failing to capture the broader 'why' behind meal-skipping. Driven by these insights, my project is undergoing a profound shift from a simple 'personal diary' to a 'social intervention tool' aimed at raising public awareness about irregular eating habits and self-care. To achieve this, my design direction using digital p5.js visualization to approach. To build a robust foundation for this new direction, I will expand my scope to simultaneously track the dietary data of family members and friends, thereby better reflecting the diverse habits of my target personas. Consequently, to address all existing data gaps and gather a more scientifically and emotionally rigorous dataset, I have decided to officially redo and restart my data collection process.

### Data Collection Method
The data was collected through a daily food diary. Each day, I recorded what I ate, the type of day it was (school day, weekend, or holiday), my estimated calorie intake, and my daily energy level on a scale from 1 to 10.
### Data Categories
#### Date and Day Type
This records when the data was collected and provides context about my daily routine. Different types of days, such as school days, weekends, and holidays, may influence eating habits.
#### Breakfast, Lunch, and Dinner
These categories record what foods were eaten during each meal. They also show whether a meal was skipped.
#### Total Calories
This is an estimate of the total amount of energy consumed each day through food and drinks.
#### Energy Level (1–10)
This is a self-reported score that reflects how energetic I felt throughout the day. Higher scores indicate feeling more focused, active, and energetic, while lower scores indicate tiredness or lack of energy.

### Anna's Self-tracked personal dietary log (April 16, 2026 – May 31, 2026)， 46 days.
| Date | state | Breakfast| Lunch | Dinner | Total calories | Energy Levels (1-10) |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **04/16** | Holiday | None | fried rice | chicken soup + rice + steak dish | 1650 | 5 |
| **04/17** | Holiday | eggs + nibbles | steak nodolles | steam chicken + rice + Boiled green vegetable| 2150 | 8 |
| **04/18** | Holiday | None | pie + chocolate milk | Boiled broccoli + steak dish + rice | 1300 | 4|
| **04/19** | Holiday | bread + milk | cheese pasta + chocolate milk | fried rice |1850 | 7 |
| **04/20** | School | eggs + milk | None | steak nodolles | 1300 | 4 |
| **04/21** | School | bread + egg | pie | chicken soup + rice + Boiled green vegetable + shredded potatoes| 1750 | 6 |
| **04/22** | School | bread + nibbles + egg| None | fried rice | 1100 | 3 |
| **04/23** | School | None | None | steak nodolles | 800 | 1 |
| **04/24** | School | bread + nibbles | None | steak dish | 830 | 2|
| **04/25** | weekend | eggs + milk | fried rice | steak dish + rice + Boiled broccoli | 1900 | 7|
| **04/26** | weekend | bread + egg + milk | cheese pasta | steam chicken + rice + chicken soup | 2050 | 8|
| **04/27** | School | bread + nibbles + egg| apple | fried rice + cherry + steam chicken | 1650 | 6|
| **04/28** | School | eggs + milk + hot dog | pie + chocolate milk | chicken soup + rice + steak dish | 2250 | 8 |
| **04/29** | School | bread  + Cereal + egg | cheese pasta + apple + chocolate | steak noodles + chicken soup | 2550 |10 |
| **04/30** | School | bread + nibbles | fried rice + pear | pizza + coke| 2400 |8 |
| **05/01** | School | eggs + milk | None | fried rice + steam chicken | 1400 | 4 |
| **05/02** | weekend  | bread + egg + milk | steak nodolles | cheeseburger + coke + chip | 2700| 10 |
| **05/03** | weekend  | bread + nibbles+ orange juice | cheese pasta + chocolate milk| chicken soup + rice + shredded potatoes | 2150 | 8 |
| **05/04** | School | chicken noodle | apple | steak nodolles | 1400 | 4 |
| **05/05** | School | bread + milk + egg | pie | Pepperoni pizza + Chicken soup| 2200 | 8 |
| **05/06** | School | cereal | cheese pasta | steak dish + rice | 1900 | 7|
| **05/07** | School | bread + nibbles + egg| None | chicken soup + rice + shredded potatoes | 1200 | 3 |
| **05/08** | School | None | fried rice + apple | pizza + chicken soup + mango | 1900 | 6 |
| **05/09** | weekend  | eggs + nibbles | pie + chocolate milk | steak dish + rice + Boiled broccoli | 1950 | 7 |
| **05/10** | weekend  | bread + egg + milk | cheese pasta | fried rice + apple pie| 2150 | 8 |
| **05/11** | School | bread + nibbles | None | chicken soup + steak dish + rice + Boiled green vegetable| 1150 | 3 |
| **05/12** | School | eggs + milk | fried rice + strawberry + grape | steak dish + rice + black tea | 2150 | 8 |
| **05/13** | School | bread + egg + yogurt | pie | steak noodles + soup | 1850 | 7 |
| **05/14** | School | None | cheese pasta + chocolate milk| steam chicken + rice + shredded potatoes | 1500 | 5 |
| **05/15** | School | bread + nibbles | fried rice +  orange juice | chicken soup + rice + steak dish | 1900 | 7 |
| **05/16** | weekend  | bread + cereal | steak noodles | Boiled broccoli + steak noddles| 1750 | 6 |
| **05/17** | weekend  | bread + egg + cereal| pie + chocolate milk | steam chicken + rice + Boiled green vegetable| 2050 | 8 |
| **05/18** | School | None | cheese pasta | steak noodles | 1500 | 5 |
| **05/19** | School | bread + nibbles | fried rice | chicken soup + rice + shredded potatoes | 1750 | 6|
| **05/20** | School | hot dog+ milk | pie | fried rice + steam chicken | 1850 | 7 |
| **05/21** | School | eggs + nibbles | steak noodles | chicken soup + steak noddles| 2000 | 7 |
| **05/22** | School | yogurt + chicken soup + rice | None | steak dish + rice | 1100 | 3 |
| **05/23** | weekend  | bread + egg+apple | fried rice | Boiled broccoli + steak dish + rice | 1950 | 7 |
| **05/24** | weekend  | eggs + milk | pie + chocolate milk | chicken soup + rice + steam chicken | 2100 | 8 |
| **05/25** | School | bread + nibbles | cheese pasta | steak noodles | 1750 | 6 |
| **05/26** | School | bread + egg + milk | fried rice | steam chicken + rice + shredded potatoes | 1900 | 7 |
| **05/27** | School | fried egg + orange juice + nibbles | pie | chicken soup + rice + steak dish | 1950 | 7 |
| **05/28** | School | None | steak noodles +  orange juice | fried rice + Boiled green vegetable + strawberry | 1500 | 5 |
| **05/29** | School | None| cheese pasta + chocolate milk| steam chicken + rice + Boiled broccoli | 1400 | 4 |
| **05/30** | weekend  | eggs + nibbles + grapes | fried rice + apple | Boiled broccoli + steak dish + rice | 1900 | 7 |
| **05/31** | weekend  | chicken noodles + black tea | steak noodles + apple | steam chicken + rice + chicken soup | 2100 | 8 |

### Anna's friend's Diet and Calorie Record (April 16 - June), 
- he always missed breakfast, almost do not have breakfast. and he also want to loss wait, so this would be a really unhealthy sign。但是这里也揭露了他少时的原因，一方面是漏掉早餐，但是一方面是减肥故意减少摄取量。这就给我带来了不同的原因。


### Anna's friend two Diet and Calorie Record (April 16 - June), 

### Anna's sister Diet and Calorie Record (April 16 - June), 
### Anna's mom Diet and Calorie Record (April 16 - June), 


## 2. Visual Research and Precedent Study 
During Week 6, I spent 45 minutes collecting visual references related to my project. I used Google Gemini to help me search for examples of data visualization, physical data design, and nutrition tracking projects.

![Alt text](../assets/week-06/lazer_cut.png)

The first reference I found was Hangjie Cai's final project called "Noisy Factory." This project uses laser cut to cut each data point into a separate piece. When all the pieces are stacked together, they reveal the relationship between environmental noise and economic disparities in London. What attracts me most is how physical the piece feels. By stacking laser-cut layers, you can actually see the pattern emerge. I want to use a similar method in my project, where each meal or skipped meal becomes a physical layer. 

![Alt text](../assets/week-06/dear_data.webp)

The second reference is "Dear Data" by Giorgia Lupi and Stefanie Posavec. This is a famous project where they hand-drew small data points on postcards every day for a year. They recorded tiny details like what they ate, how they felt, and their complaints. What I love most is the handmade feel. Each drawing is personal and unique. I will use their idea of different shapes and colors to represent different types of food or meals. 

![Alt text](../assets/week-06/quantifiedself.png)

The third reference is "The Quantified Self" and Nicholas Felton's annual reports. This project shows how people track their own data over months or years. I like how Felton organizes long timelines and clearly shows the difference between weekdays and weekends. Since my data starts from April 16th, I can use a similar timeline structure to compare my school days and holidays. 

![Alt text](../assets/week-06/giorgialupi.webp)

The fourth reference is Giorgia Lupi's project "Bruises: The Data We Don't See." This project visualizes a girl with an immune disease. Instead of simple charts, she uses flowing shapes that look like cells or petals. What I learn from this is that feelings like "tiredness" or "not feeling well" are hard to measure with numbers. I can use brush stroke thickness or color depth to show these feelings, not just calorie counts. 

![Alt text](../assets/week-06/datastring.webp)

The fifth reference is from "Domestic Data Streamers," a design team from Barcelona. They turn boring data into physical installations that let audiences "feel" the weight and volume of data. What attracts me is how they use weight and liquids to represent energy. I could use a leaking container to show energy loss, or different weights of sand to represent my daily intake.

![Alt text](../assets/week-06/datadesign.jpg)

The sixth reference is from Nathalie Miebach, an artist who translates complex data into hand-woven 3D sculptures. She turns abstract numbers into intricate physical structures that let audiences observe the fragility and interconnectedness of data. What attracts me is how she uses the structural integrity of a weave as a metaphor for stability. I could use this weaving concept to represent my daily eating routines; consistent meals would form a strong, tightly woven pattern.

After researching how different artists express data in unique ways, I am really excited to move on to the next phase: transforming my own data collection into amazing artwork. I am incredibly inspired by their use of drawing, laser-cutting, handcrafting, and coding to visualize data. This has deeply impacted me and made me reflect on how I can express and convey my own data to make a meaningful impact on others.
## 3. Project Planning and Skills Roadmap 
### 3.1 What do I need to make?
At this stage, I need to create a series of experiments that explore different ways of representing my food diary data. Rather than focusing on a final outcome, I will produce sketches, concept drawings, and small prototypes to test how information can be translated into visual and physical forms.

My experiments will investigate how calorie intake, meal patterns, and energy levels can be represented through colour, shape, size, layering, or movement. I will test both digital outputs using p5.js and physical outputs using paper, cardboard, and laser-cut materials. These explorations will help me evaluate which approach communicates the data most effectively and identify a suitable direction for the final project.


## 画一个草图

### 3.2 What do I need to learn?
1. Data Visualisation Principles

Learn how designers transform raw information into meaningful visual forms and how visual elements can communicate patterns and relationships.

2. p5.js Programming

Develop basic coding skills to create digital and interactive data visualisations.

3. Adobe Illustrator

Learn how to create vector graphics and prepare files for fabrication and prototyping.

4. Laser Cutting Techniques

Understand how to prepare laser-cut files, choose suitable materials, and operate fabrication equipment safely.

5. Material Experimentation

Explore how different materials and construction methods can influence the communication of data.

### 3.3 What are my next steps?

My next step is to continue collecting and organising my food diary data while analysing it for patterns and relationships. Once the dataset is complete, I will identify which variables are most meaningful to visualise, such as calorie intake, meal frequency, and energy levels.

At the same time, I will begin researching examples of data visualisation, data sculptures, and physical data representations created by other designers. Using these references, I will generate a range of sketches and concepts before developing simple digital and physical prototypes.

To support this process, I will improve my skills in p5.js, Adobe Illustrator, and laser cutting. Through testing, reflection, and iteration, I aim to discover an appropriate visual language for my dataset and establish a clear direction for the final project.

## Independent Study

### 1. Consultation Reflection
During the proposal consultation, I met with my instructor to discuss my project idea of creating a food diary that tracks both eating behaviour and daily calorie intake. I shared my personal experience of losing weight due to medication, developing irregular eating habits, and how this motivated me to pay more attention to my health through mindful eating.

The instructor asked several helpful questions that challenged my thinking. First, he asked who my target audience was—myself or others. This made me reconsider whether my project should remain a personal reflection or communicate a broader message. Second, he asked how I would obtain accurate nutritional data. At the time, I was unsure about reliable sources and methods for calorie calculation. Finally, he encouraged me to research existing data visualisation projects for inspiration and to understand how other designers communicate complex information.

The discussion helped sharpen my project direction. Initially, I focused mainly on documenting my own eating habits. However, I realised that I need to connect my personal experience to wider issues surrounding nutrition, health, and wellbeing. As a result, I plan to expand my research beyond my own dataset and investigate why regular eating is important, including the physical and mental impacts of skipping meals. I will also explore nutrition databases and APIs to improve the accuracy of my calorie data and study existing data visualisation and data sculpture projects to inform future design decisions.

### 2. Technical Skill Building

My project is a physical data visualization that combines digital design and laser-cut craftsmanship. This idea is inspired by Hangjie Cai’s project, "Noisy Factory." My goal is to transform my abstract dietary data into a tangible, 3D piece that people can see and touch. 
The physical part will be made with laser cut. Each layer will represent a day. The size of each layer will show how much I ate. If I skipped a meal, that layer will be smaller or missing. When all layers are stacked together, viewers will see the pattern of my eating habits.
I will first draw the design on paper. This helps me see the idea before cutting expensive materials. I will iterate with paper many times until the design looks good. Then I will use the laser cut machine to make the final piece.

| Priority | Skill/Tool | Why I Need It |
|----------|-----------|--------------|
| 1 | Drawing / Sketching | To visualize my idea before making |
| 2 | Laser Cut Machine | To create the physical layers |
| 3 | Data Collection | To record and organize my food data |
| 4 | Photography | To document my final project |

My next step is to finish the data collection. I need to add the "reason" column to my table. This means recording why I skipped a meal. Was I busy? Was I not hungry? Did I sleep late? Understanding the "why" behind my behavior is important. I also need to calculate the calories for each meal. There are two ways to do this. First, I can use the USDA FoodData Central API, which is free and accurate. Second, I can search on Google Gemini for estimated values. Either way, I need to finish this before I start designing.
After the data is ready, I will start drawing the first sketch on paper. I want to try 2-3 different designs. Each design will show the data in a different way. I will ask my classmates for feedback on these sketches. This will help me choose the best direction. While waiting for feedback, I will begin to make a simple version first. I will add colors and more details later.
Finally, I will book time at the laser cut workshop. I need to practice on cheap paper before using the final material. This helps me reduce waste and save money. I will iterate 3-4 times until the design looks good.

After seeing these references, I decided to move in a clearer direction. I want to combine digital visualization with handmade physical elements. The laser cut will show the patterns, and the colors will show the feelings. This approach feels more meaningful than just numbers on a screen.

The data also influenced my design direction. Originally, I planned to create a digital visualisation using p5.js. However, I realised that a physical data sculpture could better communicate the personal and emotional aspects of eating habits. The calorie data can provide a clear numerical structure, while handmade physical elements can represent personal experiences, emotions, and energy levels in a more meaningful way.

For these reasons, I decided to restart the data collection process with a larger group of participants and use the new dataset to inform the final design outcome.


### Current Progress and Development 
I am using p5.js to design the visual interface. Below are the initial images and code from my Week 5 report, representing the rough data visualization from the planning stage. Following the proposal consultation, I am now focused on further developing this idea. The first step in the development phase is to find a usable API that can be integrated into my project. Currently, the nutritional data for my p5.js visualization does not come from a standard nutrition API; instead, I am using Google Gemini to query the energy content of foods. At this stage, I am collecting nutritional data manually, but my next step is to find a functional API to automate this process within the visualization.

### Video & Code

<iframe src="https://www.youtube.com/embed/ZtuKyqvnCUM" width="560" height="315"> </iframe>

Below are the P5.JS code: 

![Alt text](../assets/week-06/code.png) 
### 3. Initial Concept Sketch
Based on my paper sketches from class, I created a more detailed concept. The first layer is the physical laser-cut piece. Each day is a circular layer. The size of the circle shows how much I ate. Missing meals create empty spaces. When stacked together, these layers show my eating patterns over time.

![Alt text](../assets/week-06/brainstorm.jpg)

## Reference

(Gastric Health – How Overeating or Under-eating Can Impact Your Stomach)
https://gastro.com.sg/gastric-health-how-overeating-or-under-eating-can-impact-your-stomach/#:~:text=When%20you%20do%20not%20eat,can%20affect%20your%20overall%20wellbeing.

(How Many Calories Should You Eat in a Day?)
https://health.clevelandclinic.org/how-many-calories-a-day-should-i-eat

https://www.instagram.com/p/DDEtR3EiRrU/?img_index=3

https://www.dear-data.com/theproject

https://quantifiedself.com/

https://giorgialupi.com/bruises-the-data-we-dont-see

https://www.domesticstreamers.com/work/data-strings/

https://news.virginia.edu/content/qa-how-do-you-weave-data-art


## AI Usage Statement

*Document any use of AI tools under an AI Usage Statement heading. Explain which tools you used and describe how you used them. Reference any AI-generated content (see [QuickCite](https://auckland.libguides.com/referencing-generative-ai-tools) for guidance).*
