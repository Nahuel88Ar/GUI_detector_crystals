# 📄 Chlamydomonas Crystal Detection GUI

A Python-based graphical user interface (GUI) to **detect and analyze intracellular crystals** in *Chlamydomonas* algae using bright-field (BF) and polarized light (PL) microscopy images.

---

## ⭐ Features

- Detects and segments **cells** and **crystals**.
- Supports batch processing of images.
- Calculates:
  - Number and percentage of cells with crystals.
  - Crystal area and relative area per cell.
  - Total cell areas and cell counts.
- Generates plots to visualize results over time (e.g., days).
- Exports detailed Excel datasets and annotated images.

---

## 🧬 Use Case

Designed specifically for microscopy studies on *Chlamydomonas* algae to quantify and analyze crystal formation inside cells under different experimental conditions.

---

## 💻 Installation

### Requirements

- Python 3.x
- Install dependencies:

```bash 
pip install opencv-python opencv-python-headless numpy pandas openpyxl matplotlib PyQt5 imageio scikit-image scipy scikit-learn xlsxwriter
```
Also you can use the file requirements.txt to install all dependencies.

- **Recommended IDE:** PyCharm (or any Python IDE supporting GUI execution).

---

## 🟢 Getting Started

### 1️⃣ Clone the repository

```bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
```

### 2️⃣ Run the GUI

```bash
python GUI_FINAL_CLEAN.py
```

Or open the file in PyCharm and run it.

---

## 🗺️ Workflow

### Add Scales

To calculate cell and crystal areas in µm², you need a pixel-to-micrometer scale.

- Use [ImageJ](https://imagej.net/ij/):
  - Open an image containing a scale bar.
  - Draw a line over the scale bar.
  - Go to **Analyze → Measure** to get pixel length.
  - Add this scale to the GUI using **"Set µm to px Scale"**.

---

### Prepare Images

- Images should be named with a **day number and letter**, for example:
  ```
  1A, 1B, 1C
  2A, 2B, 2C
  ```
- Separate **BF** and **PL** images into different folders.

---

### Select Folders

- **BF Folder**: Bright-field images.
- **PL Folder**: Polarized light images.
- **Output Folder**: Folder where results (annotated images, Excel files) will be saved.

⚠️ **Important:** Change or empty the output folder for each batch to avoid overwriting previous results.

---

### Run Analyses

#### Number of Crystals

- Counts cells with crystals and plots % of cells with crystals over time.

#### Areas

- Calculates crystal areas and their percentage relative to cell areas.
- Generates plots over time.

#### Number of Cells

- Counts cells and measures cell areas.
- Outputs segmentation images, overlap images, and histograms (no time plots).

---

### Stop / Restart

- You can stop or restart batch processing at any time.

---

## 📄 Output Data

### Per Image — Cells

- **Region Label**: Cell ID.
- **Region Area (pixels)** and **Region Area (µm²)**.
- **Total Area**.
- **Total Cells**.

### Per Image — Crystals

- **Region Label**: Crystal ID.
- **Associated Cell**: Linked cell ID.
- **Overlap**: Overlapping area with cell.
- **Region Area (pixels)** and **Region Area (µm²)**.
- **Associated Cell Count**: Number of crystals per cell.
- **Total Cells with Crystals**.
- **Total Area Crystals**.

### Summary Table (Per Folder)

- **Days**: Day number.
- **Mean Percentage**: Average % of cells with crystals.
- **Standard Deviation**.

---

## 🧹 Utilities

- Add/delete scales easily within the GUI.
- Automatically saves and loads scales for future analyses.

---

## ⚖️ License

MIT License

---

## 🙌 Acknowledgments

This tool was designed to support *Chlamydomonas* algae research, enabling accurate quantification and visualization of intracellular crystals under different experimental conditions.

---

## 📬 Contact

For questions or contributions, please open an issue or contact [[your-email@example.com](mailto\:nahuelutn88@gmail.com)].

