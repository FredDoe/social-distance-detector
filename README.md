# Social Distance Detector :cop::heavy_minus_sign::cop:
Social distancing detector built with OpenCV using YOLO object detector
<p align="left">
   Social distancing is crucial to the prevention of the spread of contagious diseases.
</p>


## Installation :package:

1. Clone the repository

```bash
   $ git clone git@github.com:FredDoe/social-distance-detector.git
   $ cd social-distance-detector
```

2. Create Virtual environment and Install dependencies

```
python -m venv venv

source venv/Scripts/activate

pip install -r requirements.txt
```

3. Run the main social distance detector file. (set display to 1 if you want to see output video as processing occurs)
```
python social_distancing_detector.py --input pedestrians.mp4 --output output.avi --display 0
```


## Running this Application :computer:
* Caution :bomb:\
For most accurate results, you should calibrate your camera through intrinsic/extrinsic parameters so that you can map pixels to measurable units.
An easier alternative(but less accurate) method would be to apply triangle similarity calibaration. Both of these methods can be used to map pixels to measurable units.\
If you do not want/cannot apply camera calibration, you can still utilize the social distance detector but you'll have to rely strictly on the pixel distances, which won't necessarily be accurate.
For the sake of simplicity, this OpenCV Social Distancing detector implementation will rely on pixel distances. 
You can extend the implementation as you see fit though :wink:.

* YOLO COCO weights\
The weight file exceeds the github limits but can be download from <a href="https://pjreddie.com/media/files/yolov3.weights">here</a>.\
Add the weight file to the yolo-coco folder.

* GPU\
Provided you already have OpenCV installed with NVIDIA GPU support, all you need to do is set ```USE_GPU=True``` in your ```config.py``` file.

## Demo :movie_camera:
![raw-vid](res/demo0.gif "Unprocessed video") ![processed-vid](res/demo1.gif "Processed video")



## References :book:
* Inspiration from Adrian Rosebrock's <a href="https://www.pyimagesearch.com/2020/06/01/opencv-social-distancing-detector/">OpenCV Social Distancing Detector</a> :heart:
* <a href="https://en.wikipedia.org/wiki/Social_distancing">Social Distancing</a>
* <a href="https://www.reddit.com/r/computervision/comments/gf4zhj/automatic_social_distance_measurement/">Automatic social distance measurement</a>
* <a href="https://www.linkedin.com/feed/update/urn%3Ali%3Aactivity%3A6661455400346492928/">Rohit Kumar Srivastava’s social distancing implementation</a>
* <a href="https://www.linkedin.com/feed/update/urn%3Ali%3Aactivity%3A6655464103798157312/">Venkatagiri Ramesh’s social distancing project</a>


## License :key:

MIT &copy; Godfred Doe
