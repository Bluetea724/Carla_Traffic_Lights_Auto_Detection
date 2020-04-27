# Carla_Traffic_Lights_Auto_Detection

You only look once (Yolo) is a state-of-the-art, real-time object detection system. The strong points of Yolo are fast and accurate. Currently, if CARLA user wants to use Yolo, they have to capture and label themselves. But I will make auto labeling feature to assist user's convenience, but also can be used as unsupervising learning. After capturing data, I checked those data with Yolo_mark which is yolo label program. Then, I trained, and tested it on CARLA.

# 1) Manual_control.py - main source code

Use ARROWS or WASD keys for control.

    W            : throttle
    S            : brake
    AD           : steer
    Q            : toggle reverse
    Space        : hand-brake
    P            : toggle autopilot
    M            : toggle manual transmission
    ,/.          : gear up/down

    TAB          : change sensor position
    `            : next sensor
    [1-9]        : change to sensor [1-9]
    C            : change weather (Shift+C reverse)
    Backspace    : change vehicle

    R            : toggle recording images to disk, and verify whether there is traffic signal in that screen or check based on Yolo
        1) If YoloUse = 0 -> traffic light auto detection based on Houghcircles function
        2) If YoloUse = 1 -> traffic light auto detection based on Yolo

    CTRL + R     : toggle recording of simulation (replacing any previous)
    CTRL + P     : start replaying last recorded simulation
    CTRL + +     : increments the start time of the replay by 1 second (+SHIFT = 10 seconds)
    CTRL + -     : decrements the start time of the replay by 1 second (+SHIFT = 10 seconds)

    F1           : toggle HUD
    H/?          : toggle help
    ESC          : quit

# 2) obj.data, obj.names, train.txt, yolov3-tiny.cfg 
Yolov3-Darknet configuration files

yolov3-tiny.cfg -> need to change filter and classes
    1) Currently, classes are 3 which are Green, Yellow, Red
    2) filters=(classes + 5)x3

train.txt -> image information what you want to train

# 3) Yolo dataset and weight file 
You can find it with this url: https://drive.google.com/drive/folders/1Inju5YEVRLnQ6I-fPgB81yhJ2TZkl6Su?usp=sharing

# 4) Other tools for this project
Yolo mark - https://github.com/AlexeyAB/Yolo_mark

Yolo Darknet - https://github.com/pjreddie/darknet
