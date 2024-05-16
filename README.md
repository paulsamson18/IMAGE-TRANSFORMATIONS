# IMAGE TRANSFORMATION

## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the required packages.

### Step2:
Load the image file in the program.

### Step3:
Use the techniques for Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

### Step4
Display the modified image output.

### Step5:
End the program.



## Program:

Developed By: Paul samson.S

Register Number: 212222230104

i)Image Translation
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("cat.jpg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(in_img)
plt.show()
```
ii) Image Scaling
```import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("cat.jpg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
M=np.float32([[1,0,50],
              [0,1,50],
              [0,0,1]])
trans_img=cv2.warpPerspective(in_img, M, (cols,rows))
plt.axis('off')
plt.imshow(trans_img)
plt.show() 
```
iii)Image shearing
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("cat.jpg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
M_x=np.float32([[1,0.5,0],
                [0,1 ,0],
                [0,0 ,1]])
M_y=np.float32([[1,  0,0],
                [0.5,1,0],
                [0,  0,1]])
sheared_img_x=cv2.warpPerspective(in_img,M_x,(int(cols),int(rows)))
sheared_img_y=cv2.warpPerspective(in_img,M_y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(sheared_img_x)
plt.show()
plt.axis('off')
plt.imshow(sheared_img_y)
plt.show()
```
iv)Image Reflection
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("cat.jpg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
M_x=np.float32([[1,  0,0  ],
                [0,-1,rows],
                [0,0,1  ]])
M_y=np.float32([[-1,0,cols],
                [ 0,1,0  ],
                [ 0,0,1  ]])
reflect_x=cv2.warpPerspective(in_img,M_x,(int(cols),int(rows)))
reflect_y=cv2.warpPerspective(in_img,M_y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(reflect_x)
plt.show()
plt.axis('off')
plt.imshow(reflect_y)
plt.show()  
```
v)Image Rotation
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("cat.jpg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
angle=np.radians(10)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],
              [np.sin(angle),np.cos(angle),0],
              [0,0,1]])
rotated_img=cv2.warpPerspective(in_img,M,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(rotated_img)
plt.show()  
```
vi)Image Cropping
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img = cv2.imread("cat.jpg")
in_img = cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
plt.imshow(in_img)
plt.show()
cropped_img=in_img[10:150 ,10:250]
plt.imshow(cropped_img)
plt.show()
```
## Output:
### i)Image Translation

![image](https://github.com/Afsarjumail/IMAGE-TRANSFORMATIONS/assets/118343395/424b06d9-2f0f-4023-9a47-42683e6f5c86)


### ii) Image Scaling

![image](https://github.com/Afsarjumail/IMAGE-TRANSFORMATIONS/assets/118343395/80f09bd4-95fb-4a3a-8434-2e8879366aba)



### iii)Image shearing

![image](https://github.com/Afsarjumail/IMAGE-TRANSFORMATIONS/assets/118343395/2be5c5e0-c70b-46f9-bc93-4b3988c511e3)
![image](https://github.com/Afsarjumail/IMAGE-TRANSFORMATIONS/assets/118343395/e699c5b9-4e37-4c64-b674-a30c999f9943)

### iv)Image Reflection
![image](https://github.com/Afsarjumail/IMAGE-TRANSFORMATIONS/assets/118343395/abf8d0e7-6ad1-4eca-b373-c75d8871e28a)
![image](https://github.com/Afsarjumail/IMAGE-TRANSFORMATIONS/assets/118343395/af5d1d9f-8265-4a5e-8bc6-b56c8d45b1ba)






### v)Image Rotation

![image](https://github.com/Afsarjumail/IMAGE-TRANSFORMATIONS/assets/118343395/213d8d51-bb62-4b5f-a202-a7c0e2f425c7)


### vi)Image Cropping

Original
![image](https://github.com/Afsarjumail/IMAGE-TRANSFORMATIONS/assets/118343395/dba01bb3-3c89-4121-a238-1dc5d674a091)
Cropped

## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
