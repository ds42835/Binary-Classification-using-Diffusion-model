# <center>Binary-Classification-using-CNN</center>
# Binary Classification with Diffusion Models

This project demonstrates binary classification using a diffusion model with PyTorch. It classifies images of cats and dogs while showcasing the diffusion process for image transformation.

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Requirements](#requirements)
- [Dataset](#dataset)
- [Usage](#usage)
- [Results](#results)
- [Acknowledgments](#acknowledgments)

## Overview
This project explores the potential of diffusion models for binary classification. It also incorporates a basic classifier for distinguishing between cats and dogs.

## Features
- **Diffusion Process Visualization**: Forward and reverse steps of the diffusion process.
- **Binary Classification**: Simple classifier for cats and dogs.
- **Interactive Prediction**: User input for classifying custom images.

## Requirements
Install dependencies using the following command:
```bash
pip install -r requirements.txt
```

## Dataset
The dataset consists of three classes:
- Cats
- Dogs
- Neither (Optional, extendable)

Place your dataset in the following structure:
```
data/
├── cats/
├── dogs/
└── neither/  # Optional
```

## Usage
1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/project-name.git
   ```
2. Train the diffusion model:
   ```bash
   python src/train_diffusion.py
   ```
3. Train the classification model:
   ```bash
   python src/train_classifier.py
   ```
4. Classify an image:
   ```bash
   python src/predict.py
   ```

## Results
Include sample outputs and visualizations:
- **Diffusion Process**: Before and after noise addition/removal.
- **Classification Accuracy**: X% on the test dataset.

## Acknowledgments
Inspired by research on diffusion models and binary classification techniques.

## License
This project is licensed under the MIT License.
"""

# Creating Repository Files
import os

# Define folder structure
folders = [
    "data",
    "models",
    "notebooks",
    "src"
]

files = {
    "README.md": README_CONTENT,
    "requirements.txt": "torch\ntorchvision\nPillow\nmatplotlib\ntqdm\ntimm\n",
    "LICENSE": "MIT License\n\nCopyright (c) 2025 Dinesh Sharma\n\nPermission is hereby granted, free of charge, to any person obtaining a copy\nof this software and associated documentation files (the \"Software\"), to deal\nin the Software without restriction, including without limitation the rights\nto use, copy, modify, merge, publish, distribute, sublicense, and/or sell\ncopies of the Software, and to permit persons to whom the Software is\nfurnished to do so, subject to the following conditions:\n\nThe above copyright notice and this permission notice shall be included in\nall copies or substantial portions of the Software.\n\nTHE SOFTWARE IS PROVIDED \"AS IS\", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR\nIMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,\nFITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE\nAUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER\nLIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,\nOUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE\nSOFTWARE."
}

# Code Files
src_files = {
    "dataset.py": """# Dataset-related code from the user\n...\n""",
    "models.py": """# Diffusion and classification model classes\n...\n""",
    "train_diffusion.py": """# Code for training diffusion model\n...\n""",
    "train_classifier.py": """# Code for training classification model\n...\n""",
    "utils.py": """# Utility functions\n...\n"""
}

# Create folders
for folder in folders:
    os.makedirs(folder, exist_ok=True)

# Create files
for file_name, content in files.items():
    with open(file_name, "w") as file:
        file.write(content)

for file_name, content in src_files.items():
    with open(os.path.join("src", file_name), "w") as file:
        file.write(content)
