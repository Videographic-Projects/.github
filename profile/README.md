# Digital Video Investigation Project List


## Rebuffer Chart Maker

A visualization tool for creating and analyzing rebuffer trade-off charts for adaptive bitrate streaming.

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
