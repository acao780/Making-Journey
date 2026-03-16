// Week 02: Interactive Data Portrait - What Makes Me Laugh
// By Anna

// Data from Week 1
let laughterData = [
  { day: "Mon", time: "9:30am", what: "Friend told a joke", type: "Social" },
  { day: "Mon", time: "1:00pm", what: "Funny meme on Instagram", type: "Media" },
  { day: "Mon", time: "3:30pm", what: "Classmate made a joke", type: "In-class" },
  { day: "Mon", time: "8:00pm", what: "Roommate's funny reaction", type: "Social" },
  { day: "Tue", time: "10:00am", what: "Funny video on TikTok", type: "Media" },
  { day: "Tue", time: "2:00pm", what: "Professor made a pun", type: "In-class" },
  { day: "Tue", time: "7:30pm", what: "Friend sent a funny text", type: "Social" },
  { day: "Wed", time: "11:30am", what: "Funny moment in hallway", type: "Random" },
  { day: "Wed", time: "3:00pm", what: "Group project went silly", type: "In-class" },
  { day: "Wed", time: "9:00pm", what: "Comedy clip online", type: "Media" },
  { day: "Thu", time: "9:00am", what: "Roommate's morning joke", type: "Social" },
  { day: "Thu", time: "1:30pm", what: "Funny post on social media", type: "Media" },
  { day: "Thu", time: "4:00pm", what: "Classmate's comment", type: "In-class" },
  { day: "Fri", time: "11:00am", what: "Teacher's funny example", type: "In-class" },
  { day: "Fri", time: "6:00pm", what: "Friend's story", type: "Social" },
  { day: "Fri", time: "10:00pm", what: "Party with friends", type: "Social" },
  { day: "Sat", time: "12:00pm", what: "Brunch with friends", type: "Social" },
  { day: "Sat", time: "3:00pm", what: "Funny sign while shopping", type: "Random" },
  { day: "Sat", time: "8:00pm", what: "Comedy show on TV", type: "Media" },
  { day: "Sun", time: "2:00pm", what: "Video call with friend", type: "Social" },
  { day: "Sun", time: "7:00pm", what: "Dad made a joke", type: "Social" }
];

// Color mapping
let colors = {
  "Social": "#FFD93D",    // Yellow
  "Media": "#6BCB77",     // Blue/Green
  "In-class": "#4D96FF",  // Blue
  "Random": "#FF6B6B"     // Pink/Red
};

// Filter states
let showSocial = true;
let showMedia = true;
let showInClass = true;
let showRandom = true;

// Buttons
let btnSocial, btnMedia, btnInClass, btnRandom;

function setup() {
  createCanvas(600, 500);
  textSize(14);
  
  // Create filter buttons
  btnSocial = createButton('Social (9)');
  btnSocial.position(50, 60);
  btnSocial.mousePressed(() => { showSocial = !showSocial; });
  
  btnMedia = createButton('Media (5)');
  btnMedia.position(150, 60);
  btnMedia.mousePressed(() => { showMedia = !showMedia; });
  
  btnInClass = createButton('In-class (5)');
  btnInClass.position(250, 60);
  btnInClass.mousePressed(() => { showInClass = !showInClass; });
  
  btnRandom = createButton('Random (2)');
  btnRandom.position(370, 60);
  btnRandom.mousePressed(() => { showRandom = !showRandom; });
  
  updateButtonStyles();
}

function draw() {
  background(255);
  
  // Title
  fill(50);
  noStroke();
  textSize(24);
  textAlign(CENTER);
  text("What Makes Me Laugh This Week", width/2, 35);
  
  // Draw legend
  drawLegend();
  
  // Draw data points
  let yStart = 120;
  let yGap = 18;
  let xStart = 50;
  let count = 0;
  
  for (let i = 0; i < laughterData.length; i++) {
    let d = laughterData[i];
    let shouldShow = false;
    
    if (d.type === "Social" && showSocial) shouldShow = true;
    if (d.type === "Media" && showMedia) shouldShow = true;
    if (d.type === "In-class" && showInClass) shouldShow = true;
    if (d.type === "Random" && showRandom) shouldShow = true;
    
    if (shouldShow) {
      let y = yStart + count * yGap;
      
      // Draw colored dot
      fill(colors[d.type]);
      noStroke();
      ellipse(xStart, y, 12, 12);
      
      // Draw text
      fill(50);
      textAlign(LEFT);
      textSize(12);
      text(d.day + " " + d.time + " - " + d.what, xStart + 20, y + 4);
      
      count++;
    }
  }
  
  // Total count
  fill(100);
  textSize(14);
  textAlign(RIGHT);
  text("Total showing: " + count + " / 21", width - 30, height - 20);
}

function drawLegend() {
  let legendY = 90;
  let x = 50;
  
  textSize(12);
  textAlign(LEFT);
  
  // Social
  fill(colors["Social"]);
  ellipse(x, legendY, 10, 10);
  fill(50);
  text("Social", x + 15, legendY + 4);
  
  // Media
  fill(colors["Media"]);
  ellipse(x + 100, legendY, 10, 10);
  fill(50);
  text("Media", x + 115, legendY + 4);
  
  // In-class
  fill(colors["In-class"]);
  ellipse(x + 200, legendY, 10, 10);
  fill(50);
  text("In-class", x + 215, legendY + 4);
  
  // Random
  fill(colors["Random"]);
  ellipse(x + 320, legendY, 10, 10);
  fill(50);
  text("Random", x + 335, legendY + 4);
}

function updateButtonStyles() {
  // Style the buttons based on their state
  styleButton(btnSocial, showSocial, "#FFD93D");
  styleButton(btnMedia, showMedia, "#6BCB77");
  styleButton(btnInClass, showInClass, "#4D96FF");
  styleButton(btnRandom, showRandom, "#FF6B6B");
}

function styleButton(btn, isActive, col) {
  if (isActive) {
    btn.style('background-color', col);
    btn.style('color', 'black');
  } else {
    btn.style('background-color', '#ddd');
    btn.style('color', '#888');
  }
  btn.style('border', 'none');
  btn.style('padding', '8px 15px');
  btn.style('border-radius', '5px');
  btn.style('cursor', 'pointer');
}
