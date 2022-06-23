### EX.NO : 07

### DATE : 

# <p align="center"> Edge-Detection </p>
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:

### Step 1:
Import the necessary modules.

### Step2:
Load a image using imread() from cv2 module.

### Step3:
Convert the image to grayscale.

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:
Using Laplacian operator from cv2,detect the edges of the image.

### Step6:
Using Canny operator from cv2,detect the edges of the image.

 
## Program:


## Import the packages
```python 3

import cv2
import matplotlib.pyplot as plt

```
## Load the image, Convert to grayscale and remove noise

```python 3

image = cv2.imread("Panda.jpg")
image1 = cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
cv2.imshow("PRIYA",image1)
cv2.waitKey(0)
cv2.destroyAllWindows()


img = cv2.GaussianBlur(image1,(3,3),0)
plt.figure(1)
plt.imshow(img,cmap="gray")
plt.title('Original')
plt.xticks([])
plt.yticks([])

```


## SOBEL EDGE DETECTOR
```python3

sobelx = cv2.Sobel(img,cv2.CV_64F,1,0,ksize=5)
plt.figure(1)
plt.imshow(sobelx,cmap="gray")
plt.title('Sobel x')
plt.xticks([])
plt.yticks([])
sobely = cv2.Sobel(img,cv2.CV_64F,0,1,ksize=5)
plt.figure(1)
plt.imshow(sobely,cmap="gray")
plt.title('Sobel y')
plt.xticks([])
plt.yticks([])
sobelxy = cv2.Sobel(img,cv2.CV_64F,1,1,ksize=5)
plt.figure(1)
plt.imshow(sobelxy,cmap="gray")
plt.title('Sobel xy')
plt.xticks([])
plt.yticks([])

```
## LAPLACIAN EDGE DETECTOR

```python 3

laplacian=cv2.Laplacian(img,cv2.CV_64F)
plt.imshow(laplacian,cmap="gray")
plt.title('laplacian')
plt.xticks([])
plt.yticks([])

```


## CANNY EDGE DETECTOR

```python 3
canny_edges=cv2.Canny(img,120,150)
plt.imshow(canny_edges,cmap="gray")
plt.title('Canny Edges')
plt.xticks([])
plt.yticks([])

```
## Output:
### SOBEL EDGE DETECTOR
![image](https://user-images.githubusercontent.com/81132849/168251225-bdedffad-109d-4217-b51b-b653865e5be5.png)

![image](https://user-images.githubusercontent.com/81132849/168251316-a402fa87-5a59-46d6-a0ef-c2735b496f7e.png)

![image](https://user-images.githubusercontent.com/81132849/168251364-e0770361-f450-407e-b7de-8d2369edc866.png)



### LAPLACIAN EDGE DETECTOR

![image](https://user-images.githubusercontent.com/81132849/168251437-4ddaf283-86ac-4093-968e-f12904a7bb9f.png)



### CANNY EDGE DETECTOR

![image](https://user-images.githubusercontent.com/81132849/168251510-84ebec03-a51c-405d-9db3-efd8ec8f6b9f.png)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
