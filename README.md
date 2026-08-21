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
<img width="381" height="541" alt="image" src="https://github.com/user-attachments/assets/20771e60-9052-4c72-ade2-c92dd4050d7a" />
<img width="400" height="538" alt="image" src="https://github.com/user-attachments/assets/f19a4e18-9104-4d05-ae30-873d597d48b2" />
<img width="395" height="536" alt="image" src="https://github.com/user-attachments/assets/ceca4edc-8fdd-408c-95e9-12eb58e1bdad" />
<img width="400" height="542" alt="image" src="https://github.com/user-attachments/assets/d68fedef-2a2a-4217-bf63-6666d38ac61d" />
<img width="371" height="533" alt="image" src="https://github.com/user-attachments/assets/e10751ba-5778-4dda-983f-bc818b23bcfc" />
<img width="392" height="550" alt="image" src="https://github.com/user-attachments/assets/33bd3ddb-bef5-4a63-8d4d-ef9366f77054" />
<img width="419" height="548" alt="image" src="https://github.com/user-attachments/assets/890c8d50-80bc-4413-9a12-19fdc27e3cc3" />
<img width="363" height="532" alt="image" src="https://github.com/user-attachments/assets/2d568876-5a40-4388-942d-177c167b07a7" />
<img width="370" height="526" alt="image" src="https://github.com/user-attachments/assets/90bdaf5b-6473-46c0-a2dd-7f4228b2dd87" />
<img width="395" height="558" alt="image" src="https://github.com/user-attachments/assets/61558b73-ce45-4e44-a634-2f7bb334c7a1" />
<img width="403" height="537" alt="image" src="https://github.com/user-attachments/assets/15792409-e194-42a2-801a-60b44ddb18ac" />
<img width="680" height="544" alt="image" src="https://github.com/user-attachments/assets/4db515b7-618a-4315-9005-3fdaa05f93b5" />
<img width="507" height="558" alt="image" src="https://github.com/user-attachments/assets/ba51e774-c3e4-475c-a7e7-567ea4531862" />
<img width="401" height="545" alt="image" src="https://github.com/user-attachments/assets/2d153184-d8b1-4fef-ac5a-2c48b5f93381" />
<img width="616" height="554" alt="image" src="https://github.com/user-attachments/assets/a2364bb8-ae61-46f5-8c58-b4e024cb66bd" />
<img width="521" height="570" alt="image" src="https://github.com/user-attachments/assets/0e469e95-5f07-462f-bcff-38892b2f4270" />
<img width="399" height="569" alt="image" src="https://github.com/user-attachments/assets/cc11e94e-a64c-4e72-8951-204cd1f222d4" />
<img width="389" height="548" alt="image" src="https://github.com/user-attachments/assets/c1743cab-a90c-4c90-bc0d-1a9a90a343d5" />



### RESULT
The required image processing operations were successfully performed using OpenCV, and the output images were displayed correctly for each task.
