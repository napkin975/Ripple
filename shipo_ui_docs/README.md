# Shipo UI - AI Causal Data Analyst

An end-to-end Next.js AI chat agent UI for causal data analysis, featuring interactive graph analytics and SHAP value visualizations.

## Live Demo
https://shipoui.vercel.app

## GitHub Repository
https://github.com/mahdi1234-hub/shipo_ui

## Features

### Chat Interface
- Aura-inspired design theme (Plus Jakarta Sans, Geist, Inter fonts)
- Real-time AI responses powered by Cerebras LLM (llama3.1-8b)
- Inline rendering of all analytics within the chat conversation
- Support for CSV, JSON, and structured text data input

### Graph Analytics - Sigma.js + Graphology
- Interactive causal network graphs with zoom, pan, hover
- **Individual node drag-and-drop** (drag single nodes to rearrange)
- ForceAtlas2, Circular, and Random layout algorithms
- Community detection via label propagation
- Node sizing by 6 metrics (centrality, betweenness, PageRank, closeness, degree, weighted degree)
- Node coloring by community, centrality heat, betweenness heat, PageRank heat
- Edge filtering by type (causal, correlation, association)
- Community filtering with visual badges
- **Shortest path finder** (click nodes or use dropdowns)
- Path highlighting on graph
- Node search with auto-focus
- Full node detail panel with all centrality metrics
- Neighborhood community breakdown
- Graph metrics panel (density, clustering, diameter, avg path length, components)
- Top-5 node rankings by each centrality metric
- Degree distribution histogram
- Toggle labels and edge labels

### Graph Analytics - Cosmograph (GPU-Accelerated)
- WebGL GPU-accelerated graph rendering via Cosmograph React
- CosmographProvider with connected components
- CosmographSearch for node search
- CosmographHistogram for centrality distribution
- CosmographSizeLegend
- CosmographButtonFitView and CosmographButtonZoomInOut controls
- Node analytics panel with all metrics
- Interactive node selection with connection browsing

### Centrality Algorithms
- Degree centrality (weighted)
- Betweenness centrality (Brandes algorithm)
- PageRank (iterative with damping factor)
- Closeness centrality (BFS-based)
- All-pairs shortest paths

### SHAP Value Analysis
- Global feature importance bar charts
- Waterfall charts showing feature contributions
- Beeswarm plots for SHAP value distribution
- Dependence plots with interaction coloring
- Feature interaction matrix heatmap

### Statistical Analysis
- Automatic data type detection (numeric vs categorical)
- Descriptive statistics (mean, median, std, min, max)
- Pearson correlation matrix heatmap
- Causal direction inference via lag correlation

## Tech Stack
- Next.js 16 (App Router, Turbopack)
- TypeScript
- Tailwind CSS
- Sigma.js + Graphology (graph visualization)
- Cosmograph React (GPU graph visualization)
- Recharts (SHAP plots and charts)
- Cerebras AI API (LLM)
- Vercel (deployment)
