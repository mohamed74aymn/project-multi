# Image Processing Application

This Python application processes an image by converting it to grayscale, applying a binary threshold, resizing the image based on pixel characteristics, and saving the result as a binary image.

## Features

- **Grayscale Conversion**: Converts the input image to grayscale.
- **Binary Thresholding**: Applies a threshold to convert the grayscale image to black-and-white (binary).
- **Dynamic Resizing**: Resizes the image based on the number of unique pixel values to optimize file size and performance.
- **Output**: Saves the processed image in the same directory as the input file, with the suffix `_binary`.

## Requirements

- Python 3.x
- Libraries:
  - `Pillow` (Python Imaging Library fork)
  - `NumPy`

Install the dependencies using:
```bash
pip install Pillow numpy
How It Works
User Input: Prompts the user to enter the path of an image file for processing.
Load Image: Loads the image using the Pillow library.
Pixel Count: Calculates the total number of pixels in the image before and after processing.
Grayscale and Binary Conversion: Converts the image to grayscale and applies a binary threshold.
Resizing:
If the image has ≤ 10 unique pixel values, it is scaled down to 30% of the original size.
For 11–50 unique values, it is scaled down to 60%.
If the image has more than 50 unique values, no resizing is applied.
Saving Output: The processed image is saved in the same directory as the input file, with _binary appended to the file name.
