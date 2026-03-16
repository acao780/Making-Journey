// Week 02: Interactive Data Portrait - What Makes Me Laugh
// Iteration 2: Horizontal Categories Layout
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
  "Media": "#6BCB77",     // Green
  "In-class": "#4D96FF",  // Blue
  "Random": "#FF6B6B"     // Red
};

// Organized data by category
let categories = ["Social", "Media", "In-class", "Random"];

function setup() {
  createCanvas(900, 500);
  textSize(14);
}

function draw() {
  background(255);
  
  // Title
  fill(50);
  noStroke();
  textSize(24);
  textAlign(CENTER);
  text("What Makes Me Laugh This Week", width/2, 35);
  
  // Draw columns for each category
  let colWidth = width / 4;
  let headerY = 70;
  let dataY = 110;
  let rowHeight = 25;
  
  for (let i = 0; i < categories.length; i++) {
    let cat = categories[i];
    let colX = i * colWidth;
    
    // Filter data for this category
    let catData = laughterData.filter(d => d.type === cat);
    
    // Column header with colored background
    fill(colors[cat]);
    rect(colX + 10, headerY - 20, colWidth - 20, 40, 5);
    
    // Header text
    fill(0);
    textSize(16);
    textAlign(CENTER);
    text(cat + " (" + catData.length + ")", colX + colWidth/2, headerY + 5);
    
    // Draw items in this category
    for (let j = 0; j < catData.length; j++) {
      let d = catData[j];
      let y = dataY + j * rowHeight;
      
      // Colored dot
      fill(colors[cat]);
      noStroke();
      ellipse(colX + 30, y, 8, 8);
      
      // Day and time
      fill(80);
      textSize(10);
      textAlign(LEFT);
      text(d.day + " " + d.time, colX + 45, y + 4);
    }
  }
  
  // Total count
  fill(100);
  textSize(14);
  textAlign(RIGHT);
  text("Total: 21 laughter events", width - 20, height - 20);
}
