<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Phase Diagrams Cheat Sheet | TestUrSelf</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            margin: 20px;
            background-color: #f5f5f5;
            position: relative;
            line-height: 1.6;
        }
        h1 {
            text-align: center;
            color: #2c3e50;
            margin-bottom: 30px;
            font-size: 2.5em;
            text-shadow: 1px 1px 2px rgba(0,0,0,0.1);
        }
        h2 {
            color: #3498db;
            border-bottom: 2px solid #3498db;
            padding-bottom: 5px;
            margin-top: 30px;
        }
        table {
            width: 100%;
            border-collapse: collapse;
            margin: 20px 0;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            background-color: white;
            border-radius: 8px;
            overflow: hidden;
        }
        th, td {
            padding: 12px 15px;
            text-align: left;
            border-bottom: 1px solid #ddd;
        }
        th {
            background-color: #4CAF50;
            color: white;
            font-weight: bold;
        }
        tr:hover {
            background-color: #f1f1f1;
        }
        .category-iso {
            color: #FF5733;
            font-weight: bold;
        }
        .category-vol {
            color: #33A1FF;
            font-weight: bold;
        }
        .category-eutectic {
            color: #9C33FF;
            font-weight: bold;
        }
        .category-fec {
            color: #FFC300;
            font-weight: bold;
        }
        .category-thermo {
            color: #50C878;
            font-weight: bold;
        }
        .watermark {
            position: fixed;
            bottom: 10px;
            right: 10px;
            opacity: 0.1;
            font-size: 80px;
            font-weight: bold;
            color: #333;
            pointer-events: none;
            transform: rotate(-15deg);
            z-index: 1000;
            font-family: 'Arial Black', sans-serif;
        }
        .equation {
            font-family: "Courier New", monospace;
            background-color: #f8f9fa;
            padding: 2px 5px;
            border-radius: 4px;
        }
    </style>
</head>
<body>
    <div class="watermark">TestUrSelf</div>
    <h1>Phase Diagrams Cheat Sheet</h1>

    <h2>Binary Isomorphous System</h2>
    <table>
        <thead>
            <tr>
                <th>Equation</th>
                <th>Application</th>
                <th>Category</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td class="category-iso">$W_L = \frac{C_a - C_0}{C_a - C_L}$</td>
                <td>Mass fraction of liquid phase in a binary isomorphous system</td>
                <td>Binary Isomorphous</td>
            </tr>
            <tr>
                <td class="category-iso">$W_a = \frac{C_0 - C_L}{C_a - C_L}$</td>
                <td>Mass fraction of $\alpha$ solid-solution phase in a binary isomorphous system</td>
                <td>Binary Isomorphous</td>
            </tr>
        </tbody>
    </table>

    <h2>Volume Fractions</h2>
    <table>
        <thead>
            <tr>
                <th>Equation</th>
                <th>Application</th>
                <th>Category</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td class="category-vol">$V_a = \frac{V_a}{V_a + V_\beta}$</td>
                <td>Volume fraction of $\alpha$ phase</td>
                <td>Volume Fractions</td>
            </tr>
            <tr>
                <td class="category-vol">$V_a = \frac{\rho_a}{\rho_a + \rho_\beta}$</td>
                <td>Conversion of mass fraction to volume fraction for $\alpha$ phase</td>
                <td>Volume Fractions</td>
            </tr>
            <tr>
                <td class="category-vol">$W_a = \frac{V_a \rho_a}{V_a \rho_a + V_\beta \rho_\beta}$</td>
                <td>Conversion of volume fraction to mass fraction for $\alpha$ phase</td>
                <td>Volume Fractions</td>
            </tr>
        </tbody>
    </table>

    <h2>Binary Eutectic System</h2>
    <table>
        <thead>
            <tr>
                <th>Equation</th>
                <th>Application</th>
                <th>Category</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td class="category-eutectic">$W_e = \frac{P}{P + Q}$</td>
                <td>Mass fraction of eutectic microconstituent</td>
                <td>Eutectic System</td>
            </tr>
            <tr>
                <td class="category-eutectic">$W_{a'} = \frac{Q}{P + Q}$</td>
                <td>Mass fraction of primary $\alpha$ microconstituent</td>
                <td>Eutectic System</td>
            </tr>
            <tr>
                <td class="category-eutectic">$W_a = \frac{Q + R}{P + Q + R}$</td>
                <td>Mass fraction of total $\alpha$ phase</td>
                <td>Eutectic System</td>
            </tr>
            <tr>
                <td class="category-eutectic">$W_\beta = \frac{P}{P + Q + R}$</td>
                <td>Mass fraction of $\beta$ phase</td>
                <td>Eutectic System</td>
            </tr>
        </tbody>
    </table>

    <h2>Fe–C Alloy System</h2>
    <table>
        <thead>
            <tr>
                <th>Equation</th>
                <th>Application</th>
                <th>Category</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td class="category-fec">$W_\rho = \frac{C_0' + 0.022}{0.74}$</td>
                <td>Mass fraction of pearlite in a hypoeutectoid Fe–C alloy</td>
                <td>Fe–C System</td>
            </tr>
            <tr>
                <td class="category-fec">$W_{a'} = \frac{0.76 - C_0'}{0.74}$</td>
                <td>Mass fraction of proeutectoid $\alpha$ ferrite in a hypoeutectoid Fe–C alloy</td>
                <td>Fe–C System</td>
            </tr>
            <tr>
                <td class="category-fec">$W_\rho = \frac{6.70 - C_1'}{5.94}$</td>
                <td>Mass fraction of pearlite in a hypereutectoid Fe–C alloy</td>
                <td>Fe–C System</td>
            </tr>
            <tr>
                <td class="category-fec">$W_{\text{Fe}_3\text{C}' = \frac{C_1' - 0.76}{5.94}$</td>
                <td>Mass fraction of proeutectoid $\text{Fe}_3\text{C}$ in a hypereutectoid Fe–C alloy</td>
                <td>Fe–C System</td>
            </tr>
        </tbody>
    </table>

    <h2>Thermodynamics</h2>
    <table>
        <thead>
            <tr>
                <th>Equation</th>
                <th>Application</th>
                <th>Category</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td class="category-thermo">$P + F = C + N$</td>
                <td>Gibbs phase rule (general form)</td>
                <td>Thermodynamics</td>
            </tr>
        </tbody>
    </table>

    <!-- MathJax Configuration for $...$ delimiters -->
    <script>
        MathJax = {
          tex: {
            inlineMath: [['$', '$'], ['\\(', '\\)']]
          }
        };
    </script>
    <script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
    <script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>
</body>
</html>
