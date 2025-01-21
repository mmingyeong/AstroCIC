# AstroCIC

**AstroCIC: A Python Library for Efficient 3D Data Analysis and Density Mapping**

AstroCIC is a Python library designed for efficient analysis of 3D spatial data, particularly in astronomy and large-scale scientific datasets. It provides a streamlined workflow for statistical analysis, distribution visualization, and density mapping using the Cloud-in-cell (CIC) method.

## Features

- **Input**: Handles 3D coordinate data (`x, y, z`) with support for large datasets.
- **Statistical Analysis**:
  - Compute basic and spatial statistics (e.g., mean, standard deviation, min/max values).
  - Export results to a readable text file.
- **Data Distribution Analysis**:
  - Generate 1D and 2D histograms with optional log-scale.
  - Supports data sampling and axis-based filtering.
- **Density Mapping**:
  - Generate high-resolution 3D density maps using the CIC method.
  - Visualize density slices in `XY`, `YZ`, and `XZ` planes.
- **Optimized for Performance**:
  - Accelerated with GPU computing using CuPy.
  - Supports parallel processing for large datasets.

## Why AstroCIC?
AstroCIC simplifies the process of analyzing and visualizing 3D data, making it an excellent choice for researchers in cosmology, astronomy, and other scientific domains requiring efficient spatial analysis.

## Installation

Install AstroCIC using pip:

```bash
pip install astroCIC
```

## Example Usage

```python
import astroCIC as ac

# Load your 3D data
data = ac.load_data('path_to_data')

# Compute basic statistics
stats = ac.compute_statistics(data)
ac.save_statistics(stats, 'output_stats.txt')

# Generate and visualize density maps
density_grid = ac.generate_density_map(data, grid_size=256, sample_rate=0.01)
ac.plot_density_maps(density_grid)
```

## Tags

`3D Data Analysis`, `Astronomy`, `Cloud-in-cell`, `Cosmology`, `Python`, `Density Mapping`, `Scientific Computing`

## License

This project is licensed under the MIT License. See the LICENSE file for details.
