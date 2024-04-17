# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
- Step1: Import the necessary packages
- Step2: Insert the text using cv2.putText()
- Step3: The perform the erosion for given text and display the text using imshow()
- Step4: Next,perform dilation for inout text and display the result
## Program:
```
DEVELOPED BY: DINESH KUMAR R
REGISTER NUMBER: 212222110010
```
### Import the necessary packages
```python
import cv2
import numpy as np 
import matplotlib.pyplot as plt
```
### Create the Text using cv2.putText
```python
img1=np.zeros((100,400),dtype='uint8')
font=cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img1,'Dinesh',(5,70),font,2,(255),5,cv2.LINE_AA)
```
### Create the structuring element
```python
kernel=np.ones((5,5),np.uint8)
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
```
### Erode the image
```python
image_erode1=cv2.erode(img1,kernel1)
plt.imshow(image_erode1)
plt.axis("off")
```
### Dilate the image
```python
image_dilate1=cv2.dilate(img1,kernel1)
plt.imshow(image_dilate1)
plt.axis("off")
```
## Output:
### Display the input Image

![Screenshot 2024-04-17 085015](https://github.com/DINESH18032004/erosion-dilation/assets/119477784/e3a0e70f-dc04-441a-9c4d-44828721e0a4)


### Display the Eroded Image

![Screenshot 2024-04-17 085027](https://github.com/DINESH18032004/erosion-dilation/assets/119477784/4e6afba0-c351-4793-baa1-05f815c3ab5c)


### Display the Dilated Image

![Screenshot 2024-04-17 085103](https://github.com/DINESH18032004/erosion-dilation/assets/119477784/378152ef-dcab-405c-8c90-689b5f1f0d43)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
