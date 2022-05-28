# OPENING AND CLOSING

## AIM:
To implement Opening and Closing using Python and OpenCV.

## SOFTWARE REQUIRED:
1. Anaconda - Python 3.7
2. OpenCV
## ALGORITHM:
### Step 1:
Import the necessary packages.
### Step 2:
Create the Text using cv2.putText
### Step 3:
Create the structuring element.
### Step 4:
Use Opening operation.
### Step 5:
Use Closing Operation.

<br><br><br><br><br>

## PROGRAM:
```
/*
Developed by   : B.Kavya
Register Number: 212220230007
*/
```
``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
img=np.zeros((100,400),dtype='uint8')
font=cv2.FONT_ITALIC
cv2.putText(img,'Kavya',(5,70),font,2,(255),5,cv2.LINE_AA)
plt.axis('off')
plt.imshow(img)
plt.show()

# Create the structuring element
kernel=cv2.getStructuringElement(cv2.MORPH_RECT,(9,9))

# Use Opening operation
image_open=cv2.morphologyEx(img,cv2.MORPH_OPEN,kernel)
plt.axis('off')
plt.imshow(image_open)
plt.show()

# Use Closing Operation
image_close=cv2.morphologyEx(img,cv2.MORPH_CLOSE,kernel)
plt.axis('off')
plt.imshow(image_close)
plt.show()

```
## OUTPUT:

### Display the input Image
![image](https://user-images.githubusercontent.com/75235813/170825049-85618892-2c97-4417-9ec8-89c55a43cb8d.png)

### Display the result of Opening
![image](https://user-images.githubusercontent.com/75235813/170825060-18bfebef-75af-4f74-bf7b-ee575a9db966.png)

### Display the result of Closing
![image](https://user-images.githubusercontent.com/75235813/170825070-4a683084-7a43-4d12-93d2-2f520a294af9.png)

## RESULT:
Thus the Opening and Closing operation is used in the image using python and OpenCV.
