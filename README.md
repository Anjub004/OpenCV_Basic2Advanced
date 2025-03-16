# OpenCV Basics in Jupyter Notebook

## Overview
This project contains basic OpenCV code implemented in a Jupyter Notebook. OpenCV (Open Source Computer Vision Library) is widely used for computer vision tasks such as image processing, object detection, and video analysis.

## Prerequisites
Before running the code, ensure you have the following installed:
- Python (>=3.6)
- Jupyter Notebook
- OpenCV (`cv2`)
- NumPy

## Installation
Follow these steps to set up the environment:

### Install Python and Jupyter Notebook
If you don’t have Python and Jupyter installed, install them using Anaconda:
```bash
conda install -c anaconda jupyter
```
Or install manually using pip:
```bash
pip install notebook
```

### Install OpenCV and Dependencies
```bash
pip install opencv-python numpy matplotlib
```

## Running the Jupyter Notebook
To start Jupyter Notebook, run:
```bash
jupyter notebook
```
Open the `.ipynb` file and execute the cells step by step.

## Basic OpenCV Operations
The Jupyter Notebook covers the following:
1. **Reading and Displaying an Image**
    ```python
    import cv2
    img = cv2.imread('image.jpg')
    cv2.imshow('Image', img)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
    ```
2. **Converting an Image to Grayscale**
    ```python
    gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)
    cv2.imshow('Grayscale Image', gray)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
    ```
3. **Drawing Shapes on an Image**
    ```python
    cv2.rectangle(img, (50, 50), (200, 200), (0, 255, 0), 3)
    cv2.circle(img, (150, 150), 50, (255, 0, 0), -1)
    cv2.imshow('Shapes', img)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
    ```
4. **Edge Detection using Canny Algorithm**
    ```python
    edges = cv2.Canny(gray, 100, 200)
    cv2.imshow('Edges', edges)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
    ```

## Additional Notes
- Ensure `cv2.imshow()` works in your environment; if not, use `matplotlib` for displaying images inside Jupyter Notebook:
    ```python
    import matplotlib.pyplot as plt
    plt.imshow(cv2.cvtColor(img, cv2.COLOR_BGR2RGB))
    plt.show()
    ```
- Use `cv2.waitKey(0)` to pause until a key is pressed; for continuous video streams, use `cv2.waitKey(1)`.

## Contributing
Feel free to contribute by adding more OpenCV functionalities!

## License
This project is open-source and available under the MIT License.

