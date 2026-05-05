# Fish Cage Identification Using Remote Sensing Imagery
This repository focuses on using **Artificial Intelligence** and **Satellite Imagery** to monitor global fish farming. By automating the detection of fish cages, we provide tools to help protect coastal ecosystems from unregulated expansion.

### 🚀 Key Highlights
* **Deep Learning:** Utilizes advanced models (UNet, YOLO, DeepLabv3+) to identify aquaculture structures.
* **Multi-Sensor Data:** Integrates Optical, Radar (SAR), and Hyperspectral imagery for high-accuracy monitoring.
* **Sustainability Focus:** Designed to help researchers and environmentalists track the impact of aquaculture on marine environments.

### 🛠️ Core Challenges
We address common remote sensing hurdles such as:
* **Environmental Noise:** Overcoming interference from clouds, waves, and water turbidity.
* **The "Look-Alike" Problem:** Distinguishing man-made cages from natural reefs or dikes.
* **Data Scarcity:** Improving model generalization across different geographic regions.

---

## 📁 Project Structure

### 🎓 Training Pipeline (`model_training/`)
Train or retrain segmentation models for cage detection:
- **01_image_collector.ipynb** - Collect raw satellite imagery
- **02_image_conversion.ipynb** - Convert and prepare images for training
- **03_dataset_split.ipynb** - Split data into train/validation/test sets
- **04_model_training.ipynb** - Train the segmentation model (UNet-based)

### 🔍 Inference Pipeline (`inference/`)
Detect fish cages in new satellite imagery using a pre-trained model:
- **CageAnalysis.ipynb** - Main inference notebook for cage detection and analysis
  - Downloads Sentinel-2 imagery from Copernicus Dataspace
  - Runs model inference on satellite images
  - Generates output shapefiles with detected cage locations
  - Compares results with reference data

---

## 🚀 Quick Start

### Training a New Model
1. Gather satellite images in your area of interest
2. Convert images to appropriate format (notebook 02)
3. Split data into train/validation/test (notebook 03)
4. Train the model with your dataset (notebook 04)

### Running Inference
1. Prepare Sentinel-2 imagery (or use automatic download in CageAnalysis.ipynb)
2. Run `inference/CageAnalysis.ipynb` with your pre-trained model
3. Get detected cage locations as shapefiles and visualizations

---

**Tech Stack:** *Python | Computer Vision | Remote Sensing | Deep Learning*
