# COLOR_CONVERSIONS_OF-IMAGE
## AIM
To write a python program using OpenCV to do the following image manipulations.

i) Read, display, and write an image.

ii) Access the rows and columns in an image.

iii) Cut and paste a small portion of the image.

iv)To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.


## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Choose an image and save it as a filename.jpg ,
### Step2:
Use imread(filename, flags) to read the file.
### Step3:
Use imshow(window_name, image) to display the image.
### Step4:
Use imwrite(filename, image) to write the image.
### Step5:
End the program and close the output image windows.
### Step6:
Convert BGR and RGB to HSV and GRAY
### Step7:
Convert HSV to RGB and BGR
### Step8:
Convert RGB and BGR to YCrCb
### Step9:
Split and Merge RGB Image
### Step10:
Split and merge HSV Image

##### Program:
### Developed By: Ranjan K
### Register Number: 212222230016


## Output:

### i) Read and display the image

```Python
import cv2
from google.colab.patches import cv2_imshow
image=cv2.imread("/content/uiop.jpg")
cv2_imshow(image)
cv2.waitKey(0)
cv2.destroyAllWindows()
    
```
<img width="645" alt="Screenshot 2024-09-28 at 10 50 33 AM" src="https://github.com/user-attachments/assets/470f86e7-32e5-43d9-9c98-9c8f93c4a023">




### ii)Draw shapes and add text
#### Line
```Python

import cv2
from google.colab.patches import cv2_imshow
image=cv2.imread("/content/uiop.jpg")
height,width,_=image.shape
diagonal = cv2.line(image, (0, 0), (int(width * 2), int(height * 2)), (255,
0, 0), 5)
cv2_imshow(diagonal)
cv2.waitKey(0)
cv2.destroyAllWindows()

```

<img width="643" alt="Screenshot 2024-09-28 at 10 51 14 AM" src="https://github.com/user-attachments/assets/1904e444-38f4-4f72-b97d-88c1b295bac2">


#### Circle
```Python
import cv2
from google.colab.patches import cv2_imshow
image=cv2.imread("/content/uiop.jpg")
circle=cv2.circle(image, (700, 500), 350, (0, 255, 0), 5)
cv2_imshow( circle)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
<img width="641" alt="Screenshot 2024-09-28 at 10 51 45 AM" src="https://github.com/user-attachments/assets/00f7d034-d3c3-4499-9571-4cdd7323251c">


#### Rectangle
```Python
import cv2
from google.colab.patches import cv2_imshow
image=cv2.imread("/content/uiop.jpg")
rectangle=cv2.rectangle(image, (10,10), (1450,950),(0, 0, 255), 5)
cv2_imshow(rectangle)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
<img width="649" alt="Screenshot 2024-09-28 at 10 52 31 AM" src="https://github.com/user-attachments/assets/9662bc3b-21e7-47fc-9a73-3c2c596af728">


#### Add the text "OpenCV Drawing" at the top-left corner of the image.
```Python
import cv2
image = cv2.imread("/content/uiop.jpg")
text = "OpenCV Drawing"
position = (10, 50)
font = cv2.FONT_HERSHEY_SIMPLEX
font_scale = 1
color = (204, 51, 255)
thickness = 2
res = cv2.putText(image, text, position, font, font_scale, color,
thickness, cv2.LINE_AA)
cv2_imshow(image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
<img width="645" alt="Screenshot 2024-09-28 at 10 53 20 AM" src="https://github.com/user-attachments/assets/6707c46a-b751-4054-aecf-9e0bdca6903b">



### iii) Image color conversion

#### BGR and RGB to HSV and GRAY
```Python
import cv2
image = cv2.imread('/content/uiop.jpg',1)
cv2_imshow(image)
hsv = cv2.cvtColor(image,cv2.COLOR_RGB2HSV)
cv2_imshow(hsv)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
<img width="640" alt="Screenshot 2024-09-28 at 10 54 53 AM" src="https://github.com/user-attachments/assets/7000e9be-ac78-4060-8a43-5de4a60bdb4a"><img width="646" alt="Screenshot 2024-09-28 at 10 55 10 AM" src="https://github.com/user-attachments/assets/e1b07267-86b5-4cb9-ac5e-e54d44ca7956">



```Python
import cv2
image = cv2.imread('/content/uiop.jpg',1)
cv2_imshow(image)
gray = cv2.cvtColor(image,cv2.COLOR_RGB2GRAY)
cv2_imshow(gray)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
<img width="645" alt="Screenshot 2024-09-28 at 10 55 47 AM" src="https://github.com/user-attachments/assets/7e2bdfaa-1bbc-4e2b-bf93-c822bbc183bc">
<img width="646" alt="Screenshot 2024-09-28 at 10 56 07 AM" src="https://github.com/user-attachments/assets/109b3fbb-3514-488f-a082-bc98c87e716c">







#### RGB and BGR to YCrCb
```Python
import cv2
image = cv2.imread('/content/uiop.jpg',1)
cv2_imshow(image)
YCrCb = cv2.cvtColor(image, cv2.COLOR_BGR2YCrCb)
cv2_imshow(YCrCb)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
<img width="643" alt="Screenshot 2024-09-28 at 10 59 14 AM" src="https://github.com/user-attachments/assets/a134d51b-e8e9-4b94-93ff-8a68b51f1f4a">
<img width="640" alt="Screenshot 2024-09-28 at 10 59 26 AM" src="https://github.com/user-attachments/assets/7d655ec5-6862-4d30-bcb2-b41273b6d465">






