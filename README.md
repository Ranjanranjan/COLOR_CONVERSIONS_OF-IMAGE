# COLOR_CONVERSIONS_OF-IMAGE
## AIM
Write a Python program using OpenCV that performs the following tasks:

i) Read and Display an Image.

ii) 	Draw Shapes and Add Text.

iii) Image Color Conversion.

iv) Access and Manipulate Image Pixels.

v) Image Resizing

vi) Image Cropping

vii) Image Flipping

viii)	Write and Save the Modified Image


## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Load an image from your local directory and display it.

### Step2:
o	Draw a line from the top-left to the bottom-right of the image.

o	Draw a circle at the center of the image.

o	Draw a rectangle around a specific region of interest in the image.

o	Add the text "OpenCV Drawing" at the top-left corner of the image.

### Step3:
o	Convert the image from RGB to HSV and display it.

o	Convert the image from RGB to GRAY and display it.

o	Convert the image from RGB to YCrCb and display it.

o	Convert the HSV image back to RGB and display it.



### Step4:
o	Access and print the value of the pixel at coordinates (100, 100).

o	Modify the color of the pixel at (200, 200) to white.

### Step5:
o	Resize the original image to half its size and display it.
### Step6:
o	Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.
### Step7:
o	Flip the original image horizontally and display it.
o	Flip the original image vertically and display it.

### Step8:
o	Save the final modified image to your local directory.


##### Program:
### Developed By: Ranjan K
### Register Number: 212222230116


## Output:

### 1. Read and display the image
i.Load an image from your local directory and display it.
```
import cv2
from google.colab.patches import cv2_imshow
image=cv2.imread("/content/uiop.jpg")
cv2_imshow(image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
<img width="974" alt="Screenshot 2024-09-19 at 11 04 57 AM" src="https://github.com/user-attachments/assets/c711e620-f5dc-42a5-a3c4-408f78d9b7f7">


### Draw Shapes and Add Text
(1) Draw a line from the top-left to the bottom-right of the image.
```
import cv2
from google.colab.patches import cv2_imshow
image=cv2.imread("/content/uiop.jpg")
height,width,_=image.shape
diagonal = cv2.line(image, (0, 0), (int(width * 2), int(height * 2)), (255, 0, 0), 5)
cv2_imshow(diagonal)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
<img width="977" alt="Screenshot 2024-09-19 at 11 07 17 AM" src="https://github.com/user-attachments/assets/d06ca417-879f-4dec-97b5-a77edeb6b3d4">


2. Draw a circle at the center of the image.
```
import cv2
from google.colab.patches import cv2_imshow
image=cv2.imread("/content/uiop.jpg")
circle=cv2.circle(image, (700, 500),  350, (0, 255, 0), 5)
cv2_imshow( circle)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
<img width="973" alt="Screenshot 2024-09-19 at 11 09 22 AM" src="https://github.com/user-attachments/assets/300ed1c5-f4a0-4174-9363-58fec7dc0646">



3.Draw a rectangle around a specific region of interest in the image.

```
import cv2
from google.colab.patches import cv2_imshow
image=cv2.imread("/content/uiop.jpg")
rectangle=cv2.rectangle(image, (10,10), (1450,950),(0, 0, 255), 5)
cv2_imshow(rectangle)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
<img width="976" alt="Screenshot 2024-09-19 at 11 10 28 AM" src="https://github.com/user-attachments/assets/441e528c-2b34-474c-9b44-253569a86e02">


4.Add the text "OpenCV Drawing" at the top-left corner of the image.
```
import cv2
image = cv2.imread("/content/uiop.jpg")
text = "OpenCV Drawing"
position = (10, 50)
font = cv2.FONT_HERSHEY_SIMPLEX
font_scale = 1
color = (204, 51, 255)
thickness = 2
res = cv2.putText(image, text, position, font, font_scale, color, thickness, cv2.LINE_AA)
cv2_imshow(image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
<img width="968" alt="Screenshot 2024-09-19 at 11 11 31 AM" src="https://github.com/user-attachments/assets/b66739bf-97da-4054-9b36-5809627cc91f">



### iii)Image Color Conversion
(i)Convert the image from RGB to HSV and display it
```
import cv2
image = cv2.imread('/content/uiop.jpg',1)
cv2_imshow(image)
hsv = cv2.cvtColor(image,cv2.COLOR_RGB2HSV)
cv2_imshow(hsv)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
<img width="969" alt="Screenshot 2024-09-19 at 11 13 14 AM" src="https://github.com/user-attachments/assets/6be93a99-bede-4e46-932a-34ebba8d5962"><img width="973" alt="Screenshot 2024-09-19 at 11 13 30 AM" src="https://github.com/user-attachments/assets/a489413d-0f81-4d19-86d4-9c1883a08039">



(2) Convert the image from RGB to GRAY and display it.
```
import cv2
image = cv2.imread('/content/uiop.jpg',1)
cv2_imshow(image)
gray = cv2.cvtColor(image,cv2.COLOR_RGB2GRAY)
cv2_imshow(gray)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
<img width="964" alt="Screenshot 2024-09-19 at 11 15 38 AM" src="https://github.com/user-attachments/assets/f5f1433f-a2e6-475a-bcc5-12925c670138"><img width="944" alt="Screenshot 2024-09-19 at 11 15 54 AM" src="https://github.com/user-attachments/assets/cd067163-b5f3-46dd-88e9-8053b4143fec">




(3) Convert the image from RGB to YCrCb and display it.

```
import cv2
image = cv2.imread('/content/uiop.jpg',1)

