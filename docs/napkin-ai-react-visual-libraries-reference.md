# Napkin.ai Platform Analysis & Advanced React Visual Libraries Reference

> A comprehensive reference document covering napkin.ai's platform features, pricing,
> and the professional-grade React libraries used to build napkin.ai-style visual
> experiences -- mindmaps, infographics, charts, brainstorming boards, and more.

---

## Table of Contents

1. [Napkin.ai Platform Overview](#1-napkinai-platform-overview)
2. [Napkin.ai Landing Page Features](#2-napkinai-landing-page-features)
3. [Napkin.ai Pricing & Plans](#3-napkinai-pricing--plans)
4. [Core React Libraries Used in Napkin.ai](#4-core-react-libraries-used-in-napkinai)
5. [Advanced React Libraries for Visual Content](#5-advanced-react-libraries-for-visual-content)
6. [Mindmaps & Brainstorming Libraries](#6-mindmaps--brainstorming-libraries)
7. [Chart & Data Visualization Libraries](#7-chart--data-visualization-libraries)
8. [Infographic & Diagram Libraries](#8-infographic--diagram-libraries)
9. [Canvas & Rendering Engines](#9-canvas--rendering-engines)
10. [Recommended Stack for Napkin.ai-Style Features](#10-recommended-stack-for-napkinai-style-features)
11. [Relevance to Ripple](#11-relevance-to-ripple)

---

## 1. Napkin.ai Platform Overview

**Napkin.ai** is an AI-powered visual content generation platform that transforms text
into professional-quality visuals -- infographics, diagrams, flowcharts, mindmaps,
charts, and presentation-ready graphics. It targets consultants, founders, marketers,
and educators who need to turn ideas into polished visual assets rapidly.

### Key Capabilities

| Capability | Description |
|---|---|
| **Text-to-Visual AI** | Converts plain text/bullet points into styled infographics, diagrams, and charts |
| **Template Library** | Hundreds of professional visual templates (pyramids, timelines, Venn diagrams, process flows) |
| **Smart Layout Engine** | Auto-arranges elements using constraint-based layout algorithms |
| **Style System** | Consistent color palettes, typography, and icon sets across all generated visuals |
| **Export** | SVG, PNG, PDF export at presentation-quality resolution |
| **Real-time Collaboration** | Multi-user editing with live cursors and conflict resolution |
| **Brand Kit** | Custom color palettes, fonts, and logos applied to all outputs |
| **Drag-and-Drop Editor** | WYSIWYG canvas for fine-tuning AI-generated visuals |

### Who It Serves (from landing page)

- **Consultants** -- Elevate every deck
- **Founders** -- Pitch ideas instantly
- **Marketers** -- Create content faster
- **Educators** -- Make lessons visual

---

## 2. Napkin.ai Landing Page Features

### Visual Types Showcased

Based on the platform's landing page and product screenshots:

1. **Mountain/Pyramid Diagrams** -- Layered pyramids showing hierarchical concepts
   (e.g., "The Path to Your Best Self" with Impact, Courage, Creation, Learning layers)
2. **Signpost/Direction Diagrams** -- Visual signposts showing different user personas
   and use cases
3. **Concept Cards** -- Styled cards with icons for abstract concepts
   (e.g., "Understanding Human Motivation" with Mastery, Freedom, Impact, Legacy)
4. **Layered Pyramids** -- Stacked sections with labels
   (e.g., "Enhance Your Presentation's Impact" with Grab Attention, Establish Relevance,
   Preview of Content)
5. **Flowcharts & Process Diagrams**
6. **Comparison Tables**
7. **Timeline Visualizations**
8. **Venn Diagrams**
9. **Org Charts & Tree Structures**
10. **Data-driven Charts** (bar, pie, line, area)

### Landing Page Technical Patterns

- **Next.js** as the framework (SSR + static generation for marketing pages)
- **React 18+** with Server Components
- **Framer Motion** for scroll-triggered animations and micro-interactions
- **SVG-based rendering** for all visual outputs (resolution-independent)
- **Canvas fallback** for complex compositing
- **WebSocket connections** for real-time collaboration features

---

## 3. Napkin.ai Pricing & Plans

### Free Plan

- Basic text-to-visual generation
- Limited template access
- Standard export formats (PNG)
- Watermarked outputs
- Community support

### Professional Plan (~$12-15/month billed annually)

- **Unlimited** visual generations
- **Full template library** access
- **High-resolution exports** (SVG, PNG, PDF)
- **No watermarks**
- **Brand Kit** (custom colors, fonts, logos)
- **Priority AI generation**
- **Advanced chart types** (Sankey, treemap, radar)
- **Custom icon library**

### Enterprise / Team Plan (custom pricing)

- Everything in Professional
- **Team collaboration** with shared workspaces
- **SSO / SAML** authentication
- **Admin dashboard** and usage analytics
- **API access** for programmatic visual generation
- **Custom templates** and branded outputs
- **Dedicated support** and onboarding
- **Advanced permissions** and role management

### Key Pricing Features Matrix

| Feature | Free | Pro | Enterprise |
|---|:---:|:---:|:---:|
| Text-to-Visual AI | Limited | Unlimited | Unlimited |
| Templates | Basic | Full Library | Full + Custom |
| Export Formats | PNG | SVG, PNG, PDF | All + API |
| Brand Kit | -- | Yes | Yes |
| Collaboration | -- | -- | Yes |
| API Access | -- | -- | Yes |
| Custom Icons | -- | Yes | Yes |
| Watermark-free | -- | Yes | Yes |

---

## 4. Core React Libraries Used in Napkin.ai

Based on analysis of napkin.ai's frontend bundle, technology fingerprints, and
comparable SaaS visual editors, the platform leverages these core React libraries:

### 4.1 Framework & Rendering

| Library | Version | Purpose |
|---|---|---|
| **React** | 18.x | Core UI framework |
| **Next.js** | 14.x | SSR, routing, API routes |
| **TypeScript** | 5.x | Type safety across the codebase |

### 4.2 State Management

| Library | Purpose |
|---|---|
| **Zustand** | Lightweight state for canvas/editor state |
| **Jotai** or **Recoil** | Atomic state for individual visual element properties |
| **React Query (TanStack Query)** | Server state, caching AI generation results |

### 4.3 Styling & Animation

| Library | Purpose |
|---|---|
| **Tailwind CSS** | Utility-first styling for the UI shell |
| **Framer Motion** | Page transitions, element animations, drag interactions |
| **CSS Modules** or **styled-components** | Scoped component styles |

### 4.4 Canvas & Visual Rendering (Core to Napkin.ai)

| Library | Purpose |
|---|---|
| **React Flow** (`@xyflow/react`) | Node-based diagrams, flowcharts, mindmaps |
| **Fabric.js** (via React wrapper) | Canvas-based visual editor with object manipulation |
| **Konva.js** + **react-konva** | High-performance 2D canvas rendering |
| **D3.js** + React bindings | Data-driven chart generation and custom visualizations |
| **SVG.js** or raw React SVG | SVG manipulation for vector graphics |

### 4.5 AI Integration

| Library | Purpose |
|---|---|
| **OpenAI SDK** / **Anthropic SDK** | LLM calls for text-to-visual layout generation |
| **Vercel AI SDK** (`ai`) | Streaming AI responses for real-time generation UX |
| **LangChain.js** | Prompt chaining for multi-step visual generation |

---

## 5. Advanced React Libraries for Visual Content

### 5.1 React Flow (@xyflow/react) -- PRIMARY

**The most critical library for napkin.ai-style node-based visuals.**

```
npm install @xyflow/react
```

**What it renders:**
- Flowcharts, process diagrams
- Mindmaps and concept maps
- Org charts and tree structures
- Node-based editors (like napkin.ai's drag-and-drop canvas)
- Custom node types with rich content

**Why it's essential:**
- Handles pan, zoom, drag natively
- Custom node/edge rendering with React components
- Built-in layout algorithms (dagre, elkjs integration)
- Minimap, controls, background grid
- Touch support for mobile
- Used by Stripe, Typeform, and similar SaaS products

**Key features for napkin.ai-style visuals:**
- Custom node components (render cards, icons, text blocks inside nodes)
- Edge labels and custom edge paths
- Sub-flows and grouping
- Automatic layout with dagre/ELK

### 5.2 Konva.js + react-konva -- CANVAS ENGINE

```
npm install react-konva konva
```

**What it renders:**
- Free-form canvas with shapes, images, text
- Infographic layouts with pixel-perfect positioning
- Drag-and-drop visual editors
- Image compositing and layering

**Why it's essential:**
- Hardware-accelerated 2D canvas
- Built-in transformers (resize, rotate handles)
- Event system on canvas objects
- Export to image/data URL
- High performance with thousands of elements

### 5.3 Fabric.js -- VISUAL EDITOR

```
npm install fabric
```

**What it renders:**
- Rich canvas editor (similar to Canva/Figma-lite)
- Text with fonts, colors, effects
- Shapes with fills, strokes, gradients
- Image manipulation and filters
- SVG import/export

### 5.4 D3.js + React -- DATA VISUALIZATION

```
npm install d3 @types/d3
```

**What it renders:**
- Bar, line, area, pie charts
- Treemaps, sunbursts, chord diagrams
- Force-directed graphs
- Geographic maps
- Sankey diagrams
- Any custom data visualization

---

## 6. Mindmaps & Brainstorming Libraries

### 6.1 React Flow with Dagre/ELK Layout

**Best for:** Professional mindmaps with auto-layout

```
npm install @xyflow/react dagre @dagrejs/dagre
```

Features:
- Automatic tree/radial layout
- Collapsible branches
- Custom styled nodes
- Real-time collaborative editing support
- Keyboard navigation

### 6.2 react-mindmap

```
npm install react-mindmap
```

Features:
- Purpose-built mindmap component
- Hierarchical node expansion
- Customizable node rendering
- SVG-based output

### 6.3 Markmap

```
npm install markmap-lib markmap-view markmap-toolbar
```

Features:
- Converts Markdown to interactive mindmaps
- Collapsible nodes
- Pan and zoom
- Export to SVG/HTML
- Ideal for text-first workflows (like napkin.ai's text-to-visual)

### 6.4 react-organizational-chart

```
npm install react-organizational-chart
```

Features:
- Tree structure visualization
- Custom node components
- Horizontal/vertical layouts
- Connector line customization

### 6.5 @antv/G6 -- GRAPH VISUALIZATION ENGINE

```
npm install @antv/g6
```

**Advanced features for brainstorming:**
- Multiple layout algorithms (force, dagre, radial, concentric, grid)
- Built-in mindmap layout mode
- Combo (grouping) support
- Animation and transitions
- Mini-map, tooltip, context menu plugins
- Tree graph mode
- Used by Ant Group (Alibaba) for enterprise dashboards

### 6.6 GoJS (Commercial)

```
npm install gojs
```

**Enterprise-grade features:**
- Palette-based drag-and-drop
- Automatic layout (tree, force, layered, circular)
- Link routing (orthogonal, Bezier)
- Overview panel
- Built-in undo/redo
- Used in enterprise diagramming tools

---

## 7. Chart & Data Visualization Libraries

### 7.1 Recharts -- MOST POPULAR

```
npm install recharts
```

| Feature | Support |
|---|---|
| Bar / Line / Area | Yes |
| Pie / Radar / Scatter | Yes |
| Treemap / Funnel | Yes |
| Responsive | Yes |
| Animation | Yes |
| Customizable tooltips | Yes |

### 7.2 Nivo (@nivo/core) -- DESIGN-FOCUSED

```
npm install @nivo/core @nivo/bar @nivo/line @nivo/pie @nivo/sankey @nivo/treemap
```

**Why Nivo for napkin.ai-style charts:**
- Beautiful default themes and color palettes
- Rich interactivity (hover, click, tooltips)
- SVG + Canvas + HTML rendering modes
- Responsive by default
- Server-side rendering support
- Pattern fills and gradients
- 30+ chart types including:
  - Sankey diagrams
  - Chord diagrams
  - Waffle charts
  - Bump charts
  - Swarm plots
  - Radar charts
  - Calendar heatmaps
  - Marimekko charts

### 7.3 Visx (@visx) -- LOW-LEVEL D3 + REACT

```
npm install @visx/group @visx/shape @visx/scale @visx/axis @visx/tooltip
```

**Why Visx:**
- Built by Airbnb
- D3 primitives as React components
- Maximum customization
- Tree-shakeable (small bundle)
- Used for custom napkin.ai-style chart templates

### 7.4 Apache ECharts (echarts-for-react)

```
npm install echarts echarts-for-react
```

**Enterprise-grade charting:**
- 20+ chart types
- Massive dataset support (millions of points)
- 3D charts, globe visualization
- Rich animations
- Themes and dark mode
- Used by Fortune 500 companies

### 7.5 Tremor -- DASHBOARD COMPONENTS

```
npm install @tremor/react
```

**Why Tremor:**
- Pre-built dashboard components
- Tailwind CSS integration
- Cards, KPI metrics, sparklines
- Perfect for data-heavy infographics

### 7.6 Victory (victory-native for mobile)

```
npm install victory
```

**Cross-platform charting for React and React Native.**

---

## 8. Infographic & Diagram Libraries

### 8.1 Mermaid.js + React

```
npm install mermaid react-mermaid
```

**Diagram types:**
- Flowcharts
- Sequence diagrams
- Gantt charts
- Class diagrams
- State diagrams
- Entity-relationship diagrams
- User journey maps
- Git graphs
- Pie charts

**Napkin.ai relevance:** Text-to-diagram (Markdown syntax to visual).

### 8.2 Excalidraw (@excalidraw/excalidraw)

```
npm install @excalidraw/excalidraw
```

**What makes it special:**
- Hand-drawn aesthetic (whiteboard style)
- Real-time collaboration built-in
- Library of shapes and icons
- Export to PNG, SVG, clipboard
- Infinite canvas
- Used by Meta, Google, Microsoft
- Open source (MIT license)

**Perfect for:** Brainstorming boards, quick sketches, informal diagrams.

### 8.3 TLDraw (@tldraw/tldraw)

```
npm install @tldraw/tldraw
```

**Features:**
- Full-featured whiteboard/canvas
- Drawing tools (pen, shapes, text, arrows)
- Infinite canvas with zoom
- Multi-user collaboration
- Custom shape system
- Built-in dark mode
- Export functionality

**Perfect for:** Building a custom visual editor on top of a mature canvas system.

### 8.4 JointJS / Rappid

```
npm install jointjs
```

**Enterprise diagramming:**
- BPMN, UML, ERD support
- Hierarchical layouts
- Link routing algorithms
- Built-in validation
- Stencil (shape palette)
- Paper (viewport) management

### 8.5 React Diagrams (@projectstorm/react-diagrams)

```
npm install @projectstorm/react-diagrams
```

**Features:**
- Node-based diagram engine
- Custom ports and links
- Drag-and-drop from palette
- Serialization/deserialization
- Extendable model system

---

## 9. Canvas & Rendering Engines

### 9.1 PixiJS + React (@pixi/react)

```
npm install @pixi/react pixi.js
```

**When to use:**
- WebGL-accelerated 2D rendering
- Thousands of animated elements
- Particle effects, filters, masks
- High-performance infographic animations

### 9.2 Three.js + React Three Fiber (@react-three/fiber)

```
npm install @react-three/fiber @react-three/drei three
```

**When to use:**
- 3D data visualizations
- 3D mindmaps and concept spaces
- Immersive infographic experiences
- Globe/geographic visualizations

### 9.3 Paper.js

```
npm install paper
```

**Vector graphics engine for:**
- Complex path operations (boolean operations, path simplification)
- Smooth curve fitting
- Raster effects on vector content
- SVG manipulation

### 9.4 Rough.js

```
npm install roughjs
```

**Hand-drawn style rendering:**
- Sketch-like lines and fills
- Used by Excalidraw internally
- SVG and Canvas output
- Perfect for informal/friendly visual aesthetics

---

## 10. Recommended Stack for Napkin.ai-Style Features

### Tier 1: Essential (Must-Have)

| Library | Role | Install |
|---|---|---|
| **React 18+** | Core framework | `react react-dom` |
| **Next.js 14+** | Framework | `next` |
| **React Flow** | Diagrams, flowcharts, mindmaps | `@xyflow/react` |
| **Konva + react-konva** | Canvas editor | `react-konva konva` |
| **D3.js** | Custom visualizations | `d3` |
| **Framer Motion** | Animations | `framer-motion` |
| **Zustand** | State management | `zustand` |

### Tier 2: Advanced Visuals

| Library | Role | Install |
|---|---|---|
| **Nivo** | Beautiful charts | `@nivo/core @nivo/bar @nivo/line @nivo/pie` |
| **Excalidraw** | Whiteboard/brainstorming | `@excalidraw/excalidraw` |
| **Markmap** | Text-to-mindmap | `markmap-lib markmap-view` |
| **Mermaid** | Text-to-diagram | `mermaid` |
| **@antv/G6** | Graph visualization | `@antv/g6` |

### Tier 3: Polish & Production

| Library | Role | Install |
|---|---|---|
| **TLDraw** | Full canvas editor | `@tldraw/tldraw` |
| **Recharts** | Simple charts | `recharts` |
| **Visx** | Custom D3+React charts | `@visx/*` |
| **Rough.js** | Hand-drawn style | `roughjs` |
| **html-to-image** | Export to PNG/SVG | `html-to-image` |

### Complete Install Command

```bash
npm install react react-dom next typescript \
  @xyflow/react dagre \
  react-konva konva \
  d3 @types/d3 \
  framer-motion \
  zustand \
  @nivo/core @nivo/bar @nivo/line @nivo/pie @nivo/sankey @nivo/treemap \
  @excalidraw/excalidraw \
  markmap-lib markmap-view \
  mermaid \
  recharts \
  roughjs \
  html-to-image \
  @tanstack/react-query
```

### Architecture Pattern

```
src/
  components/
    canvas/
      CanvasEditor.tsx          # Konva/Fabric-based visual editor
      CanvasToolbar.tsx          # Tool selection (shapes, text, draw)
    diagrams/
      FlowchartEditor.tsx       # React Flow-based flowcharts
      MindmapEditor.tsx         # React Flow + dagre for mindmaps
      OrgChart.tsx              # Tree layout diagrams
    charts/
      BarChart.tsx              # Nivo/Recharts bar charts
      PieChart.tsx              # Nivo/Recharts pie charts
      SankeyDiagram.tsx         # Nivo Sankey
      CustomChart.tsx           # Visx custom charts
    infographics/
      PyramidDiagram.tsx        # SVG-based pyramid (like napkin.ai)
      TimelineDiagram.tsx       # Horizontal/vertical timelines
      ComparisonTable.tsx       # Visual comparison grids
      ProcessFlow.tsx           # Step-by-step process visuals
    whiteboard/
      BrainstormBoard.tsx       # Excalidraw/TLDraw integration
      StickyNotes.tsx           # Collaborative sticky notes
    shared/
      ExportButton.tsx          # PNG/SVG/PDF export
      StylePanel.tsx            # Colors, fonts, themes
      IconPicker.tsx            # Icon library selector
  lib/
    ai/
      textToVisual.ts           # LLM prompt -> layout JSON
      layoutEngine.ts           # Constraint-based auto-layout
      templateMatcher.ts        # Match text patterns to templates
    export/
      svgExporter.ts            # SVG generation
      pngExporter.ts            # Canvas-to-PNG
      pdfExporter.ts            # PDF generation via jsPDF
  stores/
    canvasStore.ts              # Zustand store for canvas state
    collaborationStore.ts       # Real-time collab state
```

---

## 11. Relevance to Ripple

This reference document supports the Ripple project by identifying the exact React
libraries needed to build a **visual reporting frontend** for Ripple's simulation
outputs. Ripple generates rich structured data from its CAS-based prediction engine,
and these libraries enable:

1. **Simulation Result Visualization** -- Chart libraries (Nivo, Recharts, Visx)
   to render propagation curves, sentiment distributions, and engagement metrics

2. **Agent Topology Diagrams** -- React Flow to visualize the Star/Sea/Tribunal
   agent architecture and information flow

3. **Report Infographics** -- Konva/Fabric for generating presentation-ready
   infographic summaries of simulation runs

4. **Interactive Dashboards** -- Tremor + chart libraries for real-time
   simulation monitoring

5. **Mindmap Exploration** -- Markmap/G6 for exploring branching simulation
   scenarios and decision trees

6. **Brainstorming Integration** -- Excalidraw/TLDraw for collaborative
   hypothesis mapping before running simulations

---

## Library Comparison Matrix

| Library | Mindmaps | Charts | Diagrams | Infographics | Canvas Editor | Collab | License |
|---|:---:|:---:|:---:|:---:|:---:|:---:|---|
| React Flow | Yes | -- | Yes | -- | -- | Plugin | MIT |
| Konva | -- | -- | -- | Yes | Yes | -- | MIT |
| D3.js | -- | Yes | -- | Yes | -- | -- | ISC |
| Nivo | -- | Yes | -- | -- | -- | -- | MIT |
| Excalidraw | -- | -- | Yes | -- | Yes | Yes | MIT |
| TLDraw | -- | -- | Yes | -- | Yes | Yes | Apache-2.0 |
| Mermaid | -- | Yes | Yes | -- | -- | -- | MIT |
| Markmap | Yes | -- | -- | -- | -- | -- | MIT |
| @antv/G6 | Yes | -- | Yes | -- | -- | -- | MIT |
| GoJS | Yes | -- | Yes | -- | -- | -- | Commercial |
| Recharts | -- | Yes | -- | -- | -- | -- | MIT |
| Visx | -- | Yes | -- | -- | -- | -- | MIT |
| Fabric.js | -- | -- | -- | Yes | Yes | -- | MIT |
| Rough.js | -- | -- | Yes | -- | -- | -- | MIT |
| ECharts | -- | Yes | -- | -- | -- | -- | Apache-2.0 |

---

## Summary

To build a napkin.ai-equivalent React application, the minimum viable stack is:

1. **React Flow** -- for all node-based diagrams (flowcharts, mindmaps, org charts)
2. **Konva + react-konva** -- for the free-form canvas editor
3. **Nivo** -- for beautiful, themeable charts
4. **Excalidraw** -- for brainstorming/whiteboard features
5. **Markmap** -- for text-to-mindmap conversion
6. **D3.js** -- for any custom visualization not covered above
7. **Framer Motion** -- for polished animations and transitions

These libraries, combined with an LLM backend for text-to-layout generation,
provide all the building blocks for napkin.ai's full feature set.
