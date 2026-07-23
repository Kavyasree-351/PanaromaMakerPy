# 🖼️ PanoramaMakerPy

PanoramaMakerPy is a Python application that automates the process of creating image panoramas from a sequence of overlapping photographs. The program downloads images from a Google Drive folder, loads and validates them, stitches them into a panorama using OpenCV, and saves the final output.

This project was built to simplify the panorama creation workflow and to explore image processing using OpenCV in a Google Colab environment.

---

## Features

- Download images directly from a Google Drive folder
- Support for JPG and PNG image formats
- Automatic image loading and validation
- Panorama generation using OpenCV
- Save the generated panorama automatically
- Preview the panorama in Google Colab
- Error handling for invalid images and stitching failures

---

## Project Structure

```
PanoramaMakerPy/
│
├── panorama.py
├── README.md
├── requirements.txt
├── sample_images/
│   ├── image1.jpg
│   ├── image2.jpg
│   └── image3.jpg
└── output/
    └── panorama_result.jpg
```

---

## Technologies Used

- Python
- OpenCV
- Google Colab
- Google Drive
- gdown

---

## Installation

Clone the repository:

```bash
git clone https://github.com/Kavyasree-351/PanaromaMakerPy.git
cd PanaromaMakerPy
```

Install the required packages:

```bash
pip install -r requirements.txt
```

---

## Running the Project

1. Upload a folder containing overlapping images to Google Drive.
2. Set the Google Drive folder ID in the program.
3. Run `panorama.py`.
4. The program will:
   - Download the images
   - Validate the image files
   - Stitch them into a panorama
   - Save the final panorama

---

## Output

The generated panorama is saved as:

```
output/panorama_result.jpg
```

A sample output is included in the `output` folder.

---

## Sample Images

The `sample_images` folder contains example images used for testing the panorama stitching process.

For best results:

- Use images with sufficient overlap.
- Keep lighting conditions similar across images.
- Avoid large viewpoint changes.

---

## Error Handling

The application checks for common issues, including:

- Missing or unreadable images
- Unsupported file formats
- Failed panorama stitching
- Invalid Google Drive folder

If an issue occurs, the program provides an informative error message to help identify the problem.

---

## Future Improvements

Some ideas for future development include:

- Automatic image ordering
- Image resizing for faster processing
- Feature match visualization
- Batch panorama generation
