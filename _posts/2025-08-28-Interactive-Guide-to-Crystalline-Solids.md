<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>The Structure of Crystalline Solids: An Interactive Guide</title>
    <!-- Tailwind CSS for modern, responsive design -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Chart.js for interactive data visualization -->
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <!-- Three.js for 3D visualization of crystal structures -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
    <!-- OrbitControls for mouse interaction (rotate, pan, zoom) with the 3D scene -->
    <script src="https://cdn.jsdelivr.net/npm/three@0.128.0/examples/js/controls/OrbitControls.js"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
    <!-- Custom styles to complement Tailwind's utility classes and create a polished look -->
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #f0f4f8;
            color: #1e293b;
        }
        .nav-link {
            transition: color 0.3s, border-bottom-color 0.3s, transform 0.2s;
            border-bottom: 2px solid transparent;
        }
        .nav-link:hover {
            color: #0d9488;
        }
        .nav-link.active {
            color: #0f172a;
            font-weight: 600;
            border-bottom-color: #0f172a;
        }
        .card {
            background-color: #ffffff;
            border-radius: 1.5rem;
            border: 1px solid #e2e8f0;
            box-shadow: 0 10px 20px -5px rgb(0 0 0 / 0.05), 0 4px 6px -2px rgb(0 0 0 / 0.05);
            transition: transform 0.3s, box-shadow 0.3s;
        }
        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 20px 30px -5px rgb(0 0 0 / 0.1), 0 10px 15px -3px rgb(0 0 0 / 0.1);
        }
        .btn {
            padding: 0.75rem 1.75rem;
            border-radius: 9999px;
            font-weight: 600;
            text-align: center;
            transition: background-color 0.3s, transform 0.3s;
            cursor: pointer;
        }
        .btn-primary {
            background-color: #0d9488;
            color: #ffffff;
            box-shadow: 0 4px 6px -1px rgb(13 148 136 / 0.2), 0 2px 4px -2px rgb(13 148 136 / 0.2);
        }
        .btn-primary:hover {
            background-color: #0f766e;
            transform: scale(1.02);
        }
        .btn-secondary {
            background-color: #e2e8f0;
            color: #334155;
            transition: background-color 0.3s, color 0.3s;
        }
        .btn-secondary.active {
            background-color: #0d9488;
            color: #ffffff;
            box-shadow: 0 4px 6px -1px rgb(13 148 136 / 0.2), 0 2px 4px -2px rgb(13 148 136 / 0.2);
        }
        .section-title {
            font-size: 2.25rem;
            font-weight: 700;
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
            height: 300px;
            width: 100%;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
        }
        @media (min-width: 768px) {
            .chart-container {
                height: 400px;
            }
        }
        #unitCellCanvasContainer {
            position: relative;
            width: 100%;
            height: 500px;
            background-color: #f8f8f8;
            border-radius: 1rem;
        }
    </style>
