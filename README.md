# COLOR-CONVERSION
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Import cv2 library and upload the image or capture an image

### Step2:
Read the saved image using cv2.imread("filename.jpg")

### Step3:
Convert the image into the given color transformation using cv2.cvtColor(image, cv2.BGR2YCrCb) and similarly for other color formats.

### Step4:
Split and merge the image using cv2.split(hsv) and cv2.merge([h,s,v])

### Step5:

Output the image using cv2.imshow("OUTPUT", image).
## Program:
```python
# Developed By:Lokesh N
# Register Number:212222100023
# i) Convert BGR and RGB to HSV and GRAY
```python
import cv2
houseImage = cv2.imread('car.png')
cv2.imshow('212222100023-lokesh',houseImage)
hsvImage = cv2.cvtColor(houseImage,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsvImage)
hsvImage1=cv2.cvtColor(houseImage,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsvImage1)
grayImage = cv2.cvtColor(houseImage,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',grayImage)
grayImage1 = cv2.cvtColor(houseImage,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',grayImage1)
cv2.waitKey(0)
cv2.destroyAllWindows()

```

# ii)Convert HSV to RGB and BGR

```
import cv2
houseHSVImage = cv2.imread('car.png')
cv2.imshow('212222100023-lokesh',houseHSVImage)
RGBImage = cv2.cvtColor(houseHSVImage,cv2.COLOR_HSV2RGB)
cv2.imshow('BGR2HSV',RGBImage)
BGRImage=cv2.cvtColor(houseHSVImage,cv2.COLOR_HSV2BGR)
cv2.imshow('RGB2HSV',BGRImage)
cv2.waitKey(0)
cv2.destroyAllWindows()
```


# iii)Convert RGB and BGR to YCrCb
```
import cv2
houseImage = cv2.imread('car.png')
cv2.imshow('212222100023-lokesh',houseImage)
YCrCb_image = cv2.cvtColor(houseImage, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR2HSV',YCrCb_image)
YCrCb_image1 = cv2.cvtColor(houseImage, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB2HSV',YCrCb_image1)
cv2.waitKey(0)
cv2.destroyAllWindows()
```



# iv)Split and Merge RGB Image
```
import cv2
image = cv2.imread('car.png')
blue = image[:,:,0]
green = image[:,:,1]
red = image[:,:,2]
cv2.imshow('B-Channel',blue)
cv2.imshow('G-Channel',green)
cv2.imshow('R-Channel',red)
mergeBgr = cv2.merge((blue,green,red))
cv2.imshow('212222100023-lokesh',mergeBgr)
cv2.waitKey(0)
cv2.destroyAllWindows()
```



# v) Split and merge HSV Image
```
import cv2
image = cv2.imread('car.png')
hsv = cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
h,s,v = cv2.split(hsv)
cv2.imshow('Hue - Image',h)
cv2.imshow('Saturation - Image',s)
cv2.imshow('Gray - Image',v)
mergedHSV = cv2.merge((h,s,v))
cv2.imshow('212222100023-lokesh',mergedHSV)
cv2.waitKey(0)
cv2.destroyAllWindow()
```
## Output:
### i) BGR and RGB to HSV and GRAY
![Screenshot from 2023-08-23 14-05-56](https://github.com/lokeshnarayanan/COLOR-CONVERSION/assets/119393019/131fc6a6-383b-40f9-a57d-666f6abc091e)


### ii) HSV to RGB and BGR
![Screenshot from 2023-08-23 14-22-43](https://github.com/lokeshnarayanan/COLOR-CONVERSION/assets/119393019/ec553608-6f2b-4734-9a8a-6e421f5cfd24)




### iii) RGB and BGR to YCrCb

![Screenshot from 2023-08-23 14-27-46](https://github.com/lokeshnarayanan/COLOR-CONVERSION/assets/119393019/6da8a4c3-c59a-4243-997b-7438e6c94e68)



### iv) Split and merge RGB Image
![Screenshot from 2023-08-23 14-34-13](https://github.com/lokeshnarayanan/COLOR-CONVERSION/assets/119393019/76442391-d90e-4dc8-a702-af7d25edd70b)


### v) Split and merge HSV Image
![Screenshot from 2023-08-23 14-41-51](https://github.com/lokeshnarayanan/COLOR-CONVERSION/assets/119393019/46915740-a714-4cf6-ac0e-4e315c334c1b)



## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
