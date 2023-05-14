# Opening-and-Closing

## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
# Step 1:
Import the necessary packages.

# Step 2:
Create the Text using cv2.putText.

# Step 3:
Create the structuring element.

# Step 4:
Use Opening operation.

# Step 5:
Use Closing Operation.

# Step 6:
Print the output and end the program.

 
## Program:

``` Python

Developed by : Gayathri A
Register Number : 212221230028
```
# Import the necessary packages
```python
import cv2
import numpy as np
import matplotlib.pyplot as plt
```

# Create the Text using cv2.putText
```python
text_image = np.zeros((100,500),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX = 3
cv2.putText(text_image,"GAYATHRI RAJ",(5,70),font,2,(255),5,cv2.LINE_AA)
plt.title("Original Image")
plt.imshow(text_image,'magma')
plt.axis('off')
```

# Create the structuring element
```
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
```

# Use Opening operation
```python
opening_image = cv2.morphologyEx(text_image,cv2.MORPH_OPEN,kernel)
plt.title("Opening")
plt.imshow(opening_image,'magma')
plt.axis('off')
```


# Use Closing Operation
```python
closing_image = cv2.morphologyEx(text_image,cv2.MORPH_CLOSE,kernel)
plt.title("Closing")
plt.imshow(closing_image,'magma')
plt.axis('off')
```


## Output:

### Display the input Image

![d11 1](https://github.com/Gayathriraj18/Opening-and-Closing/assets/94154854/0e8ac2da-4677-4c5e-9d9e-095e4e031871)

### Display the result of Opening

![d11 2](https://github.com/Gayathriraj18/Opening-and-Closing/assets/94154854/a4ea3e1a-a56b-45b1-ba3a-514f794d0577)


### Display the result of Closing

![d11 3](https://github.com/Gayathriraj18/Opening-and-Closing/assets/94154854/1f7872fc-c883-49ba-a5a8-21e6cbcff478)


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
