# OPENING--AND-CLOSING
# Name : K S Vinay Suhirthan
# Reg. No. : 212224230305
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages

### Step2:
Create the Text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Use Opening operation

### Step5:
Use Closing Operation

## Program:

``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt


# Create the Text using cv2.putText

# Create a blank image
image = np.zeros((500, 500, 3), dtype=np.uint8)
# Add text on the image using cv2.putText
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'ARAVIND', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)

# Create the structuring element
kernel = np.ones((3, 3), np.uint8)
# Display the input image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')

# Use Opening operation
# Opening is erosion followed by dilation
opened_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)
# Display the result of Opening
plt.imshow(cv2.cvtColor(opened_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Opening Operation")
plt.axis('off')



# Use Closing Operation

# Closing is dilation followed by erosion
closed_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)
# Display the result of Opening
plt.imshow(cv2.cvtColor(closed_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Closing Operation")
plt.axis('off')



```
## Output:

### Display the input Image

<img width="389" height="411" alt="image" src="https://github.com/user-attachments/assets/6e38bfb6-a46f-4665-bdae-f388eeb6f83a" />

### Display the result of Opening

<img width="389" height="411" alt="image" src="https://github.com/user-attachments/assets/066aa164-07aa-4e71-a193-ae059ab9c93e" />


### Display the result of Closing

<img width="389" height="411" alt="image" src="https://github.com/user-attachments/assets/d6f4b848-6d43-453f-99bb-0fdd42fb153a" />


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