#### (4) Convert the HSV image back to RGB and display it.
```Python
import cv2
image = cv2.imread('/content/uiop.jpg',1)
cv2_imshow(image)
RGB = cv2.cvtColor(image,cv2.COLOR_HSV2BGR)
cv2_imshow(RGB)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
<img width="641" alt="Screenshot 2024-09-28 at 11 01 11 AM" src="https://github.com/user-attachments/assets/fd65af9b-e4f9-480b-8259-5e9b21ace128">
<img width="646" alt="Screenshot 2024-09-28 at 11 01 29 AM" src="https://github.com/user-attachments/assets/45f6db18-6e4a-4a16-beb3-7aad031619b4">






### iv) Access and Manipulate Image Pixels
#### (1) Access and print the value of the pixel at coordinates (100, 100)
```Python
import cv2
image = cv2.imread('/content/uiop.jpg',1)
pixel_value = image[100, 100]
print(f"Pixel value at (100, 100): {pixel_value}")
```
<img width="257" alt="Screenshot 2024-09-28 at 11 02 29 AM" src="https://github.com/user-attachments/assets/0a19d8a9-f2b2-45e3-95bb-3a14f8d474db">


#### (2) Modify the color of the pixel at (200, 200) to white
```Python
import cv2
image = cv2.imread('/content/uiop.jpg',1)
image = cv2.resize(image,(400,300))
cv2_imshow(image)
image[200, 200] = [255, 255, 255]
cv2_imshow( image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
<img width="259" alt="Screenshot 2024-09-28 at 11 03 13 AM" src="https://github.com/user-attachments/assets/918eec96-15ed-4192-aba2-882c3a38c17c">


### v) Image Resizing
```Python
import cv2
image = cv2.imread('/content/uiop.jpg', 1)
cv2_imshow(image)
cv2_imshow(cv2.resize(image, (image.shape[1] // 2, image.shape[0] // 2)))
cv2.waitKey(0)
cv2.destroyAllWindows()
```
<img width="639" alt="Screenshot 2024-09-28 at 11 03 49 AM" src="https://github.com/user-attachments/assets/d0a1bf29-50f6-4ebc-95f6-776b3d092090">
<img width="470" alt="Screenshot 2024-09-28 at 11 04 22 AM" src="https://github.com/user-attachments/assets/e1d5d1e8-6470-4edd-bae6-e2ed0b092135">


### vi) Image Cropping
```Python
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
<img width="67" alt="Screenshot 2024-09-28 at 11 04 58 AM" src="https://github.com/user-attachments/assets/2c4485c4-0d98-4a72-aaad-d760aa1f19a8">


 ### vii) Image Flipping
 #### (1) Flip the original image horizontally and display it
```Python
import cv2
image = cv2.imread("/content/uiop.jpg")
image = cv2.resize(image,(300,200))
flip=cv2.rotate(image,cv2.ROTATE_180)
cv2_imshow(image)
cv2_imshow(flip)
cv2.waitKey(0)
cv2.destroyAllWindows()
`
```
<img width="194" alt="Screenshot 2024-09-28 at 11 05 30 AM" src="https://github.com/user-attachments/assets/73ba59d5-7f26-41a3-95f8-975c3e6b8cb5">


#### (2) Flip the original image vertically and display it
```Python
import cv2
image = cv2.imread("/content/uiop.jpg")
image = cv2.resize(image,(300,200))
res=cv2.rotate(image,cv2.ROTATE_90_CLOCKWISE)
cv2_imshow(image)
cv2_imshow(res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
<img width="194" alt="Screenshot 2024-09-28 at 11 06 37 AM" src="https://github.com/user-attachments/assets/4cae7797-78bd-4a1c-9ecf-307172865db5">
<img width="131" alt="Screenshot 2024-09-28 at 11 06 54 AM" src="https://github.com/user-attachments/assets/7d87b5ad-6023-42a1-a2e3-e0474a339785">


### viii)Write and Save the Modified Image
```Python
import cv2
img = cv2.imread("/content/uiop.jpg")
img = cv2.resize(img,(300,200))
cv2.imwrite('nature_pic.jpg',img)
```
<img width="88" alt="Screenshot 2024-09-28 at 11 07 33 AM" src="https://github.com/user-attachments/assets/36e0454c-3d96-48cf-8406-c4cf957adb4f">







## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







