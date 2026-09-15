
# IMPLEMENTATION-OF-EROSION-AND-DILATION

### Aim
To write a Python program using OpenCV to perform morphological operations such as Erosion and Dilation on an image.

### The program performs the following operations:

Image Erosion
Image Dilation
Software Used
Anaconda – Python 3.7
Jupyter Notebook / VS Code
OpenCV (cv2)
NumPy
Matplotlib
### Algorithm
#### Step 1:
Import the required libraries: OpenCV, NumPy, and Matplotlib.

#### Step 2:
Create a blank image using NumPy.

#### Step 3:
Insert text onto the image using OpenCV's text drawing function.

#### Step 4:
Display the original image.

#### Step 5:
Create a structuring element (kernel) of suitable size.

#### Step 6: Image Erosion
Apply the erosion operation using the created kernel.
Remove pixels from the boundaries of foreground objects.
Display the eroded image.
#### Step 7: Image Dilation
Apply the dilation operation using the same kernel.
Add pixels to the boundaries of foreground objects.
Display the dilated image.
#### Step 8:
Compare the original, eroded, and dilated images.

### Program
#### Developed By
##### Name: DEEPIKA R

##### Register No: 212224230054

### Output
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
```
def load_img():
    blank_img = np.zeros((600,600))

    font = cv2.FONT_HERSHEY_SIMPLEX

    cv2.putText(blank_img,
                text='deepi',
                org=(50,300),
                fontFace=font,
                fontScale=5,
                color=(255,255,255),
                thickness=25,
                lineType=cv2.LINE_AA)

    return blank_img
```
```
def display_img(img):

    fig = plt.figure(figsize=(12,10))
    ax = fig.add_subplot(111)
    ax.imshow(img, cmap='gray')
    ax.set_title("Image")
    plt.axis("off")
    plt.show()
```
```
img = load_img()
display_img(img)
```


<img width="1347" height="802" alt="Screenshot 2026-09-15 082636" src="https://github.com/user-attachments/assets/f54f436b-bc7e-4672-bbba-947e0bbe4838" />




```
kernel = np.ones((5,5), np.uint8)
```
```
def display_img(img):

    fig = plt.figure(figsize=(12,10))
    ax = fig.add_subplot(111)
    ax.imshow(img, cmap='gray')
    ax.set_title("Erosion")
    plt.axis("off")
    plt.show()
```
```
eroded_img = cv2.erode(img, kernel, iterations=3)
```
```
display_img(eroded_img)
```
<img width="1212" height="807" alt="Screenshot 2026-09-15 082754" src="https://github.com/user-attachments/assets/1fb07ef9-2b27-4dfe-9518-c39c6fc14ebf" />



```
kernel = np.ones((5,5), np.uint8)
```
```
def display_img(img):

    fig = plt.figure(figsize=(12,10))
    ax = fig.add_subplot(111)
    ax.imshow(img, cmap='gray')
    ax.set_title("Dilated")
    plt.axis("off")
    plt.show()
```
```
def display_img(img):

    fig = plt.figure(figsize=(12,10))
    ax = fig.add_subplot(111)
    ax.imshow(img, cmap='gray')
    ax.set_title("Dilated")
    plt.axis("off")
    plt.show()
```
```
dilated_img = cv2.dilate(img, kernel, iterations=8)
```
```
display_img(dilated_img)
```

<img width="1312" height="807" alt="image" src="https://github.com/user-attachments/assets/1705780c-e576-4b6b-bb26-c65a30b6428e" />



#### Result
Thus, the morphological operations Erosion and Dilation are successfully implemented using OpenCV.
