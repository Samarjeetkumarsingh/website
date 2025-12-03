<!DOCTYPE html>
<html>
<head>
  <title>GATE 2025 TTT Simulator</title>
  <style>
    body { font-family: 'Segoe UI', sans-serif; padding: 20px; background: #f0f2f5; }
    .container { max-width: 800px; margin: 0 auto; background: white; padding: 20px; border-radius: 12px; box-shadow: 0 4px 20px rgba(0,0,0,0.1); }
    canvas { background: #fff; border: 1px solid #ccc; width: 100%; border-radius: 4px; }
    .controls { margin-top: 20px; display: flex; gap: 10px; flex-wrap: wrap; }
    button { 
      padding: 10px 20px; border: none; border-radius: 6px; cursor: pointer; font-weight: 600; 
      background: #007bff; color: white; transition: all 0.2s; flex: 1;
    }
    button:hover { background: #0056b3; transform: translateY(-1px); }
    #status { 
      margin-top: 20px; padding: 15px; background: #e9f5ff; border-left: 5px solid #007bff; 
      border-radius: 4px; font-size: 1.1em; color: #333; min-height: 24px;
    }
    .legend { font-size: 0.9em; color: #666; margin-top: 10px; text-align: center; }
  </style>
</head>
<body>

<div class="container">
  <h2 style="text-align:center; color:#333;">GATE 2025: TTT Cooling Path Simulator</h2>
  <canvas id="tttCanvas" width="800" height="500"></canvas>
  
  <div class="controls">
    <button onclick="runPath('P')">Path P (Quench)</button>
    <button onclick="runPath('Q')">Path Q (Pearlite)</button>
    <button onclick="runPath('R')">Path R (Bainite)</button>
    <button onclick="runPath('S')">Path S (The Trap)</button>
    <button onclick="drawBackground()" style="background:#6c757d">Reset</button>
  </div>
  
  <div id="status">Select a path to simulate...</div>
  <div class="legend">X-Axis: Time (Log Scale) | Y-Axis: Temperature (K)</div>
</div>

<script>
const canvas = document.getElementById('tttCanvas');
const ctx = canvas.getContext('2d');
// Handle High DPI displays
const dpr = window.devicePixelRatio || 1;
const rect = canvas.getBoundingClientRect();
canvas.width = rect.width * dpr;
canvas.height = rect.height * dpr;
ctx.scale(dpr, dpr);
const width = rect.width;
const height = rect.height;

const CONFIG = {
  Ae1: 1000, Ms: 500, Mf: 373,
  minTemp: 300, maxTemp: 1100,
  minTime: 0.1, maxTime: 100000
};

// --- Coordinate Systems ---
function mapX(time) {
  const logTime = Math.log10(time);
  const minLog = Math.log10(CONFIG.minTime);
  const maxLog = Math.log10(CONFIG.maxTime);
  return 60 + ((logTime - minLog) / (maxLog - minLog)) * (width - 100);
}

function mapY(temp) {
  return height - 50 - ((temp - CONFIG.minTemp) / (CONFIG.maxTemp - CONFIG.minTemp)) * (height - 100);
}

function drawBackground() {
  ctx.clearRect(0, 0, width, height);
  
  // Grid & Axes
  ctx.strokeStyle = "#e0e0e0";
  ctx.lineWidth = 1;
  ctx.font = "12px sans-serif";
  ctx.fillStyle = "#666";

  // Time Grid (1, 10, 100...)
  for(let i=0; i<=5; i++) {
    let t = Math.pow(10, i);
    if(t < CONFIG.minTime) continue;
    let x = mapX(t);
    ctx.beginPath(); ctx.moveTo(x, 50); ctx.lineTo(x, height-50); ctx.stroke();
    ctx.fillText(t + "s", x-10, height-30);
  }
  
  // Temp Grid
  for(let T=300; T<=1100; T+=100) {
    let y = mapY(T);
    ctx.beginPath(); ctx.moveTo(60, y); ctx.lineTo(width-40, y); ctx.stroke();
    ctx.fillText(T, 25, y+4);
  }

  // Draw Axes Lines
  ctx.strokeStyle = "#333"; ctx.lineWidth = 2;
  ctx.beginPath();
  ctx.moveTo(60, height-50); ctx.lineTo(width-40, height-50); // X
  ctx.moveTo(60, height-50); ctx.lineTo(60, 50); // Y
  ctx.stroke();

  // Critical Lines
  drawLine(CONFIG.Ae1, "Ae1 (1000K)", "#333", []);
  drawLine(CONFIG.Ms, "Ms (500K)", "purple", [5, 5]);
  drawLine(CONFIG.Mf, "Mf (373K)", "purple", [5, 5]);

  // --- Accurate C-Curves ---
  ctx.lineWidth = 3;
  ctx.lineCap = "round";
  
  // Start Curve (1%)
  ctx.strokeStyle = "#28a745";
  ctx.beginPath();
  // Top to Nose
  ctx.moveTo(mapX(100), mapY(980));
  ctx.quadraticCurveTo(mapX(2), mapY(900), mapX(1), mapY(823)); 
  // Nose to Bay
  ctx.bezierCurveTo(mapX(1), mapY(700), mapX(20), mapY(600), mapX(30), mapY(500));
  ctx.stroke();
  ctx.fillStyle = "#28a745"; ctx.fillText("Start", mapX(1)-30, mapY(823));

  // Finish Curve (99%)
  ctx.strokeStyle = "#dc3545";
  ctx.beginPath();
  ctx.moveTo(mapX(2000), mapY(980));
  ctx.quadraticCurveTo(mapX(50), mapY(900), mapX(5), mapY(823));
  // Nose to Bay (Wide Shelf)
  ctx.bezierCurveTo(mapX(10), mapY(700), mapX(1000), mapY(600), mapX(3000), mapY(500));
  ctx.stroke();
  ctx.fillStyle = "#dc3545"; ctx.fillText("Finish", mapX(10)+10, mapY(823));
}

function drawLine(temp, label, color, dash) {
  ctx.strokeStyle = color; ctx.setLineDash(dash); ctx.lineWidth = 1.5;
  ctx.beginPath(); ctx.moveTo(60, mapY(temp)); ctx.lineTo(width-40, mapY(temp)); ctx.stroke();
  ctx.setLineDash([]);
  ctx.fillStyle = color; ctx.fillText(label, width-100, mapY(temp)-5);
}

// --- Animation Engine ---
let animationId = null;

function runPath(id) {
  if(animationId) clearInterval(animationId);
  drawBackground();
  
  let config = { target: 0, hold: 0 };
  if(id === 'P') config = { target: 300, hold: 0 };
  if(id === 'Q') config = { target: 873, hold: 240 };
  if(id === 'R') config = { target: 673, hold: 1200 };
  if(id === 'S') config = { target: 623, hold: 120 };
  
  let state = { 
    t: 0.1, 
    temp: 1073, 
    history: [{x: mapX(0.1), y: mapY(1073)}],
    phase: 'COOLING',
    holdStartT: 0
  };

  const statusEl = document.getElementById('status');

  animationId = setInterval(() => {
    drawBackground();
    
    // 1. Update Physics
    if (state.phase === 'COOLING') {
      if (state.temp > config.target) {
        state.temp -= 8; // Cooling Rate
        state.t += 0.05; // Time Passage (Slope)
        statusEl.innerText = `Cooling... Temp: ${Math.round(state.temp)} K`;
      } else {
        state.phase = config.hold > 0 ? 'HOLDING' : 'DONE';
        if(id === 'P') state.phase = 'DONE';
        state.holdStartT = state.t;
      }
    } 
    else if (state.phase === 'HOLDING') {
       // Logarithmic time step
       state.t *= 1.05;
       statusEl.innerText = `Holding at ${config.target} K... Time: ${Math.round(state.t)}s`;
       
       if (state.t >= config.hold) {
         state.phase = (id === 'S') ? 'QUENCHING' : 'DONE';
       }
    }
    else if (state.phase === 'QUENCHING') {
       if (state.temp > 300) {
         state.temp -= 8;
         state.t += 0.1; 
         statusEl.innerText = "Final Quench to 300 K...";
       } else {
         state.phase = 'DONE';
       }
    }

    // 2. Draw Path
    state.history.push({ x: mapX(state.t), y: mapY(state.temp) });
    
    ctx.beginPath();
    ctx.strokeStyle = "blue"; ctx.lineWidth = 4; ctx.lineJoin = "round";
    ctx.moveTo(state.history[0].x, state.history[0].y);
    for(let p of state.history) ctx.lineTo(p.x, p.y);
    ctx.stroke();
    
    // Tracer Head
    let last = state.history[state.history.length-1];
    ctx.fillStyle = "blue"; ctx.beginPath(); 
    ctx.arc(last.x, last.y, 6, 0, Math.PI*2); ctx.fill();

    // 3. Completion
    if(state.phase === 'DONE') {
      clearInterval(animationId);
      let msg = "";
      if(id === 'P') msg = "Result: 100% Martensite";
      if(id === 'Q') msg = "Result: 100% Coarse Pearlite (Crossed Finish)";
      if(id === 'R') msg = "Result: 100% Bainite (Crossed Finish)";
      if(id === 'S') msg = "Result: Bainite (50%) + Martensite (50%) [Interrupted]";
      statusEl.innerHTML = `<strong>${msg}</strong>`;
    }

  }, 20);
}

// Init
drawBackground();
</script>
</body>
</html>
