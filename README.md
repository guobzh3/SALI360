# SALI360
This is python code for the paper work accepted in ACM MMSys'20. You can access to the paper through this link.

## Prerequisities
- Language: Python
- Required Packages: numpy, pandas, matplotlib, scipy, sklearn, and opencv
- Need to install 'OpenCV' [link](https://www.pyimagesearch.com/2016/10/24/ubuntu-16-04-how-to-install-opencv/)
- Need to install 'transform360' developed by 'facebook' [link](https://github.com/facebook/transform360)
- The following link would be helpful for installation [link](https://github.com/facebook/transform360/issues/56)
- Need to install 'FFMPEG' [link](https://www.ffmpeg.org/download.html)
- To install the required package, type the following command:

1) Python 2
```
pip install numpy pandas matplotlib scipy sklearn
```
2) Python 3
```
pip3 install numpy pandas matplotlib scipy sklearn
```

## Dataset
We collected head and eye gaze movement dataset from 20 vonlunteers over 10 360-degree VR video.


### Running the code
- How to generate the eye gaze heat map
```
python3 eye_gaze_heatmap.py
```
The command above would generate the eye gaze heatmap figure shown below in 'figure' directory, named 'eye_gaze_heatmap.png'. 

![Data Filter](figure/eye_gaze_heatmap.png)

- How to plot yaw & pitch deviation from center of front face 
```
python3 gaze_deviation.py
python3 gaze_deviation_visualization.py
```
1. The first command 'python3 gaze_deviation.py' calculates the yaw and pitch deviation from the center of front face in cube map representation, which would be saved in a format of 'pickle' file in 'data' directory to be used in the following script. 
2. 'gaze_deviation_visualization.py' would save the deviation plots, each of which would be saved as 'type_of_data'_'duration'.png (e.g., pitch_2.png) in the 'figure' directory. The figure below is 'pitch_5.png that shows the deviation pattern when 5-second-of video segments are streamed. 

![Interpolation](figure/pitch_5.png)

Pyramid Encoding
```
python3 pyramid_b_encoding.py
```
Pyramid Decoding
```
python3 pyramid_b_decoding.py
```
Saliency to Json Files
```
python3 saliency_json.py
```
Saliency Stitching
```
python3 saliency_stitching.py
```
