# Real Time Object Detection Using Machine Learning

#### Introduction:

Welcome to the Git repository for my project in Computer Vision and Machine Learning. This repository consolidates all code, documentation, and resources developed throughout the project. It provides a clear overview of the work and guides you through the structure and contents of the repository



# Getting Started
### Conda

```bash
#Tensorflow CPU
conda env create -f conda-cpu.yml
conda activate yolov4-cpu

#Tensorflow GPU
conda env create -f conda-gpu.yml
conda activate yolov4-gpu
```

### Pip
```bash
# TensorFlow CPU
pip install -r requirements.txt

# TensorFlow GPU
pip install -r requirements-gpu.txt
```

### Commands:

```bash
python yolo_project.py --weights_location ./weights/yolov4-tiny-416 --model yolov4 --video_location cars_test.mp4

python yolo_project.py --weights_location ./weights/yolov4-tiny-416 --model yolov4 --video_location 0

python yolo_project.py --weights_location ./weights/yolov4-tiny-416 --model yolov3 --video_location ./test/video.mp4
```

```
--output ./detections/results.avi
  --video: path to input video (use 0 for webcam)
    (default: './data/video/video.mp4')
  --output: path to output video (remember to set right codec for given format. e.g. XVID for .avi)
    (default: None)
  --output_format: codec used in VideoWriter when saving video to file
    (default: 'XVID)
  --[no]tiny: yolov4 or yolov4-tiny
    (default: 'false')
  --weights: path to weights file
    (default: './checkpoints/yolov4-416')
 --info: print info on detections
  --model: yolov3 or yolov4
--framework: what framework to use (tf, trt, tflite)
```


#### Count Objects Per Class
To count the number of objects for each individual class of your object detector you need to add the custom flag "--count" as well as change one line in the detect.py or detect_video.py script. By default the count_objects function has a parameter called <strong>by_class</strong> that is set to False. If you change this parameter to <strong>True</strong> it will count per class instead.

#### Print Detailed Info About Each Detection (class, confidence, bounding box coordinates)
I have created a custom flag called <strong>INFO</strong> that can be added to any detect.py or detect_video.py commands in order to print detailed information about each detection made by the object detector. To print the detailed information to your command prompt just add the flag "--info" to any of your commands. The information on each detection includes the class, confidence in the detection and the bounding box coordinates of the detection in xmin, ymin, xmax, ymax format.

