# OPENING--CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.

### Step2:
Create the Text using cv2.putText.

### Step3:
Create the structuring element.

### Step4:
Use Opening operation.

### Step5:
Use Closing Operation.
 
## Program:
```
DEVELOPED BY: YAMUNAASRI T S
REGISTER NO: 212222240117
```
### Import the necessary packages
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
### Create the Text using cv2.putText
```
img = np.zeros((100, 550), dtype = 'uint8')
font = cv2.FONT_ITALIC
cv2.putText(img, 'YAMUNAAARI T S', (5,70), font, 2, (255), 5, cv2.LINE_AA)
n_img = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
plt.imshow(n_img)
plt.axis("off")
```
### Create the structuring element
```
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS, (11,11))
```
### Use Opening operation
```
image_open = cv2.morphologyEx(n_img, cv2.MORPH_OPEN, kernel)
plt.imshow(image_open)
plt.axis("off")
```
### Use Closing Operation
```
image_close = cv2.morphologyEx(n_img, cv2.MORPH_CLOSE, kernel)
plt.imshow(image_close)
plt.axis("off")
```
## Output:

### Display the input Image
![Screenshot 2023-10-25 161321](https://github.com/Yamunaasri/OPENING--CLOSING/assets/115707860/23bc0d8f-0185-4082-8cc8-4c06172c27bc)


### Display the result of Opening
![Screenshot 2023-10-25 161337](https://github.com/Yamunaasri/OPENING--CLOSING/assets/115707860/f6e7ba68-cb20-4623-9b93-289aa8e05f06)

### Display the result of Closing
![Screenshot 2023-10-25 161342](https://github.com/Yamunaasri/OPENING--CLOSING/assets/115707860/e989f86c-b43e-4bf3-bc30-848be3f0f85c)


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
