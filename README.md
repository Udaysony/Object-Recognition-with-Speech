# Object-Recognition-with-Speech
[Source project](https://github.com/miyosuda/TensorFlowAndroidDemo)

 It is compatible with Android Studio and usable out of the box. It can detect the 20 classes of objects in the Pascal VOC dataset: aeroplane, bicycle, bird, boat, bottle, bus, car, cat, chair, cow, dining table, dog, horse, motorbike, person, potted plant, sheep, sofa, train and tv/monitor. The network only outputs one predicted bounding box at a time for now. The code can and will be extended in the future to output several predictions.

To use this demo first clone the repository. Download the TensorFlow YOLO [model](https://drive.google.com/open?id=1j8uGXuYaqmxup6J2iokXcPF-X-1aShDI) and put it in /app/src/main/assets. Then open the project on Android Studio. Once the project is open you can run the project on your Android device using the Run 'app' command and selecting your device.


Disclaimer:
The app is hardcoded for 20 classes and for the tiny-yolo network final output layer.

The code describes the interpretation of the output.

The code for the network inference pass is written in C++ and the output is passed to Java. The output of the network is in the form of a String which is converted to a StringTokenizer and is then converted into an array of Floats in line 87 of TensorflowClassifier.java

You can work from there and read the papers to transform the new yolo model output into something that makes sense. 
