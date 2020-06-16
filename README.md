# License-Plate-Recognition
1. License plate detection using **YOLOv4** trained on custom data. </br>
  a. YOLOv4 - mAP(), IOU(), fps() </br>
  b. YOLOv3 - mAP(), IOU() </br>
  c. YOLOv2 - mAP(), IOU() </br>
2. Plate text detection and recognition using keras-ocr. </br>
3. Rejecting false positives using pattern matching w.r.t. Indian license plates. </br>

### Requirements:
Yet to be added

### Demo:
<pre><code> #Run demo on sample video with default arguments
 python demo_video.py
 
 #Run demo with command line arguments </br>
 python demo_video.py --input <Input_video_path> --output <Path_to_save_result> --size <frame_size>"
 
 #Example
 python demo_video.py --input inputs/demo1.mp4 --output results/output1.avi --size 608 </code></pre>

<pre><code>#Run demo on sample image with default arguments
python demo.py

#Run demo with command line arguments
python demo_video.py --input <Input_image_path> --output <Path_to_save_result> --size <frame_size>"

#Example
python demo.py --input inputs/1.jpg --output results/output1.jpg --size 608 </code></pre>

#Note - Size must be a multiple of 32. Increasing size increases the accuracy of license plate detection but requires more memory. Reduce the size if your gpu runs out of memory.

### Results:
![results/output1.jpg](https://github.com/keshavoct98/License-Plate-Recognition/blob/master/results/output1.jpg)
![results/output2.jpg](https://github.com/keshavoct98/License-Plate-Recognition/blob/master/results/output2.jpg)
![results/output3.jpg](https://github.com/keshavoct98/License-Plate-Recognition/blob/master/results/output3.jpg)
![results/output4.jpg](https://github.com/keshavoct98/License-Plate-Recognition/blob/master/results/output4.jpg)
![results/output1.gif](https://github.com/keshavoct98/License-Plate-Recognition/blob/master/results/output1.gif)
![results/output2.gif](https://github.com/keshavoct98/License-Plate-Recognition/blob/master/results/output2.gif)

### How to train:
1. Download dataset zip from this link - https://www.kaggle.com/tustunkok/license-plate-detection/data
2. Create a folder named 'dataset' inside 'data' and extract the content of zip into 'dataset' folder.
3. Go to 'data' folder and run the given command on cmd - "python augmentation.py". After augmentation number of images will be 2154.
4. Now to train darknet YOLOv4 on the dataset, follow the steps given here - https://github.com/AlexeyAB/darknet#how-to-train-to-detect-your-custom-objects

### References
https://www.kaggle.com/tustunkok/license-plate-detection/data
https://github.com/AlexeyAB/darknet
https://github.com/hunglc007/tensorflow-yolov4-tflite
http://openaccess.thecvf.com/content_ICCVW_2019/papers/RLQ/Nguyen_State-of-the-Art_in_Action_Unconstrained_Text_Detection_ICCVW_2019_paper.pdf
https://pypi.org/project/keras-ocr/
