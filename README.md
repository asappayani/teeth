# Dental Health AI Analyzer

This project aims to train an advanced computer vision model to analyze dental OPG (Orthopantomogram) X-ray images. The primary goal is to distinguish between healthy and unhealthy teeth, identify the reasons for the diagnosis (e.g., cavities, decay, implants), and ultimately guide users on potential next steps regarding their dental health.

## Project Overview

The core of this project is to leverage object detection to identify each tooth in a dental X-ray. By analyzing these detections, the model will learn to classify the condition of each tooth. The long-term vision is to create a tool that can:

-   **Identify and locate** every tooth in an X-ray.
-   **Classify** each tooth as "good" or "bad" based on visual indicators.
-   **Provide reasons** for its classification (e.g., identifying cavities, plaque, or other dental issues).
-   **Empower users** with a preliminary understanding of their dental health.

The dataset consists of OPG X-ray images and corresponding annotation files in YOLO format, which define bounding boxes around individual teeth.

## 🚀 Getting Started: Project Setup

This project uses Python notebooks for analysis and visualization, with `uv` for fast package management.

### Prerequisites

-   Python 3.9+
-   [uv](https://github.com/astral-sh/uv) (a fast Python package installer and resolver).
-   [Visual Studio Code](https://code.visualstudio.com/)
-   The official [Jupyter extension](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter) for VS Code.

### Installation and Setup

1.  **Clone the Repository**
    ```bash
    git clone <your-repository-url>
    cd <your-repository-directory>
    ```

2.  **Create a Virtual Environment**
    Use `uv` to create a virtual environment. This will create a `.venv` folder in your project directory.
    ```bash
    uv venv
    ```

3.  **Activate the Environment**
    You must activate the environment in your terminal before installing packages or running notebooks.
    ```bash
    source .venv/bin/activate
    ```
    *(You'll know it's active when you see `(.venv)` at the beginning of your terminal prompt.)*

4.  **Install Required Packages**
    With the environment active, use `uv` to install all necessary libraries.
    ```bash
    uv pip install opencv-python matplotlib jupyter
    ```

5.  **Configure VS Code**
    -   Open the project folder in VS Code.
    -   Open the `main.ipynb` notebook.
    -   When prompted to select a kernel, or by clicking the kernel version in the top-right corner, select the Python interpreter from your newly created virtual environment. It should be listed with a path similar to `./.venv/bin/python`.

## How to Use

The primary tool for data exploration is `main.ipynb`. This Jupyter notebook contains helper functions to:
-   Load an X-ray image.
-   Read its corresponding YOLO annotation file.
-   Draw the bounding boxes on the image.
-   Display the result.

This allows you to visually inspect the dataset and verify that the annotations correctly correspond to the teeth in the images.
