---
layout: default
---

# Week 02

[← Back to Home](../index.md)

## Documentation

### What I Chose to Work With

For this week's interactive data portrait, I chose to continue with the **same data from Week 1**—"what makes me laugh and when". This was a deliberate choice because I had already spent a week collecting and visualising this data by hand, so I understood its structure well. The data includes 21 laughter events recorded over one week, each with a day, time, type, and description. I kept the same color coding system (yellow for Social, green for Media, blue for In-class, red for Random) to maintain consistency with my hand-drawn portrait.

### Iteration 1: Filter Buttons (First Version)

My first approach was to create **four toggle buttons** that filter the data by laughter type. Each button controls whether items of that category are shown or hidden. I also added a counter at the bottom showing how many items are currently displayed out of the total 21.

**Why this approach?**
- It directly extends my original visual system from Week 1 (color-coded categories)
- Buttons are familiar and intuitive for users
- The toggle mechanic is simple to understand

**Challenges faced:**
- Initial button positioning was off-screen
- Had to learn how to style buttons with CSS in p5.js
- The counter needed to update dynamically

### Iteration 2: Horizontal Categories (Refined Version)

After testing Iteration 1, I explored a **horizontal layout** where data is organized into four distinct columns by type. Each column has a header showing the category name and count.

**What changed:**
- Replaced buttons with visual columns
- Data is always visible but organized by type
- Easier to compare across categories at a glance

**Why keep both?**
- Iteration 1 emphasizes **user control** (viewers choose what to see)
- Iteration 2 emphasizes **visual organization** (categories are pre-sorted)
- Both represent valid design decisions for different use cases

### Tools and Learning

I used **vibe coding** (AI-assisted coding) to help create both versions of this sketch. I described what I wanted in plain language to an LLM, which generated the initial code structure. This was helpful because I'm still learning p5.js, and the AI helped me understand how to create buttons and handle click events.

From this process, I learned:
- How to use DOM elements in p5.js (createButton)
- How to use conditional logic to filter data
- How to style HTML elements with CSS
- That AI-generated code sometimes needs adjustment—initial versions had positioning issues that I had to fix

---

## Images & Media

### Iteration 1: Filter Buttons
![Interactive Data Portrait - Filter Buttons](../assets/week-02/iteration-1-filter-buttons.png)
*Interactive p5.js sketch with toggle buttons for different laughter types*

### Iteration 2: Horizontal Categories
![Interactive Data Portrait - Horizontal Layout](../assets/week-02/iteration-2-horizontal.png)
*Organized layout with category columns*

---

## Reflection

### What data and visual aspects from Experiment 1 did you choose to work with, and why?

I chose to work with the **same data from Week 1**—"what makes me laugh and when"—because I had already spent a week collecting this data and understood its structure well. The data includes 21 laughter events with day, time, type, and description. I kept the same color coding system (yellow for Social, green for Media, blue for In-class, red for Random) to maintain consistency with my hand-drawn portrait. This continuity allowed me to focus on learning interactive techniques rather than figuring out a new dataset.

### How did you decide which interactive elements to use?

I decided to use **four filter buttons** (Iteration 1) because this directly extends my original visual system. In Week 1, I used colors to represent different types of laughter. The buttons let viewers toggle which types they want to see—this felt natural and intuitive. After testing, I also created **Iteration 2** with horizontal category columns for viewers who prefer pre-organized layouts over manual filtering. Both approaches address the same goal (helping viewers explore data by type) but through different interaction models.

### What can a viewer learn by interacting with your sketch that they couldn't from my hand-drawn portrait?

The interactive sketch reveals **patterns and comparisons** that are hard to see in a static drawing. Viewers can instantly see which category is most common (Social: 9 events). They can also explore questions like "When do I laugh most at school versus at home?" by toggling categories. In Iteration 2, the horizontal layout makes direct comparison even easier—all categories are visible simultaneously. This active exploration isn't possible with a hand-drawn portrait where all information is visible at once.

### Did you use vibe coding or other tools in your process? What did you learn from this?

Yes, I used **vibe coding** (AI-assisted coding) to build both iterations of this sketch. I described my requirements in plain language to an LLM, which generated the initial code. From this process, I learned how to use DOM elements in p5.js (createButton), how to filter data using conditional logic, and how to style elements with CSS. I also learned that AI-generated code sometimes needs adjustment—initial versions had positioning issues that I had to fix manually.

### What would you develop further with more time?

If I had more time, I would add:
- A **day selection** feature to filter by specific days of the week (dropdown or slider)
- **Smooth animations** so items fade in/out when toggling categories
- **Click for details** - show more information when clicking on each data point
- **Mobile-friendly design** - make the layout work better on smaller screens

### Any other reflections?

This exercise changed how I think about data visualisation. I realised that **interaction itself tells a story**—the choices viewers make when exploring data reveal their own interests and questions. An interactive visualisation doesn't just present answers; it invites viewers to ask their own questions. I also reflected on the relationship between my hand-drawn Week 1 portrait and this digital Week 2 version. The hand-drawn version is personal and artistic, while the interactive version is functional and exploratory. Both are valuable—they serve different purposes and tell different stories about the same data. Creating two iterations helped me understand that there are multiple valid solutions to the same design problem.

---

## AI Usage Statement

I used **vibe coding** (LLM-assisted coding) to help generate both iterations of the p5.js sketch. I described my requirements in plain language, reviewed the generated code, and made adjustments as needed.