cv2_imshow(image)
YCrCb = cv2.cvtColor(image, cv2.COLOR_BGR2YCrCb)
cv2_imshow(YCrCb)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
<img width="970" alt="Screenshot 2024-09-19 at 11 16 40 AM" src="https://github.com/user-attachments/assets/cd428211-aa17-4b05-b835-fa92975bb79b"><img width="971" alt="Screenshot 2024-09-19 at 11 17 03 AM" src="https://github.com/user-attachments/assets/7b0da274-c183-49d3-9c40-5905277391e2">



(4) Convert the HSV image back to RGB and display it.

```
import cv2
image = cv2.imread('/content/uiop.jpg',1)
cv2_imshow(image)
RGB = cv2.cvtColor(image,cv2.COLOR_HSV2BGR)
cv2_imshow(RGB)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
<img width="952" alt="Screenshot 2024-09-19 at 11 18 06 AM" src="https://github.com/user-attachments/assets/6b576d33-8ff2-488a-a256-3a5b3bd3572f"><img width="972" alt="Screenshot 2024-09-19 at 11 18 25 AM" src="https://github.com/user-attachments/assets/a0050fa7-4571-4e7c-968f-0ec940275205">



### iv)Access and Manipulate Image Pixels
(1) Access and print the value of the pixel at coordinates (100, 100)
```
import cv2
image = cv2.imread('/content/uiop.jpg',1)
pixel_value = image[100, 100]
print(f"Pixel value at (100, 100): {pixel_value}")
```

<img width="263" alt="Screenshot 2024-09-19 at 12 16 05 PM" src="https://github.com/user-attachments/assets/eea25d7b-8ed7-4069-b88c-b296764c6391">




(2) Modify the color of the pixel at (200, 200) to white
```
import cv2
image = cv2.imread('/content/uiop.jpg',1)
image = cv2.resize(image,(400,300))
cv2_imshow(image)
image[200, 200] = [255, 255, 255] 
cv2_imshow( image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

<img width="262" alt="Screenshot 2024-09-19 at 11 34 15 AM" src="https://github.com/user-attachments/assets/9c0ae95b-92d7-4eb2-88d5-cc8dc37337fe">


### v)Image Resizing:
Resize the original image to half its size and display it.
```
import cv2
image = cv2.imread('/content/uiop.jpg', 1)
cv2_imshow(image)
cv2_imshow(cv2.resize(image, (image.shape[1] // 2, image.shape[0] // 2)))
cv2.waitKey(0)
cv2.destroyAllWindows()
```
<img width="971" alt="Screenshot 2024-09-19 at 12 19 10 PM" src="https://github.com/user-attachments/assets/72b59aaf-3bd8-4b24-87bd-adf3afd454c7">

<img width="479" alt="Screenshot 2024-09-19 at 12 19 27 PM" src="https://github.com/user-attachments/assets/7a1fa852-8a84-4813-8f0f-9083a3cde697">



### vi)Image Cropping
Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.
```
import cv2
image = cv2.imread('/content/uiop.jpg',1)

image = cv2.resize(image,(400,300))
x, y = 50, 50
width, height = 100, 100
roi = image[y:y + height, x:x + width]
cv2_imshow(roi)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
<img width="68" alt="Screenshot 2024-09-19 at 12 20 22 PM" src="https://github.com/user-attachments/assets/f07a4430-bc6f-44ac-91fb-5cff2b3fc0ee">



### vii)Image Flipping:
(1) Flip the original image horizontally and display it.
```
import cv2
image = cv2.imread("/content/uiop.jpg")
image = cv2.resize(image,(300,200))
flip=cv2.rotate(image,cv2.ROTATE_180)
cv2_imshow(image)
cv2_imshow(flip)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
<img width="198" alt="Screenshot 2024-09-19 at 12 20 55 PM" src="https://github.com/user-attachments/assets/ab6aee42-b3bd-4047-a75b-82db65de2bd7">




(2) Flip the original image vertically and display it.
```
import cv2
image = cv2.imread("/content/uiop.jpg")
image = cv2.resize(image,(300,200))
res=cv2.rotate(image,cv2.ROTATE_90_CLOCKWISE)
cv2_imshow(image)
cv2_imshow(res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

<img width="196" alt="Screenshot 2024-09-19 at 12 21 45 PM" src="https://github.com/user-attachments/assets/ea8849f9-1213-46db-9c25-2ca16a1fe661"><img width="130" alt="Screenshot 2024-09-19 at 12 21 59 PM" src="https://github.com/user-attachments/assets/cfedf925-3b11-45e1-a665-4f16c64fee6c">




### viii)Write and Save the Modified Image
Save the final modified image to your local directory.

```
import cv2
img = cv2.imread("/content/uiop.jpg")
img = cv2.resize(img,(300,200))
cv2.imwrite('nature_pic.jpg',img)
```
<img width="89" alt="Screenshot 2024-09-19 at 12 22 40 PM" src="https://github.com/user-attachments/assets/4800979c-4b56-4aff-a528-573934dfc647">




## Result:
Thus the images are read, displayed, and written ,and color conversion was performed  successfully using the python program.







