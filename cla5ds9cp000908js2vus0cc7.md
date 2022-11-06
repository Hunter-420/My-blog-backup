# AI |Count Object

Count object is the task of computer vision. There are many kinds of computer vision library are avilable in python to perform this task like OpenCV, Tenserflow,pytorch,cvlib.

But here we are going to use cvlib. If you don't know what is this library & why we are going to use it??

We choose this library because it is the simple,high level & easy to use computer vision library. It was developed with a focus on enabling easy and fast experimentation. Being able to go from an idea to prototype with least amount of delay is key to doing good research.

Guiding principles of cvlib are heavily inspired from Keras (deep learning library).

- simplicity
- user friendliness
- modularity
- extensibility
What other things you can do on cvlib?

1. Face Detection
2. Gender Detection
3. Age Detection
4. Objection Detection
To install this library just enter the command

For command prompt
```
pip install cvlib
```
For google collab

```
!pip install cvlib
```
Make sure that you also install Tenserflow & OpenCV too

for that

```
pip install opencv-python tensorflow
```
Now lets see how to use object count library in python to count object from photo. To do that at first we read image with the help of OpenCV. Then I will detect the object & count that object having same level. To perform this task I will use this image shown below :

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1667739943325/atrvCRPvd.png align="left")

As you can see the image which I taken above is the image of many types vehicle. so at first we detect those vehicle & then count them. So below we see how to count specific vehicle using python. For that let's import the library.

```
!pip install cvlib
```
```
!pip install opencv-python tensorflow
```
Import Library
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
import cvlib as cv
from cvlib.object_detection import draw_bbox
from numpy.lib.polynomial import poly
```
Read image using OpenCV
```
image=cv2.imread("/content/drive/MyDrive/Object Count using cvlib/Vehicles all in one image.jpg")
```
Detect the common object from our image using cvlib
```
box,label,count=cv.detect_common_objects(image)
```
Now we draw a box around the detected object with the labels
```
output=draw_bbox(image,box,label,count)
```
At last we display our output using pyplot
```
plt.imshow(output)
plt.show()
print("The numbers of car in this image : " +str(label.count("car")))
```

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1667740253861/AhSwtjYed.png align="left")
In similar way we can also able to detect the person. For that we again took another image of people dataset

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1667740272826/ftn8f4_ag.png align="left")
```
#set the path of image
image=cv2.imread("/content/drive/MyDrive/Object Count using cvlib/grid people image.jpg")
#detect common objects in image
box,label,count=cv.detect_common_objects(image)
#load image object label & box in output
output=draw_bbox(image,box,label,count)
#display output
plt.imshow(output)
plt.show()
#print the total counted person
print("The numbers of person in image : "+str(label.count("person")))
```

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1667740312447/XiNkBF1Ct.png align="left")
Thank you

[Nischal Khanal | Facebook](https://www.facebook.com/nischal.khanal69/)

[Nischal Khanal | GitHub](https://github.com/Hunter-420/Hunter-420)

[Nischal Khanal | LinkdIn](https://www.linkedin.com/in/nischalkhanal/)
