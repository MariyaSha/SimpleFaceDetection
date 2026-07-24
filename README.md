# SimpleFaceDetection
A Simple Face Detection and Object Detection Workflow for Images and Real Time Video Streams

## Face Detection Model Source
This workflow relies both on the official version of YOLO that we download directly from our Python code, as well as a community version of YOLO, `yolov8m-face.pt`, that we download from here:
<br>
https://github.com/akanametov/yolo-face
<br>
<br>
Huge shoutout to Akanametov for sharing his community version of YOLO-Face with the world!
<br>
Please give him a star and a follow if you end up using this workflow:
<br>
https://github.com/akanametov

## Installation Instructions - CPU:
1. Install Miniconda on your Windows system: https://www.anaconda.com/download/success
2. Set up a working environemnt:
```
conda create -n detection_env python=3.12
conda activate detection_env
```
3. Install dependencies:
```
pip install opencv-python ultralytics jupyter
```
4. Open Jupyter Lab:
```
jupyter lab
```
5. Run notebooks.

## Installation Instructions - GPU:
Same as the CPU instructions from above, but with the following Pytorch addons:
1. Find your version of CUDA in your terminal with: `nvidia-smi`
2. Find the right command for your version of CUDA here: https://pytorch.org/get-started/locally/
3. If the right command for your version of CUDA is `pip3 install torch torchvision --index-url https://download.pytorch.org/whl/cu130` then do the following:
   - uninstall Pytorch, such that: `pip uninstall torch torchvision`
   - only then, right command for your version of CUDA: `pip install torch torchvision --index-url https://download.pytorch.org/whl/cu130`
4. Open Jupyter Lab:
```
jupyter lab
```
5. Run notebooks.

## Download Demo Images

There are two ways to get the demo images used in this tutorial.

### Option 1 (Recommended)

Clone this repository. All resized demo images are already included and ready to use.

### Option 2

Download the original high-resolution images from Magnific and resize them yourself using the code below.

### Demo Image Sources

demo.jpg (Girl + Cat)
https://www.magnific.com/free-photo/beautiful-stylish-woman-purple-suit-hat-walking-city-street-spring-summer-autumn-season-fashion-trend-black-cat_11576374.htm#fromView=search&page=1&position=8&uuid=b7d0d360-4260-48fc-9f61-3005a0486868&query=cat+lady

demo1.jpg (Cyclist + Cars)
https://www.magnific.com/free-photo/cyclist-riding-bridge-city-dynamic-motion-with-blur-effect_427602721.htm#fromView=search&page=1&position=31&uuid=8c46b620-363f-45fe-b57c-280a59fac0c3&query=vehicles

demo2.jpg (Kitchen)
https://www.magnific.com/free-photo/portrait-beautiful-brunette-girl-chopping-vegetables-meal-making-salad-kitchen-eating_78042227.htm#fromView=search&page=1&position=20&uuid=38c9393f-bb3d-4cb1-ae0f-b9eaaa835d21&query=kitchen

demo3.jpg (Sheep)
https://www.magnific.com/free-photo/mother-sheep-with-its-two-baby-sheep-grassy-field-daytime_11063035.htm#fromView=search&page=2&position=25&uuid=4838e797-6eb9-4369-971a-6549ce62d2f6&query=dog+sheep

demo4.jpg (Laptop, Cup & Mouse)
https://www.magnific.com/free-photo/laptop-mouse-top-view_7342965.htm#fromView=search&page=1&position=16&uuid=bb4236e1-ad8c-4b86-a33d-b209ded588a1&query=computer

### Resize the Images

Use the following OpenCV code to resize each downloaded image to approximately 15% of its original size.

```python
import cv2

img = cv2.imread("original_image_name.jpg")

resized_img = cv2.resize(
    img,
    None,
    fx=0.15,
    fy=0.15
)

cv2.imwrite("resized_image_name.jpg", resized_img)
```
