# AI4Diff v1.0.0 – Executable Release

**AI4Diff** (电子显微图像晶体结构智能分析系统) is an intelligent analysis system for crystal structure and orientation recognition from transmission electron microscopy (TEM) images. It combines dynamic electron diffraction simulation with machine learning‑inspired matching algorithms to provide fast and accurate crystallographic analysis.

---

## 📢 Important Notice

**Source code** for this release is currently being updated and is **not included** in this package.  
For immediate use, please download the **standalone executable** from the [Releases](https://github.com/yourusername/AI4Diff/releases) page.

---

## Overview

AI4Diff is designed for materials scientists and crystallographers who need to determine crystal orientations or identify unknown phases from TEM/FFT patterns. It offers:

- **Orientation Recognition** – given a known crystal structure (CIF file), the software finds the best‑matching zone axis.
- **Structure Recognition** – when both the phase and orientation are unknown, it screens a set of candidate structures (local files or downloaded from [Materials Project](https://materialsproject.org)) and ranks them by match quality.

The core engine uses **dynamic electron diffraction** (Bloch‑wave formalism) to simulate diffraction patterns, and an **intelligent matching** strategy based on polar‑transform and cyclic cross‑correlation that is up to 150× faster than traditional methods.

---

## Key Features

- **File Support**  
  Load TEM images in Gatan formats (`.dm3`, `.dm4`) or common raster formats (`.png`, `.tif`, `.jpg`, `.gif`, `.bmp`).  
- **Interactive ROI Selection**  
  Choose the region of interest in real space; adjust contrast and histogram for optimal FFT quality.  
- **Diffraction Simulation**  
  Dynamic simulation using Bloch‑waves, with thickness optimisation (10–1000 Å, error ≤2%).  
- **Orientation Recognition**  
  Automatically determine the zone axis from a known CIF file.  
- **Structure Recognition**  
  Screen multiple candidate structures (local CIFs or download via Materials Project API) and rank by matching score.  
- **Rich Outputs**  
  Save matching overlays, simulated patterns, annotated images, and detailed diffraction information (CSV and XYZ files).  
- **User‑Friendly GUI**  
  Built with PySide6, providing an intuitive interface for interactive analysis.

---

## 🚀 Getting the Executable

### System Requirements
- **Operating System**: Windows 10/11 (64‑bit)  
- **Hardware**: No special requirements; typical desktop or laptop with 8 GB RAM recommended  
- **Runtime**: The executable is self‑contained – no Python installation needed.

### Download
1. Go to the **[Releases page](https://github.com/EMIT-Lab/AI4Diff/releases/)**.
2. Download the latest `AI4Diff_v1.0.0.zip` file.
3. Double‑click `AI4Diff.exe` to launch the application.  
   *(If Windows SmartScreen appears, click “More info” then “Run anyway”)*

---

## Quick Start

1. **Launch the software** – double‑click the `.exe`.
2. **Load an image** – use `File → Load Image` and select your TEM micrograph (DM3/DM4 or common formats). If no scale is embedded, a calibration dialog will appear – enter the known scale bar length.
3. **Select ROI** – in real‑space view, adjust the red square (rotate/translate) to choose the area for FFT. The FFT is automatically updated in the reciprocal‑space view.
4. **Tune FFT display** – use the histogram to improve contrast. Adjust the two concentric circles in reciprocal space to enclose the main diffraction spots – the inner circle defines the probe size, the outer circle the resolution range.
5. **Choose analysis mode** – **Orientation Recognition** (known structure) or **Structure Recognition** (unknown phase).
6. **Set parameters** – in the dialog, specify input/output paths, acceleration voltage, tolerances, etc. Hover over any field for a tooltip.
7. **Run** – click **OK** to start the calculation. For structure recognition, you can first select candidate CIFs from local files or download from Materials Project (requires an API key).
8. **View results** – matching overlays, simulated patterns, and annotated images are displayed and saved to the output folder. A CSV file with detailed diffraction information is also generated.

---

## Documentation

- The executable package includes a **User Manual** (`docs/UserManual.pdf`) with detailed instructions (in Chinese).  
- For any questions, please open an issue on GitHub.

---

## Citation

If you use AI4Diff in your research, please cite:

> to be added

---

## Contact

Developed by [EMIT Lab](https://www.ywang.group/), South China University of Technology.  
For questions or collaborations, please open an issue on GitHub.

---

**Acknowledgements**  
This work uses the [Materials Project](https://materialsproject.org) API for structure retrieval.
