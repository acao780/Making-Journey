---
layout: default
---

# Week 06

[← Back to Home](../index.md)

## Documentation 
During the week 6 consultation, I introduced my topic to the instructor. I explained that I want to create a food diary that tracks both my eating behavior and daily caloric intake. My motivation stems from an experience last year when a medication I was taking caused a loss of appetite and a dislike for meat. My weight dropped from 53kg to below 50kg, which left me feeling exhausted and unhealthy.

I began recording my data on April 16th. Through this process, I discovered that I often skip breakfast during holidays and occasionally skip lunch on school days. This pattern is a significant concern for my future health, especially since my grandfather suffered from a stomach disease caused by food scarcity during his childhood. By tracking my energy intake and monitoring my behaviors, I aim to create a tool that reminds me to prioritize my well-being.

### Current Progress and Development 

I am using p5.js to design the visual interface. Below are the initial images and code from my week 5 report, representing the rough data visualization at the planning stage. Following the proposal consultation, I am now focused on further developing this idea. The first step in the development phase is to find a usable API that can be integrated into my project. Currently, the nutritional data for my p5.js visualization doesn't come from a standard nutrition API; instead, it uses Google Gemini to query the energy content of foods. At this stage, I'm collecting nutritional data manually, rather than through automated API calls. My next step is to find a usable API that can be integrated into this visualization.

#### code
let inputFood, button;
let dailyRecords = []; 
let todayCalories = 0; 
function setup() {
  createCanvas(600, 400);
  inputFood = createInput('1 burger'); 
  inputFood.position(420, 70);
  inputFood.size(150);
  button = createButton('Log Energy');
  button.position(420, 105);
  button.style('background-color', '#0096ff');
  button.style('color', 'white');
  button.style('border', 'none');
  button.style('border-radius', '5px');
  button.style('padding', '8px 15px');
  button.style('cursor', 'pointer');
  button.mousePressed(addEnergyEffect);
  for (let i = 0; i < 7; i++) {
    dailyRecords.push(random(500, 2200));
  }
}
function draw() {
  background(252);
  drawHistory();      
  drawMainBottle();   
  drawInterface();    
}
function drawHistory() {
  push();
  fill(240);
  noStroke();
  rect(15, 15, 130, 370, 15); 
  textAlign(CENTER);
  textSize(12);
  textStyle(BOLD);
  fill(100);
  text("HISTORY", 80, 40);
  for (let i = 0; i < dailyRecords.length; i++) {
    let y = 60 + i * 45;
    stroke(200);
    strokeWeight(1);
    fill(255);
    rect(35, y, 22, 32, 5); 
    let h = map(dailyRecords[i], 0, 3000, 0, 32);
    h = constrain(h, 0, 32);
    noStroke();
    fill(135, 206, 235);
    rect(35, y + 32 - h, 22, h, 5);
    fill(130);
    textStyle(NORMAL);
    textSize(10);
    textAlign(LEFT);
    text("Day " + (i + 1), 70, y + 15);
    text(floor(dailyRecords[i]) + " kcal", 70, y + 28);
  }
  pop();
}
function drawMainBottle() {
  push();
  translate(270, 120); 
  let w = 110;      
  let h = 200;      
  let neckW = 45;   
  let neckH = 40;   
  let bottlePath = () => {
    beginShape();
    vertex(-neckW/2, -neckH); 
    vertex(neckW/2, -neckH);  
    bezierVertex(neckW/2, 0, w/2, 0, w/2, 30); 
    vertex(w/2, h - 30); 
    bezierVertex(w/2, h, -w/2, h, -w/2, h - 30); 
    vertex(-w/2, 30); 
    bezierVertex(-w/2, 0, -neckW/2, 0, -neckW/2, -neckH); 
    endShape(CLOSE);
  };
  noStroke();
  fill(240, 248, 255);
  bottlePath();
  push();
  drawingContext.save();
  bottlePath(); 
  drawingContext.clip(); 
  let fillHeight = map(todayCalories, 0, 3000, 0, h + neckH);
  fillHeight = constrain(fillHeight, 0, h + neckH);
  fill(0, 150, 255, 180); 
  rect(-w/2, h - fillHeight, w, fillHeight + 100); 
  drawingContext.restore();
  pop()
  stroke(40);
  strokeWeight(5);
  noFill();
  bottlePath();
  fill(60);
  noStroke();
  rect(-neckW/2 - 5, -neckH - 12, neckW + 10, 18, 4);
  pop();
}
function drawInterface() {
  push();
  textAlign(LEFT);
  fill(50);
  noStroke();
  textSize(15);
  textStyle(BOLD);
  text("DAILY LOG", 420, 50);
  textStyle(NORMAL);
  textSize(12);
  text("What did you eat?", 420, 65);
  let calStr = floor(todayCalories).toString();
  textSize(24);
  textStyle(BOLD);
  fill(0, 102, 204);
  text(calStr, 420, 180); 
  let kcalX = 420 + textWidth(calStr) + 8; 
  textSize(14);
  textStyle(NORMAL);
  fill(120);
  text("kcal", kcalX, 180)
  if (todayCalories > 2500) {
    fill(220, 0, 0);
    textStyle(BOLD);
    textSize(13);
    text(" ENERGY LIMIT!", 420, 210);
  }
  pop();
}
function addEnergyEffect() {
  let food = inputFood.value().toLowerCase();
  let energy = 0;
  if (food.includes("apple")) energy = 95;
  else if (food.includes("burger")) energy = 550;
  else if (food.includes("pizza")) energy = 285;
  else if (food.includes("chicken")) energy = 400;
  else if (food.includes("rice")) energy = 200;
  else if (food.includes("coke")) energy = 140;
  else energy = floor(random(150, 450)); 
  todayCalories += energy;
  console.log("Logged: " + food + " (+" + energy + " kcal)");
}


## Images & Media


![Alt text](../assets/week-01/your-image.jpg)


## AI Usage Statement

*Document any use of AI tools under an AI Usage Statement heading. Explain which tools you used and describe how you used them. Reference any AI-generated content (see [QuickCite](https://auckland.libguides.com/referencing-generative-ai-tools) for guidance).*
