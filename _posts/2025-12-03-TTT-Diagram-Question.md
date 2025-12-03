<!DOCTYPE html>
<html>
<head>
  <title>TTT Path Simulator</title>
  <style>
    canvas { border: 1px solid #333; background: #f9f9f9; margin-bottom: 10px; }
    button { padding: 8px 16px; cursor: pointer; background: #007bff; color: white; border: none; border-radius: 4px; margin-right: 5px; }
    button:hover { background: #0056b3; }
    .controls { margin-top: 10px; font-family: sans-serif; }
    #status { font-weight: bold; margin-top: 10px; height: 20px; color: #333; }
  </style>
</head>
<body>

<h3>GATE 2025: TTT Cooling Path Simulator</h3>
<canvas id="tttCanvas" width="600" height="400"></canvas>
<div class="controls">
  <button onclick="runPath('P')">Path P (300K)</button>
  <button onclick="runPath('Q')">Path Q (873K)</button>
  <button onclick="runPath('R')">Path R (673K)</button>
  <button onclick="runPath('S')">Path S (623K)</button>
</div>
<div id="status">Select a path to simulate...</div>

<script>
const canvas = document.getElementById('tttCanvas');
const ctx = canvas.getContext('2d');
const width = canvas.width;
const height = canvas.height;

// Coordinate Mapping (Log Time x Temp)
function mapX(time) { return 50 + (Math.log10(time) + 1) * (width - 100) / 6; }
function mapY(temp) { return height - 50 - (temp - 300) * (height - 100) / 800; }

function drawTTT() {
  ctx.clearRect(0, 0, width, height);
  
  // Draw Axes
  ctx.beginPath(); ctx.moveTo(50, height-50); ctx.lineTo(width-50, height-50); ctx.stroke();
  ctx.beginPath(); ctx.moveTo(50, height-50); ctx.lineTo(50, 50); ctx.stroke();
  
  // Draw Labels
  ctx.font = "12px Arial"; ctx.fillStyle = "black";
  ctx.fillText("Time (s) [Log Scale]", width/2 - 40, height - 15);
  ctx.fillText("Temp (K)", 10, height/2);
  ctx.fillText("1073K (Ae1)", 60, mapY(1073));

  // Draw C-Curves (Schematic)
  ctx.beginPath(); ctx.strokeStyle = "#666"; ctx.lineWidth = 2;
  // Start Curve
  ctx.moveTo(mapX(10), mapY(1000));
  ctx.bezierCurveTo(mapX(0.5), mapY(900), mapX(0.5), mapY(800), mapX(10), mapY(600));
  ctx.stroke();
  // Finish Curve
  ctx.beginPath();
  ctx.moveTo(mapX(1000), mapY(1000));
  ctx.bezierCurveTo(mapX(50), mapY(900), mapX(50), mapY(800), mapX(1000), mapY(600));
  ctx.stroke();

  // Ms / Mf lines
  ctx.strokeStyle = "purple"; ctx.setLineDash([5, 5]);
  ctx.beginPath(); ctx.moveTo(50, mapY(500)); ctx.lineTo(width-50, mapY(500)); ctx.stroke();
  ctx.fillText("Ms (500K)", width-120, mapY(500)-5);
  
  ctx.beginPath(); ctx.moveTo(50, mapY(373)); ctx.lineTo(width-50, mapY(373)); ctx.stroke();
  ctx.fillText("Mf (373K)", width-120, mapY(373)-5);
  ctx.setLineDash([]);
}

function animatePath(targetTemp, holdTime, name) {
  let t = 0.1;
  let currentTemp = 1073;
  const interval = setInterval(() => {
    drawTTT();
    
    // Draw Path Trace
    ctx.strokeStyle = "red"; ctx.lineWidth = 3;
    ctx.beginPath();
    ctx.moveTo(mapX(0.1), mapY(1073));
    
    // Cooling Phase
    if (currentTemp > targetTemp) {
      currentTemp -= 15;
      ctx.lineTo(mapX(0.1), mapY(currentTemp));
      document.getElementById('status').innerText = `Status: Rapid Cooling to ${targetTemp} K...`;
    } else {
      // Holding Phase
      currentTemp = targetTemp;
      t *= 1.2; // Logarithmic speed
      ctx.lineTo(mapX(0.1), mapY(targetTemp)); // Vertical drop drawn
      ctx.lineTo(mapX(t), mapY(targetTemp));   // Horizontal hold
      document.getElementById('status').innerText = `Status: Holding at ${targetTemp} K... Time: ${Math.round(t)}s`;
    }
    ctx.stroke();

    // Stop Conditions
    if (t >= holdTime) {
      clearInterval(interval);
      // Final Logic for Path S (Quench)
      if (name === 'S') {
         ctx.lineTo(mapX(t), mapY(300));
         ctx.stroke();
         document.getElementById('status').innerHTML = "Result: <span style='color:red'>Bainite + Martensite</span> (Quenched!)";
      } else {
         let result = name === 'P' ? "Martensite" : (name === 'Q' ? "Pearlite" : "Bainite");
         document.getElementById('status').innerHTML = `Result: <span style='color:green'>${result}</span>`;
      }
    }
  }, 30);
}

function runPath(p) {
  if(p==='P') animatePath(300, 1000, 'P'); // Quench
  if(p==='Q') animatePath(873, 240, 'Q');  // 4 min
  if(p==='R') animatePath(673, 1200, 'R'); // 20 min
  if(p==='S') animatePath(623, 120, 'S');  // 2 min
}

// Init
drawTTT();
</script>
</body>
</html>

function animatePath(targetTemp, holdTime, name) {
  let t = 0.1;
  let currentTemp = 1073;
  
  const interval = setInterval(() => {
    drawTTT();
    
    ctx.strokeStyle = "red"; 
    ctx.lineWidth = 3;
    ctx.beginPath();
    ctx.moveTo(mapX(0.1), mapY(1073)); // Start point

    // --- THE FIX IS HERE ---
    if (currentTemp > targetTemp) {
      // 1. Cool down
      currentTemp -= 15; 
      
      // 2. Increment time slightly to create the SLOPE
      // A rapid quench is not instantaneous!
      t += 0.05; 
      
      // 3. Draw to the NEW time coordinate, not fixed 0.1
      ctx.lineTo(mapX(t), mapY(currentTemp));
      
      document.getElementById('status').innerText = `Cooling... Temp: ${currentTemp}K`;
    } else {
      // Holding Phase Logic...
      ctx.lineTo(mapX(t), mapY(targetTemp)); // Draw the cooling slope first
      
      // Now increment time for the hold
      let holdStart = t;
      // ... (rest of your hold logic) ...
    }
    ctx.stroke();
    // ...
  }, 30);
}
