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

### Import the necessary packages
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```

### Create the Text using cv2.putText
```
text_image = np.zeros((100,190),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX = 3
cv2.putText(text_image,"Pooja ",(5,70),font,2,(255),5,cv2.LINE_AA)
plt.title("Created_text")
plt.imshow(text_image,'magma')
plt.axis('off')
```

### Create the structuring element
```
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
```

### Use Opening operation
```
opening_image = cv2.morphologyEx(text_image,cv2.MORPH_OPEN,kernel)
plt.title("Opening")
plt.imshow(opening_image,'magma')
plt.axis('off')
```

### Use Closing Operation
```
closing_image = cv2.morphologyEx(text_image,cv2.MORPH_CLOSE,kernel)
plt.title("Closing")
plt.imshow(closing_image,'magma')
plt.axis('off')
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
