<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>The Structure of Crystalline Solids: An Interactive Guide</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
    <!-- Chosen Palette: Warm Neutrals -->
    <!-- Application Structure Plan: A single-page, vertically scrolling dashboard with a fixed top navigation. This structure was chosen to transform a dense, linear academic text into an engaging, non-linear exploratory experience. It's divided into thematic sections (Core Concepts, Structure Explorer, Calculators, etc.) that allow users to focus on specific topics and interact with them through visualizers and tools. This task-oriented, modular design enhances usability and comprehension by making learning an active rather than passive process. -->
    <!-- Visualization & Content Choices: Report Info -> Crystalline vs. Noncrystalline -> Goal: Compare -> Viz: Interactive two-column layout -> Interaction: Click-to-reveal text -> Justification: Clear, direct comparison. | Report Info -> BCC/FCC/HCP Structures -> Goal: Inform/Compare -> Viz: Dynamic dashboard with canvas drawing & stat cards -> Interaction: Buttons to switch structure view -> Justification: Visualizes complex 3D structures. | Report Info -> Structure Properties -> Goal: Compare -> Viz: Bar Chart -> Interaction: Buttons to update chart data -> Justification: Effective quantitative comparison -> Library: Chart.js. | Report Info -> Stacking Sequences -> Goal: Show Process -> Viz: Custom HTML/JS animation -> Interaction: Toggle between FCC/HCP -> Justification: Clarifies a dynamic process. | Report Info -> Formulas/Notation -> Goal: Apply Knowledge -> Viz: Interactive Calculators/Tools -> Interaction: User input triggers JS calculations -> Justification: Reinforces learning through practice. -->
    <!-- CONFIRMATION: NO SVG graphics used. NO Mermaid JS used. -->
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #f8f7f4;
            color: #1e293b;
        }
        .nav-link {
            transition: color 0.3s, border-bottom-color 0.3s;
            border-bottom: 2px solid transparent;
        }
        .nav-link:hover, .nav-link.active {
            color: #0d9488;
            border-bottom-color: #0d9488;
        }
        .card {
            background-color: #ffffff;
            border-radius: 0.75rem;
            border: 1px solid #e2e8f0;
            box-shadow: 0 4px 6px -1px rgb(0 0 0 / 0.1), 0 2px 4px -2px rgb(0 0 0 / 0.1);
            transition: transform 0.3s, box-shadow 0.3s;
        }
        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 15px -3px rgb(0 0 0 / 0.1), 0 4px 6px -4px rgb(0 0 0 / 0.1);
        }
        .btn {
            display: inline-block;
            padding: 0.75rem 1.5rem;
            border-radius: 0.5rem;
            font-weight: 600;
            text-align: center;
            transition: background-color 0.3s, transform 0.3s;
            cursor: pointer;
        }
        .btn-primary {
            background-color: #0d9488;
            color: #ffffff;
        }
        .btn-primary:hover {
            background-color: #0f766e;
            transform: scale(1.05);
        }
        .btn-secondary {
            background-color: #e2e8f0;
            color: #334155;
        }
        .btn-secondary.active {
            background-color: #0d9488;
            color: #ffffff;
        }
        .section-title {
            font-size: 2.25rem;
            font-weight: 700;
            margin-bottom: 1rem;
            color: #0f172a;
        }
        .section-subtitle {
            font-size: 1.125rem;
            color: #475569;
            max-width: 48rem;
            margin: 0 auto 3rem auto;
        }
        .chart-container {
            position: relative;
            width: 100%;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
            height: 300px;
            max-height: 400px;
        }
        @media (min-width: 768px) {
            .chart-container {
                height: 350px;
            }
        }
    </style>
