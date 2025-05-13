# Digital Video Investigation Project List


## [Rebuffer Chart Maker](https://github.com/Videographic-Projects/rebuffer-chart-maker)

A visualization tool for creating and analyzing rebuffer trade-off charts for adaptive bitrate streaming.

[Project Poster](https://github.com/Videographic-Projects/rebuffer-chart-maker/blob/main/Adaptive%20Bitrate%20Streaming%20Simulation.pdf)
<br>
[Project Research Paper](https://github.com/Videographic-Projects/rebuffer-chart-maker/blob/main/Adaptive%20Bitrate%20Streaming%20Simulation%20Report_CB_Final.pdf)


### Overview

This tool generates high-quality visualization graphs for analyzing the relationship between segment length, smoothing window configurations, and buffering in adaptive video streaming. These visualizations help identify optimal settings for minimizing rebuffering while maximizing bitrate.

### Key Files

- **plot-maker.py**: Core visualization engine with customizable styling and chart generation
- **visualization_styles.py**: Shared styling components for consistent visual identity
- **buffer_dynamics.py**: Buffer behavior visualization for understanding playback dynamics
- **heatmap_analysis.py**: Heatmaps for comparing multiple metrics simultaneously
- **tradeoff_analysis.py**: Line charts showing relationships between configuration variables
- **sweep_results.csv**: Sample data for visualization (segment lengths, smoothing windows, etc.)

```text
rebuffer-chart-maker/
├── plot-maker.py              # Main visualization script with configurable styling
├── visualization_styles.py    # Shared UI components and styling utilities
├── buffer_dynamics.py         # Buffer behavior visualization tool
├── heatmap_analysis.py        # Heatmap generation for multi-variable analysis
├── tradeoff_analysis.py       # Line charts for parameter relationship analysis
├── markov-chain.py            # Network state transition modeling
├── config.yaml                # Configuration settings
├── requirements.txt           # Python dependencies
├── sweep_results.csv          # Sample data for visualizations
└── img/                       # Generated visualization outputs
    ├── buffer_dynamics.png
    ├── heatmap_analysis.png
    └── tradeoff_analysis.png
```

### How to Use

1. Ensure Python and required dependencies are installed (matplotlib, pandas, numpy, seaborn)
2. Run any of the visualization scripts:
   ```bash
   python plot-maker.py    # For trade-off analysis
   python buffer_dynamics.py    # For buffer behavior visualization
   ```
3. Customize visualizations by modifying parameters in the script files

### Visualizations Available

- **Trade-off Analysis**: Compares rebuffer time and bitrate across different segment lengths and smoothing windows
- **Buffer Dynamics**: Illustrates buffer filling and depleting during streaming
- **Heatmap Analysis**: Combines multiple metrics into color-coded heatmaps

### Learning Insights

This project demonstrates:
- How segment length and smoothing window settings affect streaming performance
- The trade-offs between video quality (bitrate) and playback stability (rebuffering)
- Data visualization techniques for complex multi-variable relationships
- Implementation of professional-grade matplotlib visualizations with custom styling
- How to build a modular visualization system with reusable components

### Sample Output

The visualizations help identify optimal configuration points where both rebuffering is minimized and video quality is maximized, which is crucial for adaptive bitrate streaming algorithms.



## [Interactive Video Player Playground](https://github.com/Videographic-Projects/video-player-playground)

A next-generation video player with advanced adaptive streaming capabilities, performance metrics visualization, and interactive controls.

### Overview

This Next.js application provides a platform for experimenting with video playback technologies, focusing on adaptive bitrate streaming implementation and analysis. The playground allows users to test different streaming strategies, visualize performance metrics in real-time, and understand the impact of various configurations on video delivery quality.

### Key Files

- **VideoPlayer.tsx**: Core player component with adaptive streaming support and advanced controls
- **VideoLibrary.tsx**: Media browsing interface with thumbnail generation and filtering
- **BitrateMetrics.tsx**: Real-time visualization of streaming performance metrics
- **useVideoControls.tsx**: Custom hook for unified player control logic
- **VideoCard.tsx**: Reusable component for displaying video thumbnails with metadata

```text
video-player-playground/
├── src/
│   ├── app/
│   │   ├── components/
│   │   │   ├── VideoPlayer.tsx       # Main player with adaptive streaming support
│   │   │   ├── VideoLibrary.tsx      # Media browsing interface
│   │   │   ├── BitrateMetrics.tsx    # Performance metrics visualization
│   │   │   └── VideoCard.tsx         # Thumbnail display component
│   │   ├── hooks/
│   │   │   └── useVideoControls.tsx  # Unified player control logic
│   │   ├── utils/
│   │   │   └── adaptive-streaming.ts # Streaming algorithm implementations
│   │   ├── api/
│   │   │   └── video/                # Video processing endpoints
│   │   ├── page.tsx                  # Main application page
│   │   └── layout.tsx                # Application layout structure
├── public/
│   └── Videos/                       # Sample video content for testing
├── tailwind.config.ts                # UI styling configuration
├── next.config.ts                    # Next.js configuration
└── package.json                      # Project dependencies
```

### How to Use

1. Install dependencies with npm, yarn, or pnpm:
   ```bash
   npm install
   ```
2. Start the development server:
   ```bash
   npm run dev
   ```
3. Open http://localhost:3000 in your browser to explore the video player

### Features Available

- **Adaptive Bitrate Streaming**: DASH protocol implementation with configurable parameters
- **Real-time Performance Metrics**: Visualize bitrate, buffer length, and download speed
- **Interactive Controls**: Keyboard shortcuts, custom UI controls, and playback settings
- **Responsive Design**: Elegant animations and layout adaptations for different screen sizes
- **Custom Aspect Ratios**: Support for various video formats and aspect ratio controls

### Learning Insights

This project demonstrates:
- Implementation of adaptive streaming algorithms in a modern web framework
- Real-time performance metric visualization techniques
- Progressive enhancement for video playback user experience
- Component-based architecture for media applications
- Integration between low-level media APIs and high-level UI components
- Animation techniques for smooth transitions between player states

### Sample Experience

The interactive player provides insights into how adaptive streaming decisions affect user experience, allowing developers to test and visualize different approaches to video delivery optimization in a controlled environment.
