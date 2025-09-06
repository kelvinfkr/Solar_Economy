# Solar_Economy

## Data-driven Solar Forecasting Enables Near-Optimal Economic Decisions

This repository contains the implementation code for the research paper **"Data-driven solar forecasting enables near-optimal economic decisions"**, a collaborative work between **NVIDIA**, **Tongji University**, **Shanghai Innovation Institution**, and **Shanghai Jiao Tong University**.

## 📋 Overview

This project implements a comprehensive solar energy forecasting system that integrates advanced machine learning models with economic optimization frameworks. The system enables near-optimal economic decisions in power grid operations by providing accurate solar power generation predictions.

## 🗂️ Repository Structure

The repository contains **5 Jupyter notebooks**, each serving a specific purpose in the solar forecasting and economic optimization pipeline:

### 1. 📥 `data_download.ipynb` - Data Acquisition
- Automated download pipeline for meteorological data
- Retrieves historical weather data and solar irradiance measurements
- Configures data storage and preprocessing
- Handles both ERA5 reanalysis and GFS forecast data sources

### 2. 🌍 `inference_era5.ipynb` - ERA5-based Inference
- Solar power forecasting using ERA5 reanalysis data
- Historical data-driven predictions
- Implements deep learning models for retrospective analysis
- Suitable for backtesting and model validation

### 3. 🌤️ `inference_gfs.ipynb` - GFS-based Inference
- Real-time solar forecasting using GFS weather predictions
- Operational forecast pipeline
- Forward-looking predictions for grid operations
- Optimized for deployment in production environments

### 4. 🔄 `pipeline.ipynb` - Complete Pipeline & Reproducibility
- **End-to-end experimental pipeline with integrated data downloading**
- Combines data acquisition, model inference
- One-stop solution for replicating research results

### 5. 📊 `visualization.ipynb` - Results Visualization
- Comprehensive visualization of forecasting results
- Generates publication-ready figures
- Performance metrics and error analysis
- Comparative analysis between predictions and ground truth

## 🚀 Quick Start

### Prerequisites

```bash
# Python 3.8 or higher
python --version

# Jupyter Notebook
pip install jupyter

# CUDA support (optional but recommended for faster inference; >40G GPU Memory)
nvidia-smi
```

### Installation

1. **Clone the repository**:
```bash
git clone https://github.com/kelvinfkr/Solar_Economy.git
cd Solar_Economy
```

2. **Install dependencies**:
Please go to https://www.nvidia.cn/high-performance-computing/earth-2/

### Usage

#### Option 1: Run the Complete Pipeline (Recommended for Paper Reproduction)
```bash
jupyter notebook pipeline.ipynb
# This notebook includes data downloading and runs all experiments from the paper
```

#### Option 2: Run Individual Components

1. **Download data**:
```bash
jupyter notebook data_download.ipynb
```

2. **Run inference** (choose one):
```bash
# For historical analysis
jupyter notebook inference_era5.ipynb

# For real-time forecasting
jupyter notebook inference_gfs.ipynb
```

3. **Visualize results**:
```bash
jupyter notebook visualization.ipynb
```

## 📊 Key Features

- **Dual Data Sources**: Supports both ERA5 reanalysis and GFS forecast data
- **State-of-the-art Models**: Advanced deep learning architectures for solar forecasting
- **Economic Integration**: Direct coupling with power grid economic optimization
- **Production Ready**: Optimized for both research and operational deployment
- **Comprehensive Validation**: Extensive experiments and performance metrics

### Data Sources
- **ERA5**: ECMWF reanalysis data for historical analysis
- **GFS**: Global Forecast System for operational predictions


## 📈 Results

Our approach achieves:
- Significant improvement in solar forecasting accuracy
- Near-optimal economic decisions 
- Robust performance across different weather conditions

## 🏢 Collaboration

This research is a joint effort between:
- **NVIDIA**
- **Tongji University**
- **Shanghai Innovation Institution**
- **Shanghai Jiao Tong University**

## 📖 Citation

If you use this code in your research, please cite our paper:

```bibtex
@article{solar_economy_2025,
  title={Data-driven solar forecasting enables near-optimal economic decisions},
  author={[Author Names]},
  journal={[Journal Name]},
  year={2025},
  institution={NVIDIA, Tongji University, Shanghai Innovation Institution, Shanghai Jiao Tong University}
}
```

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 😄 Colab
You could reproduce some results with the colab link here by uploading the plot.zip into the folder :https://colab.research.google.com/drive/1urFq3f1cjMtF29syTgPcb8Y_51cd5EIr?usp=sharing 
It is recommended running the full pipeline with the docker packed up by Nvidia:  https://www.nvidia.cn/high-performance-computing/earth-2/. It is hard to do that on colab.
If interested in running Pangu on colab, you could go to: https://github.com/kelvinfkr/Perturbation_AI_weather which runs Pangu in one click. 

## 🙏 Acknowledgments

We thank NVIDIA for computational resources, and all participating institutions for their support in this research.

---

**Note**: The `pipeline.ipynb` notebook provides the most straightforward way to reproduce all results from our paper, including automatic data downloading and complete experimental procedures.
