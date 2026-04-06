# Shipo UI - AI Causal Data Analyst

An end-to-end Next.js AI chat agent UI for causal data analysis, featuring interactive graph analytics and SHAP value visualizations.

## Live Demo
https://shipoui.vercel.app

## GitHub Repository
https://github.com/mahdi1234-hub/shipo_ui

## Features

### Chat Interface
- Aura-inspired design theme (Plus Jakarta Sans, Geist, Inter fonts)
- Real-time AI responses powered by Cerebras LLM (llama-4-scout-17b-16e-instruct)
- Inline rendering of all analytics within the chat conversation
- Support for CSV, JSON, and structured text data input

### Graph Analytics (Sigma.js + Graphology)
- Interactive causal network graphs with zoom, pan, hover
- ForceAtlas2 layout algorithm
- Community detection via label propagation
- Degree centrality computation
- Node/edge highlighting on hover
- Graph metrics (density, clustering coefficient, components)
- Edge type classification (causal, correlation, association)

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
- Next.js 16 (App Router)
- TypeScript
- Tailwind CSS
- Sigma.js + Graphology (graph visualization)
- Recharts (SHAP plots and charts)
- Cerebras AI API (LLM)
- Vercel (deployment)
