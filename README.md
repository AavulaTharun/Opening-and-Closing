# Opening-and-Closing

## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
Step 1:
Import the necessary packages.

Step 2:
Create the Text using cv2.putText.

Step 3:
Create the structuring element.

Step 4:
Use Opening operation.

Step 5:
Use Closing Operation.

Step 6:
Print the output and end the program.

 
## Program:

``` 
# Import the necessary packages

import numpy as np
import matplotlib.pyplot as plt
import cv2

# Create the Text using cv2.putText

text_image = np.zeros((100,440),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX = 3
cv2.putText(text_image," Tharun",(5,70),font,2,(255),5,cv2.LINE_AA)
plt.title("Original Image")
plt.imshow(text_image)
plt.axis('off')

# Create the structuring element

kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(11,11))

# Use Opening operation

opening_image = cv2.morphologyEx(text_image,cv2.MORPH_OPEN,kernel)
plt.title("Opening")
plt.imshow(opening_image)
plt.axis('off')

# Use Closing Operation

closing_image = cv2.morphologyEx(text_image,cv2.MORPH_CLOSE,kernel)
plt.title("Closing")
plt.imshow(closing_image)
plt.axis('off')

```
## Output:

### Display the input Image

![ex-11 1](https://user-images.githubusercontent.com/93427201/172906930-6ac628b2-268a-4da0-a549-fc8e870e28cf.png)

### Display the result of Opening

![ex-11 2](https://user-images.githubusercontent.com/93427201/172906949-27c7d026-1905-49ef-a4a0-3d1c581d912e.png)

### Display the result of Closing
![ex-11 3](https://user-images.githubusercontent.com/93427201/172906975-72fbfc50-bc74-4879-be1c-90e507bdbeb6.png)


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