</head>
<body class="antialiased">

    <!-- Sticky Navigation Header -->
    <header class="bg-white/80 backdrop-blur-lg sticky top-0 z-50 border-b border-slate-200">
        <nav class="container mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex items-center justify-between h-16">
                <div class="flex-shrink-0">
                    <a href="#" class="text-2xl font-bold text-teal-700">Crystalline Solids</a>
                </div>
                <div class="hidden md:block">
                    <div class="ml-10 flex items-baseline space-x-4">
                        <a href="#introduction" class="nav-link px-3 py-2 text-sm font-medium">Introduction</a>
                        <a href="#structures" class="nav-link px-3 py-2 text-sm font-medium">Structures</a>
                        <a href="#properties" class="nav-link px-3 py-2 text-sm font-medium">Properties</a>
                        <a href="#stacking" class="nav-link px-3 py-2 text-sm font-medium">Stacking</a>
                        <a href="#calculators" class="nav-link px-3 py-2 text-sm font-medium">Calculators</a>
                        <a href="#notation" class="nav-link px-3 py-2 text-sm font-medium">Notation</a>
                    </div>
                </div>
            </div>
        </nav>
    </header>

    <main class="container mx-auto px-4 sm:px-6 lg:px-8 py-12">
        
        <!-- Hero Section -->
        <section id="introduction" class="text-center py-16">
            <h1 class="text-4xl md:text-6xl font-extrabold text-slate-900 tracking-tight">The Structure of Crystalline Solids</h1>
            <p class="mt-6 max-w-4xl mx-auto text-lg text-slate-600">An interactive journey into the ordered world of atoms. Explore the fundamental building blocks of materials and discover how their arrangement dictates the properties we observe and engineer.</p>
        </section>

        <!-- Crystalline vs. Noncrystalline -->
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

        <!-- Crystal Structure 3D Explorer -->
        <section id="structures" class="py-16 text-center">
            <h2 class="section-title">3D Crystal Structure Explorer</h2>
            <p class="section-subtitle">Most metals crystallize into one of three densely packed arrangements. Select a structure below to visualize its unit cell—the smallest repeating building block—and see its unique properties.</p>
            <div class="flex flex-wrap justify-center gap-4 mb-8">
                <button id="btn-bcc" class="btn btn-secondary active">Body-Centered Cubic (BCC)</button>
                <button id="btn-fcc" class="btn btn-secondary">Face-Centered Cubic (FCC)</button>
                <button id="btn-hcp" class="btn btn-secondary">Hexagonal Close-Packed (HCP)</button>
            </div>
            <div class="card max-w-7xl mx-auto p-6 lg:p-8">
                <div class="grid lg:grid-cols-2 gap-8 items-center">
                    <!-- Three.js renderer will be injected into this container -->
                    <div id="unitCellCanvasContainer" class="w-full aspect-[1/1] lg:aspect-auto"></div>
                    <div id="structure-info" class="text-left">
                        <!-- Content will be injected here by JavaScript -->
                    </div>
                </div>
            </div>
        </section>
        
        <!-- Stacking Sequences -->
        <section id="stacking" class="py-16 text-center">
            <h2 class="section-title">Understanding Close-Packed Stacking</h2>
            <p class="section-subtitle">FCC and HCP structures are both "close-packed," but they differ in how atomic planes are stacked. This fundamental difference determines many properties, including slip systems and ductility.</p>
            <div class="card max-w-5xl mx-auto p-8">
                <div class="flex justify-center gap-4 mb-6">
                    <button id="btn-stack-fcc" class="btn btn-secondary active">FCC (ABCABC...)</button>
                    <button id="btn-stack-hcp" class="btn btn-secondary">HCP (ABAB...)</button>
                </div>
                <div id="stacking-container" class="relative w-full overflow-hidden" style="height: 200px;">
                    <!-- Visualizer will be drawn here by JS -->
                </div>
            </div>
        </section>
        
        <!-- Comparing Structures by the Numbers (Chart.js) -->
        <section id="properties" class="py-16 text-center">
            <h2 class="section-title">Comparing Structures by the Numbers</h2>
            <p class="section-subtitle">How efficiently are atoms packed? How many neighbors does each atom have? These key metrics differentiate the crystal structures and influence material properties like ductility and density.</p>
            <div class="card max-w-5xl mx-auto p-6 lg:p-8">
                <div class="flex flex-wrap justify-center gap-4 mb-6">
                    <button id="btn-prop-apf" class="btn btn-secondary active">Packing Efficiency</button>
                    <button id="btn-prop-cn" class="btn btn-secondary">Coordination Number</button>
                    <button id="btn-prop-atoms" class="btn btn-secondary">Atoms per Cell</button>
                </div>
                <div class="chart-container">
                    <canvas id="propertiesChart"></canvas>
                </div>
            </div>
        </section>

        <!-- Interactive Calculators -->
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
        
        <!-- Miller Indices Notation -->
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
                        <label for="intercept-z" class="block text-sm font-medium text-slate-700">Z-intercept ('inf' for &infin;)</label>
                        <input type="text" id="intercept-z" value="inf" class="mt-1 block w-full p-2 border border-slate-300 rounded-md shadow-sm text-center">
                    </div>
                </div>
                <button id="miller-calculate" class="btn btn-primary">Find Miller Indices</button>
                <div id="miller-result" class="mt-6 text-left space-y-3">
                    <p class="text-slate-600 text-center">Result will be shown here.</p>
                </div>
            </div>
        </section>

        <!-- Macroscopic Properties -->
        <section id="macroscopic" class="py-16">
            <div class="text-center">
                <h2 class="section-title">From Single Crystals to Bulk Materials</h2>
                <p class="section-subtitle">How do individual crystals combine to form the materials we use every day? The distinction between single crystals and polycrystals, and the concepts of isotropy and anisotropy, explain how atomic order scales up.</p>
            </div>
            <div class="grid md:grid-cols-2 gap-8 max-w-6xl mx-auto">
                <div class="card p-8">
                    <h3 class="text-2xl font-bold mb-4 text-slate-800">Single vs. Polycrystalline</h3>
                    <p class="text-slate-600 mb-4">A material can be one continuous crystal or a composite of many small, randomly oriented crystal grains.</p>
                    <ul class="space-y-3">
                        <li><strong>Single Crystal:</strong> A solid where the crystal lattice is continuous and unbroken throughout the entire sample. Often exhibits flat faces (facets). Properties are typically anisotropic (direction-dependent).</li>
                        <li><strong>Polycrystalline:</strong> A solid composed of many small crystals (grains) with varying orientations. The interfaces where grains meet are called grain boundaries. If grains are randomly oriented, the bulk material is often isotropic (properties are the same in all directions).</li>
                    </ul>
                </div>
                <div class="card p-8">
                    <h3 class="text-2xl font-bold mb-4 text-slate-800">Isotropy vs. Anisotropy</h3>
                    <p class="text-slate-600 mb-4">Does a material's strength or conductivity change with direction? This property is dictated by the symmetry of its internal structure.</p>
                    <ul class="space-y-3">
                        <li><strong>Isotropic:</strong> Properties are identical in all directions. This is common in amorphous materials (like glass) and polycrystalline metals with random grain orientation.</li>
                        <li><strong>Anisotropic:</strong> Properties are direction-dependent. A single non-cubic crystal will be stronger along certain crystallographic planes. Wood is a classic example, being much stronger along the grain than across it.</li>
                    </ul>
                </div>
            </div>
        </div>
        </section>
    </main>

    <!-- Footer -->
    <footer class="bg-slate-900 text-slate-300 mt-16 rounded-t-3xl">
        <div class="container mx-auto px-4 sm:px-6 lg:px-8 py-8 text-center">
            <p>Interactive Guide to Crystalline Solids &mdash; A Materials Engineering Resource.</p>
        </div>
    </footer>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            // --- DATA MODELS ---
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

            // --- 3D VISUALIZATION (Three.js) ---
            const canvasContainer = document.getElementById('unitCellCanvasContainer');
            const scene = new THREE.Scene();
            const camera = new THREE.PerspectiveCamera(75, canvasContainer.clientWidth / canvasContainer.clientHeight, 0.1, 1000);
            const renderer = new THREE.WebGLRenderer({ antialias: true, alpha: true });
            renderer.setSize(canvasContainer.clientWidth, canvasContainer.clientHeight);
            canvasContainer.appendChild(renderer.domElement);

            const controls = new THREE.OrbitControls(camera, renderer.domElement);
            controls.enableDamping = true;
            controls.dampingFactor = 0.25;
            controls.screenSpacePanning = false;

            const light = new THREE.AmbientLight(0x404040, 2);
            scene.add(light);
            const directionalLight = new THREE.DirectionalLight(0xffffff, 1.5);
            directionalLight.position.set(5, 5, 5);
            scene.add(directionalLight);

            // Resizes the Three.js canvas when the window is resized
            function resizeThreeJsCanvas() {
                camera.aspect = canvasContainer.clientWidth / canvasContainer.clientHeight;
                camera.updateProjectionMatrix();
                renderer.setSize(canvasContainer.clientWidth, canvasContainer.clientHeight);
            }
            window.addEventListener('resize', resizeThreeJsCanvas);

            // Function to create a sphere for an atom
            function createAtom(color, radius = 0.5) {
                const geometry = new THREE.SphereGeometry(radius, 32, 32);
                const material = new THREE.MeshPhongMaterial({ color: color, shininess: 80 });
                return new THREE.Mesh(geometry, material);
            }

            // Function to create a bond/edge
            function createBond(start, end) {
                const points = [start, end];
                const geometry = new THREE.BufferGeometry().setFromPoints(points);
                const material = new THREE.LineBasicMaterial({ color: 0x94a3b8, linewidth: 2 });
                return new THREE.Line(geometry, material);
            }

            let currentModel = null;
            function loadStructure(type) {
                // Remove previous model and dispose of its resources to prevent memory leaks
                if (currentModel) {
                    currentModel.children.forEach(child => {
                        if (child.geometry) {
                            child.geometry.dispose();
                        }
                        if (child.material) {
                            if (Array.isArray(child.material)) {
                                child.material.forEach(mat => mat.dispose());
                            } else {
                                child.material.dispose();
                            }
                        }
                    });
                    scene.remove(currentModel);
                }

                const group = new THREE.Group();
                const radius = 0.5;
                const atomColor = 0x0d9488;
                const centralAtomColor = 0xf87171;

                if (type === 'bcc') {
                    // Create the cube wireframe
                    const geometry = new THREE.BoxGeometry(1.5, 1.5, 1.5);
                    const edges = new THREE.EdgesGeometry(geometry);
                    const line = new THREE.LineSegments(edges, new THREE.LineBasicMaterial({ color: 0x94a3b8 }));
                    group.add(line);

                    // Atoms for BCC
                    const cornerAtomPositions = [
                        new THREE.Vector3(-0.75, -0.75, -0.75), new THREE.Vector3(0.75, -0.75, -0.75),
                        new THREE.Vector3(-0.75, 0.75, -0.75), new THREE.Vector3(0.75, 0.75, -0.75),
                        new THREE.Vector3(-0.75, -0.75, 0.75), new THREE.Vector3(0.75, -0.75, 0.75),
                        new THREE.Vector3(-0.75, 0.75, 0.75), new THREE.Vector3(0.75, 0.75, 0.75)
                    ];
                    cornerAtomPositions.forEach(pos => {
                        const atom = createAtom(atomColor, radius * 0.5);
                        atom.position.copy(pos);
                        group.add(atom);
                    });

                    // Body-center atom
                    const centerAtom = createAtom(centralAtomColor, radius * 0.6);
                    group.add(centerAtom);

                } else if (type === 'fcc') {
                    // Create the cube wireframe
                    const geometry = new THREE.BoxGeometry(1.5, 1.5, 1.5);
                    const edges = new THREE.EdgesGeometry(geometry);
                    const line = new THREE.LineSegments(edges, new THREE.LineBasicMaterial({ color: 0x94a3b8 }));
                    group.add(line);

                    // Atoms for FCC
                    const cornerAtomPositions = [
                        new THREE.Vector3(-0.75, -0.75, -0.75), new THREE.Vector3(0.75, -0.75, -0.75),
                        new THREE.Vector3(-0.75, 0.75, -0.75), new THREE.Vector3(0.75, 0.75, -0.75),
                        new THREE.Vector3(-0.75, -0.75, 0.75), new THREE.Vector3(0.75, -0.75, 0.75),
                        new THREE.Vector3(-0.75, 0.75, 0.75), new THREE.Vector3(0.75, 0.75, 0.75)
                    ];
                    cornerAtomPositions.forEach(pos => {
                        const atom = createAtom(atomColor, radius * 0.5);
                        atom.position.copy(pos);
                        group.add(atom);
                    });

                    // Face-center atoms
                    const faceAtomPositions = [
                        new THREE.Vector3(0, 0, 0.75), new THREE.Vector3(0, 0, -0.75),
                        new THREE.Vector3(0, 0.75, 0), new THREE.Vector3(0, -0.75, 0),
                        new THREE.Vector3(0.75, 0, 0), new THREE.Vector3(-0.75, 0, 0)
                    ];
                    faceAtomPositions.forEach(pos => {
                        const atom = createAtom(centralAtomColor, radius * 0.6);
                        atom.position.copy(pos);
                        group.add(atom);
                    });
                } else if (type === 'hcp') {
                    // Create hexagonal prism wireframe
                    const h = 1.633; // c/a ratio for ideal HCP
                    const r = 0.5;
                    const angle = Math.PI / 3;
                    
                    const vertices = [];
                    for(let i = 0; i < 6; i++) {
                        // Bottom face
                        vertices.push(new THREE.Vector3(r * Math.cos(i * angle), r * Math.sin(i * angle), -h/2));
                        // Top face
                        vertices.push(new THREE.Vector3(r * Math.cos(i * angle), r * Math.sin(i * angle), h/2));
                    }
                    
                    const edges = new THREE.BufferGeometry().setFromPoints([
                        vertices[0], vertices[2], vertices[2], vertices[4], vertices[4], vertices[6], vertices[6], vertices[8], vertices[8], vertices[10], vertices[10], vertices[0], // Bottom face
                        vertices[1], vertices[3], vertices[3], vertices[5], vertices[5], vertices[7], vertices[7], vertices[9], vertices[9], vertices[11], vertices[11], vertices[1], // Top face
                        vertices[0], vertices[1], vertices[2], vertices[3], vertices[4], vertices[5], vertices[6], vertices[7], vertices[8], vertices[9], vertices[10], vertices[11] // Vertical edges
                    ]);
                    const line = new THREE.LineSegments(edges, new THREE.LineBasicMaterial({ color: 0x94a3b8 }));
                    group.add(line);

                    // Add atoms at vertices
                    vertices.forEach(pos => {
                        const atom = createAtom(atomColor, radius * 0.5);
                        atom.position.copy(pos);
                        group.add(atom);
                    });

                    // Add atoms at face centers
                    const centerTop = createAtom(centralAtomColor, radius * 0.6);
                    centerTop.position.set(0, 0, h/2);
                    group.add(centerTop);
                    const centerBottom = createAtom(centralAtomColor, radius * 0.6);
                    centerBottom.position.set(0, 0, -h/2);
                    group.add(centerBottom);

                    // Add three mid-plane atoms
                    const midPlaneAtoms = [
                        new THREE.Vector3(r * Math.cos(Math.PI/6), r * Math.sin(Math.PI/6), 0),
                        new THREE.Vector3(r * Math.cos(Math.PI/6 + 2*Math.PI/3), r * Math.sin(Math.PI/6 + 2*Math.PI/3), 0),
                        new THREE.Vector3(r * Math.cos(Math.PI/6 + 4*Math.PI/3), r * Math.sin(Math.PI/6 + 4*Math.PI/3), 0)
                    ];
                    midPlaneAtoms.forEach(pos => {
                        const atom = createAtom(centralAtomColor, radius * 0.6);
                        atom.position.copy(pos);
                        group.add(atom);
                    });
                }
                
                // Position camera based on structure
                camera.position.z = 3;
                camera.lookAt(group.position);
                
                currentModel = group;
                scene.add(currentModel);
            }

            // Animation loop
            function animate() {
                requestAnimationFrame(animate);
                controls.update();
                if (currentModel) {
                    currentModel.rotation.y += 0.005;
                }
                renderer.render(scene, camera);
            }
            animate();

            // --- UI LOGIC ---
            const structureInfo = document.getElementById('structure-info');
            const bccBtn = document.getElementById('btn-bcc');
            const fccBtn = document.getElementById('btn-fcc');
            const hcpBtn = document.getElementById('btn-hcp');

            // Function to update the descriptive information for a structure
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
            }

            // Event listeners for the 3D structure buttons
            bccBtn.addEventListener('click', () => {
                updateStructureInfo('bcc');
                loadStructure('bcc');
                document.querySelectorAll('#structures .btn-secondary').forEach(b => b.classList.remove('active'));
                bccBtn.classList.add('active');
            });
            fccBtn.addEventListener('click', () => {
                updateStructureInfo('fcc');
                loadStructure('fcc');
                document.querySelectorAll('#structures .btn-secondary').forEach(b => b.classList.remove('active'));
                fccBtn.classList.add('active');
            });
            hcpBtn.addEventListener('click', () => {
                updateStructureInfo('hcp');
                loadStructure('hcp');
                document.querySelectorAll('#structures .btn-secondary').forEach(b => b.classList.remove('active'));
                hcpBtn.classList.add('active');
            });
            
            // Initial load
            updateStructureInfo('bcc');
            loadStructure('bcc');

            // --- STACKING SEQUENCE VISUALIZER ---
            const stackingContainer = document.getElementById('stacking-container');
            const fccStackBtn = document.getElementById('btn-stack-fcc');
            const hcpStackBtn = document.getElementById('btn-stack-hcp');
            
            function createPlane(color, label) {
                const plane = document.createElement('div');
                plane.className = `absolute w-40 h-16 rounded-lg flex items-center justify-center font-bold text-white text-lg transition-transform duration-500 ease-in-out`;
                plane.style.backgroundColor = color;
                plane.textContent = label;
                return plane;
            }
            
            function visualizeStacking(type) {
                stackingContainer.innerHTML = '';
                const planes = [
                    { label: 'A', color: '#60a5fa' },
                    { label: 'B', color: '#34d399' },
                    { label: 'C', color: '#fbbf24' }
                ];
                
                if (type === 'fcc') {
                    // ABCABC... sequence
                    const positions = ['-top-2', 'top-10', 'top-24', 'top-36', 'top-50', 'top-64'];
                    stackingContainer.classList.add('h-[320px]');
                    
                    const p1 = createPlane(planes[0].color, planes[0].label); p1.style.transform = `translateY(0)`; p1.style.zIndex = 30;
                    const p2 = createPlane(planes[1].color, planes[1].label); p2.style.transform = `translateY(4rem)`; p2.style.zIndex = 20;
                    const p3 = createPlane(planes[2].color, planes[2].label); p3.style.transform = `translateY(8rem)`; p3.style.zIndex = 10;
                    const p4 = createPlane(planes[0].color, planes[0].label); p4.style.transform = `translateY(12rem)`; p4.style.zIndex = 0;
                    
                    stackingContainer.append(p1, p2, p3, p4);

                } else if (type === 'hcp') {
                    // ABAB... sequence
                    const positions = ['-top-2', 'top-10', 'top-24', 'top-36', 'top-50', 'top-64'];
                    stackingContainer.classList.add('h-[320px]');
                    
                    const p1 = createPlane(planes[0].color, planes[0].label); p1.style.transform = `translateY(0)`; p1.style.zIndex = 30;
                    const p2 = createPlane(planes[1].color, planes[1].label); p2.style.transform = `translateY(4rem)`; p2.style.zIndex = 20;
                    const p3 = createPlane(planes[0].color, planes[0].label); p3.style.transform = `translateY(8rem)`; p3.style.zIndex = 10;
                    const p4 = createPlane(planes[1].color, planes[1].label); p4.style.transform = `translateY(12rem)`; p4.style.zIndex = 0;

                    stackingContainer.append(p1, p2, p3, p4);
                }
            }
            
            fccStackBtn.addEventListener('click', () => {
                visualizeStacking('fcc');
                fccStackBtn.classList.add('active');
                hcpStackBtn.classList.remove('active');
            });
            hcpStackBtn.addEventListener('click', () => {
                visualizeStacking('hcp');
                hcpStackBtn.classList.add('active');
                fccStackBtn.classList.remove('active');
            });
            
            visualizeStacking('fcc');


            // --- CHART.JS LOGIC ---
            const propertiesChartCtx = document.getElementById('propertiesChart').getContext('2d');
            let propertiesChart;
            const chartData = {
                labels: ['BCC', 'FCC', 'HCP'],
                apf: { label: 'Atomic Packing Factor (%)', data: [68, 74, 74] },
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
                                legend: { display: true, position: 'top' }
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


            // --- CALCULATOR LOGIC ---
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
                const r_pm = metal.radius;
                const NA = 6.022e23; // Avogadro's number
                
                let a_pm;
                if (metal.structure === 'fcc') {
                    a_pm = 2 * r_pm * Math.sqrt(2);
                } else { // bcc
                    a_pm = 4 * r_pm / Math.sqrt(3);
                }
                const a_cm = a_pm * 1e-10; // Convert pm to cm
                const Vc = Math.pow(a_cm, 3);
                const density = (n * A) / (Vc * NA);
                
                tdResultDiv.innerHTML = `
                    <p class="font-bold text-center text-lg mb-2">${metal.name} (${metal.structure.toUpperCase()})</p>
                    <p><strong>n</strong> (atoms/cell): ${n}</p>
                    <p><strong>A</strong> (g/mol): ${A}</p>
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
                    if (str === 'inf' || str === 'infinity' || str === '∞') return Infinity;
                    if (str.includes('/')) {
                        const parts = str.split('/');
                        const num = parseFloat(parts[0]);
                        const den = parseFloat(parts[1]);
                        return isNaN(num) || isNaN(den) || den === 0 ? NaN : num / den;
                    }
                    return parseFloat(str);
                }
                
                const intercepts = [parseIntercept(xStr), parseIntercept(yStr), parseIntercept(zStr)];
                
                if (intercepts.some(isNaN)) {
                    millerResultDiv.innerHTML = `<p class="text-red-600 text-center">Invalid intercept value. Use numbers, fractions (e.g., 1/2), or 'inf'.</p>`;
                    return;
                }
                
                const reciprocals = intercepts.map(i => i === 0 ? Infinity : 1 / i);
                
                let commonMultiple = 1;
                for (let r of reciprocals) {
                    if (r !== 0 && r !== Infinity && !Number.isInteger(r)) {
                        const denominator = 1 / (r - Math.floor(r));
                        if (denominator !== Infinity) {
                            commonMultiple = commonMultiple * denominator;
                        }
                    }
                }
                
                const integers = reciprocals.map(r => r === Infinity ? 0 : Math.round(r * commonMultiple));
                
                const h = integers[0];
                const k = integers[1];
                const l = integers[2];
                
                const formatIndex = (n) => n < 0 ? `(${Math.abs(n)})` : n;
                const formattedH = h < 0 ? `(${Math.abs(h)})` : h;
                const formattedK = k < 0 ? `(${Math.abs(k)})` : k;
                const formattedL = l < 0 ? `(${Math.abs(l)})` : l;

                millerResultDiv.innerHTML = `
                    <div class="space-y-2 text-left">
                        <p><strong>1. Intercepts:</strong> [${intercepts.map(i => i === Infinity ? '∞' : i).join(', ')}]</p>
                        <p><strong>2. Reciprocals:</strong> [${reciprocals.map(r => r === Infinity ? '∞' : r.toFixed(2)).join(', ')}]</p>
                        <p><strong>3. Clear Fractions & Convert to Integers:</strong> [${integers.join(', ')}]</p>
                        <p class="mt-4 text-center text-2xl font-bold text-teal-700">Miller Indices (hkl) = (${formattedH} ${formattedK} ${formattedL})</p>
                    </div>
                `;
            });


            // --- NAVIGATION LOGIC ---
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
            
            // Trigger initial calculations on load
            arCalculateBtn.click();
            tdCalculateBtn.click();
            millerCalculateBtn.click();
        });
    </script>
</body>
</html>
