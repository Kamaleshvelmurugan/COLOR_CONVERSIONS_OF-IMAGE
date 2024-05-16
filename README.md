# COLOR_CONVERSIONS_OF-IMAGE
## AIM
To write a python program using OpenCV to do the following image manipulations.

i) Read, display, and write an image.

ii) Access the rows and columns in an image.

iii) Cut and paste a small portion of the image.

iv)To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.


## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Choose an image and save it as a filename.jpg ,
### Step2:
Use imread(filename, flags) to read the file.
### Step3:
Use imshow(window_name, image) to display the image.
### Step4:
Use imwrite(filename, image) to write the image.
### Step5:
End the program and close the output image windows.
### Step6:
Convert BGR and RGB to HSV and GRAY
### Step7:
Convert HSV to RGB and BGR
### Step8:
Convert RGB and BGR to YCrCb
### Step9:
Split and Merge RGB Image
### Step10:
Split and merge HSV Image

##### Program:
### Developed By:
### Register Number: 


## Output:

### i) Read and display the image
```
import cv2
img = cv2.imread('Ragul.png', 1)
cv2.imshow('Image',img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

![image](https://github.com/RagulRM/COLOR_CONVERSIONS_OF-IMAGE/assets/121609342/e489320c-c867-4d0f-a575-f9f783f9dcc0)



![WhatsApp Image 2024-05-16 at 23 50 27_5134d26c](https://github.com/Kamaleshvelmurugan/COLOR_CONVERSIONS_OF-IMAGE/assets/119477328/66ab929f-bdb5-499e-957a-cf3abf540ef5)



### ii)Write the image
```
img=cv2.imread('Ragul.png',0)
cv2.imwrite('demos.png',img)
```
![image](https://github.com/RagulRM/COLOR_CONVERSIONS_OF-IMAGE/assets/121609342/3cedbec4-683c-48c5-b18f-ce7b842adfad)


### iii)Shape of the Image
```
image=cv2.imread('Ragul.png',1)
print(image.shape)
```

![image](https://github.com/RagulRM/COLOR_CONVERSIONS_OF-IMAGE/assets/121609342/78386427-e5a7-4e41-8868-4ea1f943e840)

### iv)Access rows and columns
```
import random
image=cv2.imread('Ragul.png',1)
for i in range (150,250):
    for j in range(image.shape[1]):
        image[i][j]=[random.randint(0,255),
                     random.randint(0,255),
                     random.randint(0,255)] 