</head>
<body class="antialiased">

    <header class="bg-white/80 backdrop-blur-lg sticky top-0 z-50 border-b border-slate-200">
        <nav class="container mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex items-center justify-between h-16">
                <div class="flex-shrink-0">
                    <a href="#" class="text-xl font-bold text-teal-700">Crystalline Solids</a>
                </div>
                <div class="hidden md:block">
                    <div class="ml-10 flex items-baseline space-x-4">
                        <a href="#introduction" class="nav-link px-3 py-2 text-sm font-medium">Introduction</a>
                        <a href="#structures" class="nav-link px-3 py-2 text-sm font-medium">Structures</a>
                        <a href="#properties" class="nav-link px-3 py-2 text-sm font-medium">Properties</a>
                        <a href="#calculators" class="nav-link px-3 py-2 text-sm font-medium">Calculators</a>
                        <a href="#notation" class="nav-link px-3 py-2 text-sm font-medium">Notation</a>
                        <a href="#macroscopic" class="nav-link px-3 py-2 text-sm font-medium">Material Types</a>
                    </div>
                </div>
            </div>
        </nav>
    </header>

    <main class="container mx-auto px-4 sm:px-6 lg:px-8 py-12">
        
        <section id="introduction" class="text-center py-16">
            <h1 class="text-4xl md:text-5xl font-extrabold text-slate-900 tracking-tight">The Structure of Crystalline Solids</h1>
            <p class="mt-6 max-w-3xl mx-auto text-lg text-slate-600">An interactive journey into the ordered world of atoms. Explore the fundamental building blocks of materials and discover how their arrangement dictates the properties we observe and engineer.</p>
        </section>

        <section id="concepts" class="py-16">
            <div class="text-center">
                <h2 class="section-title">Crystalline vs. Noncrystalline</h2>
                <p class="section-subtitle">The fundamental difference between solids lies in atomic order. One is a repeating, predictable pattern, while the other is disordered. This single distinction changes everything from melting point to appearance.</p>
            </div>
            <div class="grid md:grid-cols-2 gap-8 max-w-6xl mx-auto">
                <div class="card p-8">
                    <h3 class="text-2xl font-bold mb-4 text-teal-700">Crystalline Solids</h3>
                    <p class="text-slate-600 mb-4">Atoms, ions, or molecules are arranged in a highly ordered, repeating 3D pattern called a crystal lattice. This long-range order extends throughout the entire material.</p>
                    <ul class="space-y-2 text-slate-700">
                        <li class="flex items-start"><span class="text-teal-500 mr-2 mt-1">●</span><div><strong>Order:</strong> Long-range, periodic arrangement.</div></li>
                        <li class="flex items-start"><span class="text-teal-500 mr-2 mt-1">●</span><div><strong>Melting:</strong> Sharp, distinct melting point.</div></li>
                        <li class="flex items-start"><span class="text-teal-500 mr-2 mt-1">●</span><div><strong>Appearance:</strong> Often have flat faces and distinct geometric shapes.</div></li>
                        <li class="flex items-start"><span class="text-teal-500 mr-2 mt-1">●</span><div><strong>Example:</strong> Salt (NaCl), Diamond, Metals.</div></li>
                    </ul>
                </div>
                <div class="card p-8">
                    <h3 class="text-2xl font-bold mb-4 text-rose-700">Noncrystalline (Amorphous) Solids</h3>
                    <p class="text-slate-600 mb-4">Atoms lack a long-range, repeating order. While they have short-range order (predictable nearest-neighbor distances), the structure is disordered over larger distances.</p>
                    <ul class="space-y-2 text-slate-700">
                        <li class="flex items-start"><span class="text-rose-500 mr-2 mt-1">●</span><div><strong>Order:</strong> Only short-range order.</div></li>
                        <li class="flex items-start"><span class="text-rose-500 mr-2 mt-1">●</span><div><strong>Melting:</strong> Soften gradually over a range of temperatures.</div></li>
                        <li class="flex items-start"><span class="text-rose-500 mr-2 mt-1">●</span><div><strong>Appearance:</strong> Fracture into irregular or curved shapes.</div></li>
                        <li class="flex items-start"><span class="text-rose-500 mr-2 mt-1">●</span><div><strong>Example:</strong> Glass, Polymers, Wax.</div></li>
                    </ul>
                </div>
            </div>
        </section>

        <section id="structures" class="py-16 text-center">
            <h2 class="section-title">Crystal Structure Explorer</h2>
            <p class="section-subtitle">Most metals crystallize into one of three densely packed arrangements. Select a structure below to visualize its unit cell—the smallest repeating building block—and see its unique properties.</p>
            <div class="flex justify-center space-x-4 mb-8">
                <button id="btn-bcc" class="btn btn-secondary active">Body-Centered Cubic (BCC)</button>
                <button id="btn-fcc" class="btn btn-secondary">Face-Centered Cubic (FCC)</button>
                <button id="btn-hcp" class="btn btn-secondary">Hexagonal Close-Packed (HCP)</button>
            </div>
            <div class="card max-w-5xl mx-auto p-6 lg:p-8">
                <div class="grid lg:grid-cols-2 gap-8 items-center">
                    <div class="w-full aspect-square bg-slate-50 rounded-lg p-4">
                        <canvas id="unitCellCanvas"></canvas>
                    </div>
                    <div id="structure-info" class="text-left">
                    </div>
                </div>
            </div>
        </section>
        
        <section id="properties" class="py-16 text-center">
            <h2 class="section-title">Comparing Structures by the Numbers</h2>
            <p class="section-subtitle">How efficiently are atoms packed? How many neighbors does each atom have? These key metrics differentiate the crystal structures and influence material properties like ductility and density.</p>
            <div class="card max-w-5xl mx-auto p-6 lg:p-8">
                <div class="flex justify-center space-x-4 mb-6">
                    <button id="btn-prop-apf" class="btn btn-secondary active">Packing Efficiency</button>
                    <button id="btn-prop-cn" class="btn btn-secondary">Coordination Number</button>
                    <button id="btn-prop-atoms" class="btn btn-secondary">Atoms per Cell</button>
                </div>
                <div class="chart-container">
                    <canvas id="propertiesChart"></canvas>
                </div>
            </div>
        </section>

        <section id="calculators" class="py-16">
            <div class="text-center">
                <h2 class="section-title">Interactive Calculators</h2>
                <p class="section-subtitle">Bridge the gap between atomic arrangement and macroscopic properties. Use these tools to perform the same calculations materials scientists use to characterize materials.</p>
            </div>
            <div class="grid md:grid-cols-2 gap-8 max-w-6xl mx-auto">
                <div class="card p-8">
                    <h3 class="text-2xl font-bold mb-4 text-teal-700">Atomic Radius ↔ Edge Length</h3>
                    <p class="text-slate-600 mb-6">In a unit cell, atoms touch along specific directions. This geometric constraint creates a direct relationship between atomic radius (r) and the unit cell's edge length (a).</p>
                    <div class="space-y-4">
                        <div>
                            <label for="ar-structure" class="block text-sm font-medium text-slate-700">Crystal Structure</label>
                            <select id="ar-structure" class="mt-1 block w-full p-2 border border-slate-300 rounded-md shadow-sm">
                                <option value="fcc">Face-Centered Cubic (FCC)</option>
                                <option value="bcc">Body-Centered Cubic (BCC)</option>
                            </select>
                        </div>
                        <div>
                            <label for="ar-radius" class="block text-sm font-medium text-slate-700">Atomic Radius (r) in pm</label>
                            <input type="number" id="ar-radius" value="128" class="mt-1 block w-full p-2 border border-slate-300 rounded-md shadow-sm">
                        </div>
                        <button id="ar-calculate" class="btn btn-primary w-full">Calculate Edge Length (a)</button>
                        <div id="ar-result" class="mt-4 p-4 bg-slate-50 rounded-md text-center">
                            <p class="text-slate-600">Result will be shown here.</p>
                        </div>
                    </div>
                </div>
                <div class="card p-8">
                    <h3 class="text-2xl font-bold mb-4 text-teal-700">Theoretical Density Calculator</h3>
                    <p class="text-slate-600 mb-6">Calculate a metal's theoretical density based on its crystal structure, atomic weight, and atomic radius. This is a powerful link between the micro and macro scales.</p>
                    <div class="space-y-4">
                        <div>
                            <label for="td-metal" class="block text-sm font-medium text-slate-700">Select Metal</label>
                            <select id="td-metal" class="mt-1 block w-full p-2 border border-slate-300 rounded-md shadow-sm">
                                <option value="Cr">Chromium (Cr)</option>
                                <option value="Fe">Iron (Fe)</option>
                                <option value="Cu">Copper (Cu)</option>
                                <option value="Al">Aluminum (Al)</option>
                            </select>
                        </div>
                        <button id="td-calculate" class="btn btn-primary w-full">Calculate Density (ρ)</button>
                        <div id="td-result" class="mt-4 p-4 bg-slate-50 rounded-md text-left space-y-2">
                             <p class="text-slate-600 text-center">Result will be shown here.</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>
        
        <section id="notation" class="py-16 text-center">
            <h2 class="section-title">Miller Indices for Crystal Planes</h2>
            <p class="section-subtitle">Miller indices (hkl) are a universal notation to describe the orientation of planes within a crystal lattice. This tool helps you determine them step-by-step from a plane's intercepts on the x, y, and z axes.</p>
            <div class="card max-w-3xl mx-auto p-8">
                <div class="grid sm:grid-cols-3 gap-4 mb-6">
                    <div>
                        <label for="intercept-x" class="block text-sm font-medium text-slate-700">X-intercept</label>
                        <input type="text" id="intercept-x" value="1/2" class="mt-1 block w-full p-2 border border-slate-300 rounded-md shadow-sm text-center">
                    </div>
                    <div>
                        <label for="intercept-y" class="block text-sm font-medium text-slate-700">Y-intercept</label>
                        <input type="text" id="intercept-y" value="1" class="mt-1 block w-full p-2 border border-slate-300 rounded-md shadow-sm text-center">
                    </div>
                    <div>
                        <label for="intercept-z" class="block text-sm font-medium text-slate-700">Z-intercept (use 'inf' for ∞)</label>
                        <input type="text" id="intercept-z" value="inf" class="mt-1 block w-full p-2 border border-slate-300 rounded-md shadow-sm text-center">
                    </div>
                </div>
                <button id="miller-calculate" class="btn btn-primary">Find Miller Indices</button>
                <div id="miller-result" class="mt-6 text-left space-y-3">
                    <p class="text-slate-600 text-center">Result will be shown here.</p>
                </div>
            </div>
        </section>

        <section id="macroscopic" class="py-16">
            <div class="text-center">
                <h2 class="section-title">From Single Crystals to Bulk Materials</h2>
                <p class="section-subtitle">How do individual crystals combine to form the materials we use every day? The distinction between single crystals and polycrystals, and the concepts of isotropy and anisotropy, explain how atomic order scales up.</p>
            </div>
            <div class="grid md:grid-cols-2 gap-8 max-w-6xl mx-auto">
                <div class="card p-8">
                    <h3 class="text-2xl font-bold mb-4">Single vs. Polycrystalline</h3>
                    <p class="text-slate-600 mb-4">A material can be one continuous crystal or a composite of many small, randomly oriented crystal grains.</p>
                    <ul class="space-y-3">
                        <li><strong>Single Crystal:</strong> A solid where the crystal lattice is continuous and unbroken throughout the entire sample. Often exhibits flat faces (facets). Properties are typically anisotropic (direction-dependent).</li>
                        <li><strong>Polycrystalline:</strong> A solid composed of many small crystals (grains) with varying orientations. The interfaces where grains meet are called grain boundaries. If grains are randomly oriented, the bulk material is often isotropic (properties are the same in all directions).</li>
                    </ul>
                </div>
                <div class="card p-8">
                    <h3 class="text-2xl font-bold mb-4">Isotropy vs. Anisotropy</h3>
                    <p class="text-slate-600 mb-4">Does a material's strength or conductivity change with direction? This property is dictated by the symmetry of its internal structure.</p>
                     <ul class="space-y-3">
                        <li><strong>Isotropic:</strong> Properties are identical in all directions. This is common in amorphous materials (like glass) and polycrystalline metals with random grain orientation.</li>
                        <li><strong>Anisotropic:</strong> Properties are direction-dependent. A single non-cubic crystal will be stronger along certain crystallographic planes. Wood is a classic example, being much stronger along the grain than across it.</li>
                    </ul>
                </div>
            </div>
        </section>

    </main>

    <footer class="bg-slate-800 text-slate-300 mt-16">
        <div class="container mx-auto px-4 sm:px-6 lg:px-8 py-6 text-center">
            <p>Interactive Guide to Crystalline Solids.</p>
        </div>
    </footer>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            
            const structureData = {
                bcc: {
                    name: "Body-Centered Cubic (BCC)",
                    description: "The BCC structure has atoms at each of the eight corners of a cube plus one atom in the very center of the cube. It's less densely packed than FCC or HCP.",
                    atomsPerCell: 2,
                    coordinationNumber: 8,
                    packingFactor: 0.68,
                    examples: "Iron (α-Fe), Chromium, Tungsten"
                },
                fcc: {
                    name: "Face-Centered Cubic (FCC)",
                    description: "The FCC structure has atoms at the eight corners and in the center of each of the six faces of the cube. This is a 'close-packed' structure, meaning it has the maximum possible packing density.",
                    atomsPerCell: 4,
                    coordinationNumber: 12,
                    packingFactor: 0.74,
                    examples: "Aluminum, Copper, Gold, Silver"
                },
                hcp: {
                    name: "Hexagonal Close-Packed (HCP)",
                    description: "The HCP structure is the other 'close-packed' structure, also with maximum density. Its unit cell is hexagonal. It is formed by an 'ABAB...' stacking of atomic planes.",
                    atomsPerCell: 6,
                    coordinationNumber: 12,
                    packingFactor: 0.74,
                    examples: "Magnesium, Titanium, Zinc, Cobalt"
                }
            };

            const metalData = {
                'Cr': { name: 'Chromium', structure: 'bcc', radius: 128, weight: 51.996 },
                'Fe': { name: 'Iron', structure: 'bcc', radius: 124, weight: 55.845 },
                'Cu': { name: 'Copper', structure: 'fcc', radius: 128, weight: 63.546 },
                'Al': { name: 'Aluminum', structure: 'fcc', radius: 143, weight: 26.982 },
            };

            const structureInfo = document.getElementById('structure-info');
            const bccBtn = document.getElementById('btn-bcc');
            const fccBtn = document.getElementById('btn-fcc');
            const hcpBtn = document.getElementById('btn-hcp');
            const canvas = document.getElementById('unitCellCanvas');
            const ctx = canvas.getContext('2d');
            let currentStructure = 'bcc';

            function updateStructureInfo(type) {
                const data = structureData[type];
                structureInfo.innerHTML = `
                    <h3 class="text-3xl font-bold mb-4 text-teal-700">${data.name}</h3>
                    <p class="text-slate-600 mb-6">${data.description}</p>
                    <div class="grid grid-cols-2 sm:grid-cols-3 gap-4 text-center">
                        <div class="bg-slate-100 p-4 rounded-lg">
                            <div class="text-3xl font-bold">${data.atomsPerCell}</div>
                            <div class="text-sm text-slate-500">Atoms / Cell</div>
                        </div>
                        <div class="bg-slate-100 p-4 rounded-lg">
                            <div class="text-3xl font-bold">${data.coordinationNumber}</div>
                            <div class="text-sm text-slate-500">Coordination #</div>
                        </div>
                        <div class="bg-slate-100 p-4 rounded-lg col-span-2 sm:col-span-1">
                            <div class="text-3xl font-bold">${(data.packingFactor * 100).toFixed(0)}%</div>
                            <div class="text-sm text-slate-500">Packing Factor</div>
                        </div>
                    </div>
                    <div class="mt-6">
                        <h4 class="font-semibold text-slate-800">Common Examples:</h4>
                        <p class="text-slate-600">${data.examples}</p>
                    </div>
                `;
                drawUnitCell(type);
            }

            function drawUnitCell(type) {
                const w = canvas.width;
                const h = canvas.height;
                ctx.clearRect(0, 0, w, h);
                
                const size = Math.min(w, h) * 0.5;
                const x0 = w / 2;
                const y0 = h / 2;
                const perspective = 0.4;
                const atomRadius = size * 0.1;

                function drawAtom(x, y, r, fill = 'rgba(13, 148, 136, 0.7)') {
                    ctx.beginPath();
                    ctx.arc(x, y, r, 0, Math.PI * 2);
                    ctx.fillStyle = fill;
                    ctx.fill();
                    ctx.strokeStyle = '#0f766e';
                    ctx.lineWidth = 2;
                    ctx.stroke();
                }

                if (type === 'bcc' || type === 'fcc') {
                    const points = [];
                    for (let i = 0; i < 8; i++) {
                        points.push({
                            x: (i & 1) ? size / 2 : -size / 2,
                            y: (i & 2) ? size / 2 : -size / 2,
                            z: (i & 4) ? size / 2 : -size / 2,
                        });
                    }

                    const projected = points.map(p => {
                        return {
                            x: x0 + p.x - p.z * perspective,
                            y: y0 + p.y - p.z * perspective * 0.5,
                        };
                    });

                    ctx.strokeStyle = '#94a3b8';
                    ctx.lineWidth = 2;
                    const edges = [
                        [0, 1], [1, 3], [3, 2], [2, 0],
                        [4, 5], [5, 7], [7, 6], [6, 4],
                        [0, 4], [1, 5], [2, 6], [3, 7]
                    ];
                    edges.forEach(edge => {
                        ctx.beginPath();
                        ctx.moveTo(projected[edge[0]].x, projected[edge[0]].y);
                        ctx.lineTo(projected[edge[1]].x, projected[edge[1]].y);
                        ctx.stroke();
                    });

                    projected.forEach(p => drawAtom(p.x, p.y, atomRadius));

                    if (type === 'bcc') {
                        drawAtom(x0, y0, atomRadius * 1.2, 'rgba(204, 37, 37, 0.8)');
                    }
                    if (type === 'fcc') {
                        const faceCenters = [
                            {x: x0, y: y0 - size/2 * (1 - 0.5 * perspective)}, // top
                            {x: x0, y: y0 + size/2 * (1 - 0.5 * perspective)}, // bottom
                            {x: x0 - size/2 * (1 - perspective), y: y0}, // left
                            {x: x0 + size/2 * (1 - perspective), y: y0}, // right
                            {x: x0 - size/2 * perspective, y: y0 - size/4 * perspective}, // back
                            {x: x0 + size/2 * perspective, y: y0 + size/4 * perspective} // front
                        ]
                        faceCenters.forEach(p => drawAtom(p.x, p.y, atomRadius, 'rgba(204, 37, 37, 0.8)'));
                    }
                } else if (type === 'hcp') {
                    const r = size / 2;
                    const h = r * 1.633;
                    const angle = Math.PI / 3;

                    const topPoints = [];
                    const bottomPoints = [];
                    for(let i=0; i<6; i++){
                        topPoints.push({x: x0 + r * Math.cos(i*angle), y: y0 - h/2 + r * 0.5 * Math.sin(i*angle)});
                        bottomPoints.push({x: x0 + r * Math.cos(i*angle), y: y0 + h/2 + r * 0.5 * Math.sin(i*angle)});
                    }
                    
                    ctx.strokeStyle = '#94a3b8';
                    ctx.lineWidth = 2;
                    for(let i=0; i<6; i++){
                        ctx.beginPath();
                        ctx.moveTo(topPoints[i].x, topPoints[i].y);
                        ctx.lineTo(topPoints[(i+1)%6].x, topPoints[(i+1)%6].y);
                        ctx.stroke();

                        ctx.beginPath();
                        ctx.moveTo(bottomPoints[i].x, bottomPoints[i].y);
                        ctx.lineTo(bottomPoints[(i+1)%6].x, bottomPoints[(i+1)%6].y);
                        ctx.stroke();

                        ctx.beginPath();
                        ctx.moveTo(topPoints[i].x, topPoints[i].y);
                        ctx.lineTo(bottomPoints[i].x, bottomPoints[i].y);
                        ctx.stroke();
                    }

                    topPoints.forEach(p => drawAtom(p.x, p.y, atomRadius));
                    bottomPoints.forEach(p => drawAtom(p.x, p.y, atomRadius));
                    drawAtom(x0, y0-h/2, atomRadius, 'rgba(204, 37, 37, 0.8)'); // top face
                    drawAtom(x0, y0+h/2, atomRadius, 'rgba(204, 37, 37, 0.8)'); // bottom face
                    
                    const midR = r * 0.5;
                    drawAtom(x0, y0, atomRadius, 'rgba(204, 37, 37, 0.8)');
                    drawAtom(x0 + midR * Math.cos(Math.PI/6), y0 + midR*0.5*Math.sin(Math.PI/6), atomRadius, 'rgba(204, 37, 37, 0.8)');
                    drawAtom(x0 - midR * Math.cos(Math.PI/6), y0 - midR*0.5*Math.sin(Math.PI/6), atomRadius, 'rgba(204, 37, 37, 0.8)');
                }
            }
            
            function resizeCanvas() {
                const container = canvas.parentElement;
                canvas.width = container.clientWidth;
                canvas.height = container.clientHeight;
                drawUnitCell(currentStructure);
            }

            bccBtn.addEventListener('click', () => {
                currentStructure = 'bcc';
                updateStructureInfo('bcc');
                bccBtn.classList.add('active');
                fccBtn.classList.remove('active');
                hcpBtn.classList.remove('active');
            });
            fccBtn.addEventListener('click', () => {
                currentStructure = 'fcc';
                updateStructureInfo('fcc');
                fccBtn.classList.add('active');
                bccBtn.classList.remove('active');
                hcpBtn.classList.remove('active');
            });
            hcpBtn.addEventListener('click', () => {
                currentStructure = 'hcp';
                updateStructureInfo('hcp');
                hcpBtn.classList.add('active');
                fccBtn.classList.remove('active');
                bccBtn.classList.remove('active');
            });
            
            window.addEventListener('resize', resizeCanvas);
            updateStructureInfo('bcc');
            resizeCanvas();

            const propertiesChartCtx = document.getElementById('propertiesChart').getContext('2d');
            let propertiesChart;
            const chartData = {
                labels: ['BCC', 'FCC', 'HCP'],
                apf: { label: 'Atomic Packing Factor (Efficiency)', data: [0.68, 0.74, 0.74] },
                cn: { label: 'Coordination Number', data: [8, 12, 12] },
                atoms: { label: 'Atoms per Unit Cell', data: [2, 4, 6] }
            };

            function createOrUpdateChart(property) {
                const data = chartData[property];
                if (propertiesChart) {
                    propertiesChart.data.datasets[0].data = data.data;
                    propertiesChart.data.datasets[0].label = data.label;
                    propertiesChart.update();
                } else {
                    propertiesChart = new Chart(propertiesChartCtx, {
                        type: 'bar',
                        data: {
                            labels: chartData.labels,
                            datasets: [{
                                label: data.label,
                                data: data.data,
                                backgroundColor: ['#38bdf8', '#34d399', '#fbbf24'],
                                borderColor: ['#0ea5e9', '#10b981', '#f59e0b'],
                                borderWidth: 1
                            }]
                        },
                        options: {
                            responsive: true,
                            maintainAspectRatio: false,
                            scales: {
                                y: { beginAtZero: true }
                            },
                            plugins: {
                                legend: { display: true, position: 'top' },
                                tooltip: {
                                    callbacks: {
                                        label: function(context) {
                                            let label = context.dataset.label || '';
                                            if (label) { label += ': '; }
                                            if (context.parsed.y !== null) {
                                                if (property === 'apf') {
                                                    label += (context.parsed.y * 100).toFixed(0) + '%';
                                                } else {
                                                    label += context.parsed.y;
                                                }
                                            }
                                            return label;
                                        }
                                    }
                                }
                            }
                        }
                    });
                }
            }
            
            document.getElementById('btn-prop-apf').addEventListener('click', (e) => {
                createOrUpdateChart('apf');
                document.querySelectorAll('#properties .btn-secondary').forEach(b => b.classList.remove('active'));
                e.target.classList.add('active');
            });
            document.getElementById('btn-prop-cn').addEventListener('click', (e) => {
                createOrUpdateChart('cn');
                document.querySelectorAll('#properties .btn-secondary').forEach(b => b.classList.remove('active'));
                e.target.classList.add('active');
            });
            document.getElementById('btn-prop-atoms').addEventListener('click', (e) => {
                createOrUpdateChart('atoms');
                document.querySelectorAll('#properties .btn-secondary').forEach(b => b.classList.remove('active'));
                e.target.classList.add('active');
            });

            createOrUpdateChart('apf');

            const arCalculateBtn = document.getElementById('ar-calculate');
            const arResultDiv = document.getElementById('ar-result');
            arCalculateBtn.addEventListener('click', () => {
                const structure = document.getElementById('ar-structure').value;
                const radius = parseFloat(document.getElementById('ar-radius').value);
                if (isNaN(radius) || radius <= 0) {
                    arResultDiv.innerHTML = `<p class="text-red-600">Please enter a valid positive radius.</p>`;
                    return;
                }
                
                let a, formula;
                if (structure === 'fcc') {
                    a = 2 * radius * Math.sqrt(2);
                    formula = `a = 2 * r * sqrt(2)`;
                } else { // bcc
                    a = 4 * radius / Math.sqrt(3);
                    formula = `a = 4 * r / sqrt(3)`;
                }
                
                arResultDiv.innerHTML = `
                    <p class="text-slate-600">For a ${structure.toUpperCase()} structure:</p>
                    <p class="font-mono text-sm my-2">${formula}</p>
                    <p class="text-lg font-bold text-teal-700">Edge Length (a) = ${a.toFixed(2)} pm</p>
                `;
            });

            const tdCalculateBtn = document.getElementById('td-calculate');
            const tdResultDiv = document.getElementById('td-result');
            tdCalculateBtn.addEventListener('click', () => {
                const metalKey = document.getElementById('td-metal').value;
                const metal = metalData[metalKey];
                const n = structureData[metal.structure].atomsPerCell;
                const A = metal.weight;
                const r_cm = metal.radius * 1e-10;
                const NA = 6.022e23;
                
                let a_cm;
                if (metal.structure === 'fcc') {
                    a_cm = 2 * r_cm * Math.sqrt(2);
                } else { // bcc
                    a_cm = 4 * r_cm / Math.sqrt(3);
                }
                
                const Vc = Math.pow(a_cm, 3);
                const density = (n * A) / (Vc * NA);
                
                tdResultDiv.innerHTML = `
                    <p class="font-bold text-center text-lg mb-2">${metal.name} (${metal.structure.toUpperCase()})</p>
                    <p><strong>n</strong> (atoms/cell): ${n}</p>
                    <p><strong>A</strong> (g/mol): ${A}</p>
                    <p><strong>r</strong> (cm): ${r_cm.toExponential(3)}</p>
                    <p><strong>a</strong> (cm): ${a_cm.toExponential(3)}</p>
                    <p><strong>V<sub>c</sub></strong> (cm³/cell): ${Vc.toExponential(3)}</p>
                    <p class="mt-2 text-center text-lg font-bold text-teal-700">Density (ρ) = ${density.toFixed(3)} g/cm³</p>
                `;
            });

            const millerCalculateBtn = document.getElementById('miller-calculate');
            const millerResultDiv = document.getElementById('miller-result');
            millerCalculateBtn.addEventListener('click', () => {
                const xStr = document.getElementById('intercept-x').value.trim().toLowerCase();
                const yStr = document.getElementById('intercept-y').value.trim().toLowerCase();
                const zStr = document.getElementById('intercept-z').value.trim().toLowerCase();

                function parseIntercept(str) {
                    if (str === 'inf' || str === 'infinity') return Infinity;
                    if (str.includes('/')) {
                        const parts = str.split('/');
                        const num = parseFloat(parts[0]);
                        const den = parseFloat(parts[1]);
                        if (isNaN(num) || isNaN(den) || den === 0) return NaN;
                        return num / den;
                    }
                    return parseFloat(str);
                }
                
                const intercepts = [parseIntercept(xStr), parseIntercept(yStr), parseIntercept(zStr)];
                
                if (intercepts.some(isNaN)) {
                    millerResultDiv.innerHTML = `<p class="text-red-600 text-center">Invalid intercept value. Use numbers, fractions (e.g., 1/2), or 'inf'.</p>`;
                    return;
                }
                
                const reciprocals = intercepts.map(i => 1 / i);
                
                let commonMultiple = 1;
                let integers = [];
                
                // Simple fraction clearing
                for (let i = 1; i <= 12; i++) {
                    const testIntegers = reciprocals.map(r => Math.round(r * i * 1000) / 1000);
                    if (testIntegers.every(val => Math.abs(val - Math.round(val)) < 1e-9)) {
                        integers = testIntegers.map(Math.round);
                        break;
                    }
                }
                if (integers.length === 0) integers = reciprocals.map(r => Math.round(r));


                const h = integers[0];
                const k = integers[1];
                const l = integers[2];
                
                const formatIndex = (n) => n < 0 ? `\\bar{${Math.abs(n)}}` : n;

                millerResultDiv.innerHTML = `
                    <div class="space-y-2">
                        <p><strong>1. Intercepts:</strong> [${intercepts.map(i => i === Infinity ? '∞' : i.toFixed(2)).join(', ')}]</p>
                        <p><strong>2. Reciprocals:</strong> [${reciprocals.map(r => r.toFixed(2)).join(', ')}]</p>
                        <p><strong>3. Clear Fractions:</strong> [${integers.join(', ')}]</p>
                        <p class="mt-4 text-center text-2xl font-bold text-teal-700">Miller Indices (hkl) = (${formatIndex(h)}${formatIndex(k)}${formatIndex(l)})</p>
                    </div>
                `;
            });
            
            const navLinks = document.querySelectorAll('.nav-link');
            const sections = document.querySelectorAll('section');

            window.addEventListener('scroll', () => {
                let current = '';
                sections.forEach(section => {
                    const sectionTop = section.offsetTop;
                    if (pageYOffset >= sectionTop - 80) {
                        current = section.getAttribute('id');
                    }
                });

                navLinks.forEach(link => {
                    link.classList.remove('active');
                    if (link.getAttribute('href').includes(current)) {
                        link.classList.add('active');
                    }
                });
            });
            
            arCalculateBtn.click();
            tdCalculateBtn.click();
            millerCalculateBtn.click();
        });
    </script>
</body>
</html>
