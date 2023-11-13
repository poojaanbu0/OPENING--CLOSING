# Exp11-Record-Implementation of Opening and Closing
## AIM:
To implement Opening and Closing using Python and OpenCV.

## SOFTWARE REQUIRED:
Anaconda - Python 3.7
OpenCV

## ALGORITHM:
### Step 1:
Import the necessary packages.

### Step 2:
Create the Text using cv2.putText.

### Step 3:
Create the structuring element.

### Step 4:
Use Opening operation.

### Step 5:
Use Closing Operation.

### Step 6:
Print the output and end the program.

## PROGRAM:
```
Developed by : Pooja A
Register number : 212222240072
```
```python
# Import the necessary packages
import cv2
import numpy as np


# Create the Text using cv2.putText
img= np.zeros((350,1400),dtype ='uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img,'POOJA A',(15,200),font,5,(255),10,cv2.LINE_AA)
cv2.imshow('created_text',img)
cv2.waitKey(0)
cv2.destroyAllWindows()


# Create the structuring element
struct_ele= np.ones((9,9),np.uint8)


# Use Opening operation
opening = cv2.morphologyEx(img,cv2.MORPH_OPEN,struct_ele)
cv2.imshow('Opening',opening)
cv2.waitKey(0)
cv2.destroyAllWindows()


# Use Closing Operation
closing = cv2.morphologyEx(img,cv2.MORPH_CLOSE,struct_ele)
cv2.imshow('Closing',closing)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## OUTPUT:
### Input Image
![exp 11 created](https://github.com/poojaanbu0/OPENING--CLOSING/assets/119390329/36f735de-849a-4867-a2cc-86177459cfc5)

### Result of Opening
![exp 11 open](https://github.com/poojaanbu0/OPENING--CLOSING/assets/119390329/01b016c0-1072-4251-a899-756b5fd7e3ab)

### Result of Closing
![exp 11 close](https://github.com/poojaanbu0/OPENING--CLOSING/assets/119390329/3b4a80c0-e783-449e-abf2-66540c2d09f1)

## RESULT:
Thus, the Opening and Closing operation is used in the image using python and OpenCV.