cv2.imshow('part image',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

![image](https://github.com/RagulRM/COLOR_CONVERSIONS_OF-IMAGE/assets/121609342/37df1b38-af23-4486-8836-1a6344c3b6ca)

![WhatsApp Image 2024-05-17 at 00 03 32_5e2b727e](https://github.com/Kamaleshvelmurugan/COLOR_CONVERSIONS_OF-IMAGE/assets/119477328/23222411-812a-49a0-baec-0254194947a4)


### v)Cut and paste portion of image
```
image=cv2.imread('Ragul.png',1) 
image=cv2.resize(image,(300,300)) 
tag =image[150:200,110:160] 
image[110:160,150:200] = tag 
cv2.imshow('image1',image) 
cv2.waitKey(0) 
cv2.destroyAllWindows()
```

![image](https://github.com/RagulRM/COLOR_CONVERSIONS_OF-IMAGE/assets/121609342/934f9e37-20bb-47eb-8310-f7a39311883d)

<br>

![WhatsApp Image 2024-05-17 at 00 03 56_21a782fc](https://github.com/Kamaleshvelmurugan/COLOR_CONVERSIONS_OF-IMAGE/assets/119477328/3e87635a-a0f4-4604-b882-cbd89cd32aa0)




### vi) BGR and RGB to HSV and GRAY
```
img = cv2.imread('Ragul.png',1) 
img = cv2.resize(img,(300,300))
cv2.imshow('Original Image',img)
hsv1 = cv2.cvtColor(img,cv2.COLOR_BGR2HSV) 
cv2.imshow('BGR2HSV',hsv1)
hsv2 = cv2.cvtColor(img,cv2.COLOR_RGB2HSV) 
cv2.imshow('RGB2HSV',hsv2)
gray1 = cv2.cvtColor(img,cv2.COLOR_BGR2GRAY) 
cv2.imshow('BGR2GRAY',gray1)
gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY) 
cv2.imshow('RGB2GRAY',gray2)
cv2.waitKey(0) 
cv2.destroyAllWindows()
```
<br>

![image](https://github.com/RagulRM/COLOR_CONVERSIONS_OF-IMAGE/assets/121609342/772766e5-f926-4336-bf35-a97439c77bae)


<br>

![WhatsApp Image 2024-05-16 at 23 59 40_6bc6db6d](https://github.com/Kamaleshvelmurugan/COLOR_CONVERSIONS_OF-IMAGE/assets/119477328/cd668a1f-83ed-42ab-9475-220b2f9b783e)



### vii) HSV to RGB and BGR
```
img = cv2.imread('Ragul.png') 
img = cv2.cvtColor(img,cv2.COLOR_BGR2HSV) 
cv2.imshow('Original HSV Image',img)
RGB = cv2.cvtColor(img,cv2.COLOR_HSV2RGB) 
cv2.imshow('2HSV2BGR',RGB)
BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR) 
cv2.imshow('HSV2RGB',BGR)
cv2.waitKey(0) 
cv2.destroyAllWindows()
```

![image](https://github.com/RagulRM/COLOR_CONVERSIONS_OF-IMAGE/assets/121609342/be6a0c69-9406-4d59-87fe-7ba5b3afa453)


![WhatsApp Image 2024-05-17 at 00 00 32_292b6a78](https://github.com/Kamaleshvelmurugan/COLOR_CONVERSIONS_OF-IMAGE/assets/119477328/52ef96ec-f0b6-4233-ac2e-e7dd3552d510)



### viii) RGB and BGR to YCrCb
```
img = cv2.imread('Ragul.png') 
cv2.imshow('Original RGB Image',img)
YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb) 
cv2.imshow('RGB-2-YCrCb',YCrCb1)
YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb) 
cv2.imshow('BGR-2-YCrCb',YCrCb2)
cv2.waitKey(0) 
cv2.destroyAllWindows()
```

![image](https://github.com/RagulRM/COLOR_CONVERSIONS_OF-IMAGE/assets/121609342/efa1d3c9-37ae-4af8-acb0-1f251ebb2c90)

![WhatsApp Image 2024-05-17 at 00 01 07_cc48a08e](https://github.com/Kamaleshvelmurugan/COLOR_CONVERSIONS_OF-IMAGE/assets/119477328/ca536f77-c372-45f4-a71c-2aceddd2e2cf)


### ix) Split and merge RGB Image
```
img = cv2.imread('Ragul.png',1) 
R = img[:,:,2] 
G = img[:,:,1] 
B = img[:,:,0]
cv2.imshow('R-Channel',R) 
cv2.imshow('G-Channel',G) 
cv2.imshow('B-Channel',B)
merged = cv2.merge((B,G,R)) 
cv2.imshow('Merged RGB image',merged)
cv2.waitKey(0) 
cv2.destroyAllWindows()
```

![image](https://github.com/RagulRM/COLOR_CONVERSIONS_OF-IMAGE/assets/121609342/9ddeaa61-cb23-49b8-9504-54a4da7dbec5)

![WhatsApp Image 2024-05-17 at 00 01 48_4a9aaac1](https://github.com/Kamaleshvelmurugan/COLOR_CONVERSIONS_OF-IMAGE/assets/119477328/8b22c658-596d-4d36-b3f2-8689d1c4fdb6)



### x) Split and merge HSV Image
```
img = cv2.imread("Ragul.png",1) 
img = cv2.resize(img,(300,300)) 
img=cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
H,S,V=cv2.split(img)
cv2.imshow('Hue',H) 
cv2.imshow('Saturation',S) 
cv2.imshow('Value',V)
merged = cv2.merge((H,S,V)) 
cv2.imshow('Merged',merged)
cv2.waitKey(0) 
cv2.destroyAllWindows()
```
![image](https://github.com/RagulRM/COLOR_CONVERSIONS_OF-IMAGE/assets/121609342/c37a0051-de81-4b09-83ef-7b34b74ba200)

![WhatsApp Image 2024-05-17 at 00 02 17_d8f2ca44](https://github.com/Kamaleshvelmurugan/COLOR_CONVERSIONS_OF-IMAGE/assets/119477328/d22aebcb-5454-4e6a-ae59-fdb328182c2d)




## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







