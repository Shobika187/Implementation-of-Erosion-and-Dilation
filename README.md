# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
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
Erode and Dilate the image.

### Step5:
End the Program.

 
## Program:

``` 
Developed by :Shobika P
Register No:212221230096
```
## Import the necessary packages
```
import cv2
import  numpy as np
import matplotlib.pyplot as  plt


```

## Create the Text using cv2.putText
```
img=np.zeros((100,300),dtype='uint8')
img1=cv2.cvtColor(img,cv2.COLOR_BGR2RGB)
font = cv2.FONT_HERSHEY_TRIPLEX
cv2.putText(img1,'SHOBIKA',(0,70),font,2,((238,130,238)),5,cv2.LINE_AA)
cv2.imshow('MyName',img1)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Create the structuring element
```
kernel=np.ones((5,5),np.uint8)
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
```
## Erode the image
```

img_erode1=cv2.erode(img1,kernel1)
cv2.imshow('MyName',img_erode1)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Dilate the image
```
img_dilate1=cv2.dilate(img1,kernel1)
cv2.imshow('MyName',img_dilate1)
cv2.waitKey(0)
cv2.destroyAllWindows()



```
## Output:

### Display the input Image
![out](/10.1.png)

### Display the Eroded Image
![out](/10.2.png)

### Display the Dilated Image
![out](/10.3.png)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.