<!DOCTYPE html>
<html>
<head>
  <title>Corrected TTT Simulator</title>
  <style>
    body { font-family: 'Segoe UI', sans-serif; padding: 20px; background: #f4f4f9; }
    h3 { color: #333; }
    .container { background: white; padding: 20px; border-radius: 8px; box-shadow: 0 2px 10px rgba(0,0,0,0.1); display: inline-block; }
    canvas { border: 1px solid #ddd; background: #fff; display: block; margin-bottom: 15px; }
    .controls button {
      padding: 10px 15px; cursor: pointer; background: #007bff; color: white;
      border: none; border-radius: 4px; margin-right: 5px; font-size: 14px;
      transition: background 0.2s;
    }
    .controls button:hover { background: #0056b3; }
    #status { 
      margin-top: 15px; padding: 10px; background: #e9ecef; 
      border-left: 4px solid #007bff; font-weight: 600; color: #495057; 
    }
  </style>
</head>
<body>

<div class="container">
  <h3>GATE 2025: TTT Cooling Path Simulator (Fixed Slope)</h3>
  <canvas id="tttCanvas" width="600" height="400"></canvas>
  
  <div class="controls">
    <button onclick="startSimulation('P')">Path P (Rapid Quench)</button>
    <button onclick="startSimulation('Q')">Path Q (Pearlite)</button>
    <button onclick="startSimulation('R')">Path R (Bainite)</button>
    <button onclick="startSimulation('S')">Path S (The Trap)</button>
  </div>
  <div id="status">Select a path to simulate...</div>
</div>

<script>
const canvas = document.getElementById('tttCanvas');
const ctx = canvas.getContext('2d');
const width = canvas.width;
const height = canvas.height;

// --- Configuration ---
const CONFIG = {
  Ae1: 1000,
  Ms: 500,
  Mf: 373,
  NoseTemp: 823,
  NoseTime: 1
};

// --- Coordinate Mapping ---
// X: Logarithmic Time (0.1s to 100,000s)
// Y: Linear Temp (200K to 1100K)
function mapX(time) {
  // Math.log10(0.1) is -1. Range is -1 to 5 (6 orders of magnitude)
  return 50 + (Math.log10(time) + 1) * (width - 100) / 6;
}
function mapY(temp) {
  // Map 200K-1100K to canvas height
  return height - 50 - (temp - 200) * (height - 100) / 900;
}

// --- Drawing Background ---
function drawBackground() {
  ctx.clearRect(0, 0, width, height);
  
  // Axes
  ctx.beginPath(); ctx.moveTo(50, height-50); ctx.lineTo(width-50, height-50); ctx.stroke(); // X
  ctx.beginPath(); ctx.moveTo(50, height-50); ctx.lineTo(50, 50); ctx.stroke(); // Y
  
  // Labels
  ctx.fillStyle = "#666"; ctx.font = "12px Arial";
  ctx.fillText("Time (s) [Log Scale]", width/2 - 40, height - 15);
  ctx.fillText("Temp (K)", 10, height/2);
  
  // Critical Lines
  drawDashedLine(CONFIG.Ae1, "Ae1 (1000K)", "black");
  drawDashedLine(CONFIG.Ms, "Ms (500K)", "purple");
  drawDashedLine(CONFIG.Mf, "Mf (373K)", "purple");

  // C-Curves (Schematic)
  ctx.strokeStyle = "#444"; ctx.lineWidth = 2; ctx.setLineDash([]);
  
  // Start Curve (1%)
  ctx.beginPath();
  ctx.moveTo(mapX(10), mapY(1000));
  ctx.bezierCurveTo(mapX(0.5), mapY(900), mapX(0.5), mapY(800), mapX(10), mapY(600)); // Upper nose
  ctx.bezierCurveTo(mapX(20), mapY(500), mapX(30), mapY(400), mapX(100), mapY(350)); // Lower bay
  ctx.stroke();

  // Finish Curve (99%)
  ctx.beginPath();
  ctx.moveTo(mapX(1000), mapY(1000));
  ctx.bezierCurveTo(mapX(50), mapY(900), mapX(50), mapY(800), mapX(1000), mapY(600)); // Upper nose
  ctx.bezierCurveTo(mapX(2000), mapY(500), mapX(3000), mapY(400), mapX(5000), mapY(350)); // Lower bay
  ctx.stroke();
}

function drawDashedLine(temp, label, color) {
  ctx.strokeStyle = color; ctx.setLineDash([5, 5]); ctx.lineWidth = 1;
  ctx.beginPath(); ctx.moveTo(50, mapY(temp)); ctx.lineTo(width-50, mapY(temp)); ctx.stroke();
  ctx.fillStyle = color; ctx.fillText(label, width-120, mapY(temp)-5);
}

// --- Animation Logic ---
let animationId = null;

function startSimulation(mode) {
  if (animationId) clearInterval(animationId);
  
  // Initial State
  let state = {
    t: 0.1,         // Current Time
    temp: 1000,     // Current Temp
    history: [{x: mapX(0.1), y: mapY(1000)}], // Path for drawing
    phase: 'COOLING', // COOLING, HOLDING, QUENCHING, DONE
    targetTemp: 0,
    holdTime: 0,
    elapsedHold: 0
  };

  // Setup parameters based on mode
  if (mode === 'P') { state.targetTemp = 300; state.holdTime = 0; }
  if (mode === 'Q') { state.targetTemp = 873; state.holdTime = 240; }
  if (mode === 'R') { state.targetTemp = 673; state.holdTime = 1200; }
  if (mode === 'S') { state.targetTemp = 623; state.holdTime = 120; }

  const statusEl = document.getElementById('status');

  animationId = setInterval(() => {
    drawBackground();

    // 1. Update State
    if (state.phase === 'COOLING') {
      if (state.temp > state.targetTemp) {
        state.temp -= 10;     // Temp Drop Rate
        state.t += 0.05;      // Time Advance (The Slope Fix!)
        statusEl.innerText = `Status: Rapid Cooling... ${Math.round(state.temp)} K`;
      } else {
        state.phase = state.holdTime > 0 ? 'HOLDING' : 'DONE';
        // Special case for P (Direct Quench)
        if (mode === 'P') state.phase = 'DONE';
      }
    } 
    else if (state.phase === 'HOLDING') {
      if (state.elapsedHold < state.targetTemp * 0 + state.holdTime) { // Logic simplified
        // Logarithmic time progression for holding
        state.t *= 1.1;
        state.elapsedHold = state.t; // Approximation for viz
        statusEl.innerText = `Status: Isothermal Hold at ${state.targetTemp} K... Time: ${Math.round(state.t)}s`;
        
        if (state.t >= state.holdTime) {
           state.phase = (mode === 'S') ? 'QUENCHING' : 'DONE';
        }
      }
    }
    else if (state.phase === 'QUENCHING') {
       // Path S specific second quench
       if (state.temp > 300) {
          state.temp -= 10;
          state.t += 1; // Slower time advance on log scale at later times
          statusEl.innerText = `Status: Final Quench to 300K...`;
       } else {
          state.phase = 'DONE';
       }
    }

    // 2. Record Path
    state.history.push({ x: mapX(state.t), y: mapY(state.temp) });

    // 3. Draw Path
    ctx.beginPath();
    ctx.strokeStyle = "red"; ctx.lineWidth = 3; ctx.setLineDash([]);
    ctx.moveTo(state.history[0].x, state.history[0].y);
    for (let p of state.history) ctx.lineTo(p.x, p.y);
    ctx.stroke();

    // 4. Check End
    if (state.phase === 'DONE') {
      clearInterval(animationId);
      let msg = "";
      if (mode === 'P') msg = "Result: Martensite (100%)";
      if (mode === 'Q') msg = "Result: Coarse Pearlite";
      if (mode === 'R') msg = "Result: Bainite";
      if (mode === 'S') msg = "Result: <span style='color:red'>Bainite + Martensite</span> (Interrupted Quench)";
      statusEl.innerHTML = msg;
    }

  }, 30);
}

// Init
drawBackground();
</script>
</body>
</html>
