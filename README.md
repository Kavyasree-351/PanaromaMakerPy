# 🖼️ OpenPanoramaMaker

A lightweight Python application for automatically creating image panoramas using OpenCV. The project streamlines the complete panorama generation workflow—from downloading images stored on Google Drive to validating inputs, stitching images together, and exporting the final panorama.

Designed to run in Google Colab, OpenPanoramaMaker provides a simple and reproducible pipeline for students, researchers, and photography enthusiasts who want to generate panoramas without manually managing datasets or image processing steps.

---

## Overview

Creating panoramas typically involves collecting overlapping images, loading them into memory, handling invalid inputs, running a stitching algorithm, and exporting the final output. This project automates those steps into a single workflow.

The application:

- Downloads an entire image dataset directly from Google Drive
- Detects supported image formats automatically
- Loads and validates images before processing
- Uses OpenCV's panorama stitching pipeline to generate a panorama
- Reports errors when stitching cannot be completed
- Saves and previews the final stitched image

---

## Features

- Automatic image download from Google Drive
- Support for JPG and PNG images
- Image validation before processing
- Panorama generation using OpenCV
- Automatic output saving
- Interactive preview inside Google Colab
- Clear error handling and informative messages
- Simple, reproducible workflow

---

## Technologies Used

- Python 3
- OpenCV
- gdown
- Google Colab
- Google Drive

---

## Project Structure

```
OpenPanoramaMaker/
│
├── OpenPanoramaMaker.ipynb
├── README.md
└── sample_images/
```

---

## Installation

Install the required dependencies.

```bash
pip install opencv-python gdown
```

---

## Usage

### Step 1 — Prepare Images

Upload a folder of overlapping images to Google Drive.

Images should:

- Have sufficient overlap
- Be captured from approximately the same viewpoint
- Be in JPG or PNG format

---

### Step 2 — Download Dataset

Specify your Google Drive folder ID.

```python
folder_id = "YOUR_FOLDER_ID"
```

The notebook downloads all images automatically using **gdown**.

---

### Step 3 — Load Images

Images are automatically:

- Located
- Sorted
- Read into memory
- Validated before stitching

If an image cannot be loaded, the program raises an informative error instead of failing silently.

---

### Step 4 — Generate Panorama

The application uses OpenCV's panorama stitching API to combine all images into a single panorama.

During this stage the program:

- Processes all loaded images
- Performs feature matching and alignment through OpenCV
- Generates the panorama
- Reports stitching status

---

### Step 5 — Save Output

The generated panorama is automatically saved as

```
panorama_result.jpg
```

and displayed inside Google Colab.

---

## Example Workflow

```
Google Drive Folder
          │
          ▼
 Download Images
          │
          ▼
 Validate Images
          │
          ▼
 Load into Memory
          │
          ▼
 OpenCV Stitcher
          │
          ▼
 Panorama Generated
          │
          ▼
 Save & Display Output
```

---

## Error Handling

The program checks for several common issues before stitching.

Examples include:

- Missing images
- Unsupported file formats
- Corrupted image files
- Failed panorama generation
- Invalid Google Drive folder

Meaningful exceptions are raised to help identify the problem quickly.

---

## Requirements

- Python 3.7+
- OpenCV
- gdown
- Google Colab
- Google Drive

---

## Future Improvements

Potential enhancements include:

- Automatic image ordering
- Feature match visualization
- Image resizing for faster processing
- Exposure compensation
- Cylindrical and spherical projection options
- Command-line interface (CLI)
- Desktop GUI version
- Batch panorama generation

---

## Learning Outcomes

This project strengthened my understanding of:

- Image loading and preprocessing
- File handling in Python
- Error handling
- Working with OpenCV
- Automating data pipelines
- Managing datasets stored on Google Drive
- Building reproducible computer vision workflows

---

## Acknowledgements

This project uses OpenCV's panorama stitching implementation for image alignment and stitching, while providing an automated workflow for dataset retrieval, validation, processing, and result generation.

---

## License

This project is available under the MIT License.
