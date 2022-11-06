# Clone from Git in Colab & upload on Drive

Today, I was doing a smile face detection project in google colab where I needed to clone the "haarcascade_frontalface_default.xml" file at that time my problem was that I should first need to clone that repo on the local machine and then again uploaded it into my google drive because only google drive files are accessible in Colab. So, that takes a lot of time to complete that job. To get out of that problem I searched on google to look there is any method available on python where we can directly clone the GitHub repo to google drive without downloading it on my local machine then I got a blog where I found the easy & quick method which is very faster if you use GPU instead of CPU it will become faster.


So,
If you are working with a deep learning project, the most significant bottleneck could be the lack of computational resources (e.g a GPU). But with Google Colaboratory (Google Colab or Colab in short), now you have the freedom to use a GPU at your disposal. Let’s see how you can clone your GitHub repository into Google Drive and run your code on top of a GPU provided by Google Colab.
#keeplearning #KeepSharing

```
from google.colab import drive
drive.mount("content/gdrive")

%cd /content/gdrive/MyDrive/Clone git repo(folder name)

#clone repo link
!git clone https://github.com/opencv/opencv.git
```

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1659929013390/597hrGP8c.png align="left")

