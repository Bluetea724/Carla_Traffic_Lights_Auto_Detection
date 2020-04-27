# Carla_Traffic_Lights_Detection

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
