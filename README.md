# Exp-1-DIP-
Image-Handling-and-Pixel-Transformations-Using-OpenCV
# AIM:
To perform basic image processing operations using OpenCV, including drawing shapes, adding text, color space conversion, resizing, cropping, flipping, and displaying images.

# Software Required:
Anaconda - Python 3.7
Jupyter Notebook (for interactive development and execution)

# Algorithm:

Step 1:
Import the required libraries (OpenCV and Matplotlib).

Step 2:
Load the input image from the local directory.

Step 3:
Perform the required image processing operation (drawing shapes/text, color conversion, resizing, cropping, flipping, or modifying pixels).

Step 4:
Convert the image from BGR to RGB whenever required for correct display.

Step 5:
Display the processed image using Matplotlib.

Program Developed By:
Name: HARISH G

Register Number: 212224110020

### PROGRAM
1) Load an image from your local directory and display it.

```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread('dog.jpg', cv2.IMREAD_COLOR)
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
plt.imshow(img_rgb, cmap='viridis') 
plt.title("Original Image")
plt.axis('off')
plt.show()
```
2) Draw a line from the top-left to the bottom-right of the image
```
image = cv2.imread('1.jpg') 
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
img_rgb.shape
line_img = cv2.line(img_rgb, (0, 0), (735, 1103), (255, 0, 0), 15) # cv2.line(image, start_point, end_point, color, thickness)
plt.imshow(line_img, cmap='viridis')  
plt.title("Image with Line")
plt.axis('off')  
plt.show()
```

3) Draw a circle at the center of the image.

```
image = cv2.imread('1.jpg') 
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
img_rgb.shape
circle_img = cv2.circle(img_rgb,(368, 471),150,(0,0,0),20) # cv2.circle(image, center, radius, color, thickness)
plt.imshow(circle_img, cmap='viridis')  
plt.title("Image with Circle")
plt.axis('off')  
plt.show()
```

4) Draw a rectangle around a specific region of interest in the image.

```
image = cv2.imread('1.jpg') 
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
img.shape
rectangle_img = cv2.rectangle(img_rgb, (0, 0),(736, 1104), (255, 0, 0), 20)  # cv2.rectangle(image, start_point, end_point, color, thickness)
plt.imshow(rectangle_img, cmap='viridis')  
plt.title("Image with Rectangle")
plt.axis('off')  
plt.show()

```

5) Add the text" HARISH G" at the top-left corner of the image.

```
image = cv2.imread('1.jpg') 
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
text_img = cv2.putText(img_rgb, "HARISH", (10, 30), cv2.FONT_HERSHEY_SIMPLEX, 1, (0, 255, 0), 5)  ## cv2.putText(image, text, position, font, font_scale, color, thickness)
plt.imshow(text_img, cmap='viridis')  
plt.title("Image with Text")
plt.axis('off')  
plt.show()
```

6) Bring back the original image

```
image = cv2.imread('2.jpg')
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
plt.imshow(image_rgb)
plt.title("Original RGB Image")
plt.axis("off")
```
7) Convert the input RGB photo into HSV image
```
image_hsv = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2HSV)
plt.imshow(image_hsv)
plt.title("HSV Image")
plt.axis("off")
```
8) Convert the input RGB photo into Grayscale image
```
image_gray = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2GRAY)
plt.imshow(image_gray, cmap='gray')
plt.title("Grayscale Image")
plt.axis("off")
```
9) Convert the input RGB photo into YCrCB image
```
image_ycrcb = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2YCrCb)
plt.imshow(image_ycrcb)
plt.title("YCrCb Image")
plt.axis("off")
```
10) Convert the input HSV photo into RGB image
```
image_hsv_to_rgb = cv2.cvtColor(image_hsv, cv2.COLOR_HSV2RGB)
plt.imshow(image_hsv_to_rgb)
plt.title("HSV to RGB Image")
plt.axis("off")
```
11) Print image with a 300x300 White Block

```
image[200:500, 200:500] = [255, 255, 255]
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
plt.imshow(image_rgb)
plt.title("Image with 300x300 White Block")
plt.axis("off")
plt.show()
```
12) Resize the original image to half its size and display it.
```
image = cv2.imread('2.jpg') 
image.shape
resized_image = cv2.resize(image, (736 // 2, 1104 // 2))
resized_image_rgb = cv2.cvtColor(resized_image, cv2.COLOR_BGR2RGB)
resized_image_rgb.shape
plt.imshow(resized_image_rgb)
plt.title("Resized Image (Half Size)")
plt.axis("off")
plt.show()
```
13) Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.
```
image = cv2.imread('2.jpg') 
image.shape
roi = image[50:350, 50:350]
roi_rgb = cv2.cvtColor(roi, cv2.COLOR_BGR2RGB)
plt.imshow(roi_rgb)
plt.title("Cropped Region of Interest (ROI)")
plt.axis("off")
plt.show()
```
14)  Flip the original image horizontally and display it.
```
image = cv2.imread('2.jpg')
flipped_horizontally = cv2.flip(image, 1)
flipped_horizontally_rgb = cv2.cvtColor(flipped_horizontally, cv2.COLOR_BGR2RGB)
plt.imshow(flipped_horizontally_rgb)
plt.title("Flipped Horizontally")
plt.axis("off")
```
15) Flip the original image vertically and display it.
```
flipped_vertically = cv2.flip(image, 0)
flipped_vertically_rgb = cv2.cvtColor(flipped_vertically, cv2.COLOR_BGR2RGB)
plt.imshow(flipped_vertically_rgb)
plt.title("Flipped Vertically")
plt.axis("off")
```

### OUTPUT

<img width="736" height="1008" alt="dog" src="https://github.com/user-attachments/assets/102fe19b-e591-479e-9050-270dc48d5180" />


### RESULT
The required image processing operations were successfully performed using OpenCV, and the output images were displayed correctly for each task.
