# DAG Visualizer

An interactive web application built with **FastAPI** and **Cytoscape.js** to visualize Directed Acyclic Graphs (DAGs). This tool is designed for developers and students to quickly map out dependencies, task schedules, or algorithm logic (like LeetCode problems).

## 🚀 Features

- **DAG Rendering:** Input your edge list as a JSON array and see the graph update instantly.
- **Grid Visualization:** Visualize 2D matrices with a dynamic color gradient based on cell values.
- **Smart Layout:** Uses the Dagre engine to automatically arrange DAG nodes for maximum readability.
- **Modern UI:** A clean, responsive design with a sidebar for configuration and a large viewport for the graph.
- **SEO Optimized:** Built with accessibility and searchability in mind.

## 🛠️ Core Libraries

The visualization is powered by three key frontend libraries:
1.  **[Cytoscape.js](https://js.cytoscape.org/):** A highly optimized graph theory library for visualization and analysis.
2.  **[Dagre](https://github.com/dagrejs/dagre):** A JavaScript library that lays out directed graphs on the client side.
3.  **[Cytoscape-Dagre](https://github.com/cytoscape/cytoscape.js-dagre):** An extension that integrates the Dagre layout engine into Cytoscape.js.

The backend is built with **FastAPI** to serve the application and manage templates.

## ⚙️ Installation & Setup

### 1. Clone the Repository
```bash
git clone <your-repo-url>
cd dagviz
```

### 2. Create and Activate a Virtual Environment
```bash
python -m venv .venv
source .venv/bin/activate  # On Windows use: .venv\Scripts\activate
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

### 4. Run the Application
```bash
python main.py
```

### 5. Access the Visualizer
Open your browser and navigate to:
**[http://localhost:8000](http://localhost:8000)**

## 📊 Usage

### DAG Visualizer
Enter your edges in the sidebar using the following JSON format:
```json
[
  ["SourceNode", "TargetNode", "OptionalWeight"],
  ["A", "B", 10],
  ["B", "C", 5]
]
```
Click **"Render DAG"** to generate the visualization.

### Grid Visualizer
Switch to the **Grid Visualizer** tab and enter a 2D matrix:
```json
[
  [1, 2, 3],
  [4, 5, 6],
  [7, 8, 9]
]
```
Click **"Render Grid"** to see a heat-map style visualization where colors are automatically calculated based on the range of values in your input.
