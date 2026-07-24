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
