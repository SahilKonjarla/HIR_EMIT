# Hyperspectral Image Reconstructor (HIR) using NASA's EMIT L2A Dataset

## Overview
This repository contains the code and resources for the Hyperspectral Superresolution Image Reconstructor, a machine learning model designed to reconstruct missing wavelengths in hyperspectral data using NASA's L2A EMIT dataset on surface reflectance. The model enables accurate reconstruction of critical absorption bands of carbon dioxide and other greenhouse gases for applications in atmospheric and climate change studies.

The project was developed using Google Cloud Compute for large-scale data processing, model training, and JupyterLab for final code integration and testing.

## Repository
[GitHub Repository: HIR_EMIT](https://github.com/SahilKonjarla/HIR_EMIT)

## Key Features
- **Dataset**: NASA's EMIT L2A dataset on surface reflectance.
- **Focus**: Reconstruction of wavelengths corresponding to critical absorption bands of carbon dioxide centered at 15, 4.3, 2.7, and 2 µm.
- **Implementation**: The code uses TensorFlow, Keras for machine learning, xarray and EMIT-Data-Resoures for data processing and visualization.
- **Platform**: Developed primarily in Google Cloud Compute and tested in JupyterLab.

## Requirements
To run this code, ensure the following dependencies are installed:

- Python 3.8 or later
- JupyterLab
- Internet access to install required Python libraries from the notebook itself.
- Access to the EMIT L2A dataset (ensure the .nc file is placed in the appropriate directory).

## Getting Started
### Clone the Repository
```bash
git clone https://github.com/SahilKonjarla/HIR_EMIT.git
cd HIR_EMIT
```

### Run the Jupyter Notebooks
1. Start JupyterLab:
   ```bash
   jupyter lab
   ```

2. Open the notebooks:
   - `hyperspectral_image_reconstruction.ipynb`: For orthorectifiying, processing, and visualizing the granules.
   - `cnn_training.ipynb`: For training and testing 3 different machine learning models and test their performance.

3. Follow the instructions in each notebook to:
   - Preprocess the data.
   - Train the model.
   - Reconstruct and visualize the missing wavelengths.

### Install Dependencies
The required Python libraries will be installed directly by executing specific cells in the notebooks. Ensure you have an active internet connection for the installation.

### Access the Dataset
Place the `.nc` file (e.g., `EMIT_L2A_RFL_001_20241028T045642_2430203_015.nc`) in the repository's root directory. Ensure the file path matches the expected input path in the notebooks.

## Reproducing Results
To reproduce the results:
1. Load the dataset into the notebooks by specifying the correct file path.
2. Run each cell sequentially to:
   - Preprocess the hyperspectral data in the `hyperspectral_image_reconstruction.ipynb` file first.
   - Train the reconstruction models, in the `cnn_training.ipynb` to train, test and accumulate the necessary metrics.
   - Generate and visualize the reconstructed wavelengths.
3. Compare the output with the provided sample results in the notebooks.

## File Structure
```
HIR_EMIT/
├── hyperspectral_image_reconstruction.ipynb  # Notebook for image reconstruction
├── cnn_training.ipynb                        # Notebook for model training
├── README.md                                 # Project documentation
```

Enjoy exploring hyperspectral image reconstruction!

