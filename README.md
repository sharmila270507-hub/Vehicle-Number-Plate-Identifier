# Vehicle-Number-Plate-Identifier
# License Plate Detection and OCR Using Python

## Overview
This project recognizes vehicle license plate text from an uploaded image using Python, OpenCV, and EasyOCR. It enhances the cropped plate image using image-processing techniques to help improve optical character recognition (OCR).

The project runs in Google Colab.

## Features
- Upload a vehicle image
- Crop the approximate license plate region
- Enlarge the plate image
- Convert the image to grayscale
- Reduce noise using bilateral filtering
- Enhance contrast using CLAHE
- Sharpen the image
- Apply Otsu and adaptive thresholding
- Recognize text using EasyOCR
- Clean and format recognized characters
- Display OCR confidence scores
- Save the cropped license plate image

## Technologies Used
- Python
- Google Colab
- OpenCV
- EasyOCR
- NumPy
- Matplotlib
- Regular Expressions

## Dataset and Input Image
This project does not automatically download a dataset. It processes a vehicle image uploaded by the user in Google Colab.

A Honda City image with a clearly visible license plate can be used as a sample input.

Image sources:
- [Honda City images – Wikimedia Commons](https://commons.wikimedia.org/wiki/Category:Honda_City)
- [License plate recognition datasets – Kaggle](https://www.kaggle.com/search?q=license+plate+recognition+dataset)

**Note:** These are image and dataset sources, not the exact original image used by the author.

## Installation
Run this command in Google Colab:

```python
!pip install -q easyocr opencv-python matplotlib
```

## How to Run
1. Open [Google Colab](https://colab.research.google.com/).
2. Create a new Python notebook.
3. Paste the project code into a code cell.
4. Run the cell.
5. Upload a vehicle image when prompted.
6. View the cropped plate and processed image versions.
7. Check the OCR results and final candidate plate number.

## Workflow
1. Upload the vehicle image.
2. Read and display the image.
3. Crop the expected license plate region.
4. Enlarge and preprocess the plate.
5. Generate enhanced, binary, and adaptive-threshold versions.
6. Run EasyOCR on the different versions.
7. Clean the recognized text.
8. Apply basic OCR character corrections.
9. Select the candidate with the highest OCR confidence.
10. Display the result and save the cropped plate image.

## Output
The program displays:
- Original vehicle image
- Cropped license plate region
- Preprocessed plate images
- Recognized text and confidence scores
- Final candidate plate number

The cropped plate image is saved as:

`/content/detected_license_plate.jpg`

## Limitations
- The current implementation uses fixed crop coordinates and may not work with every image.
- Character corrections are customized for a specific plate format.
- OCR results may be incorrect due to blur, poor lighting, viewing angle, or low image resolution.
- The highest confidence score does not guarantee a correct plate number.
- The current code does not automatically detect plate locations.

## Future Improvements
- Automatically detect license plates in different image positions.
- Support multiple vehicles in one image.
- Improve recognition across different license plate formats.
- Add a graphical user interface.
- Evaluate accuracy using a labeled test dataset.

## Author
N.Sharmila.

