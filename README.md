
# YOLOV3 implementation on Open Images + Color Detection
Colour blindness is a deficiency, which decreases the ability to differentiate between colours or to see colour. People suffering from colour blindness find it difficult to perform simple tasks like reading traffic signals, during cooking, or picking clothes. This project aims to help colour blind people through object detection and predicting the colour through deep learning algorithm “YOLO”. This project uses Raspberry Pi and camera module to capture image. Then pre-processed image is sent to cloud via REST API. On cloud the image is post processed where the YOLO algorithm finds the objects in the image and the colour of object. And this information is sent back to Raspberry Pi, where text is converted to sound and sent to speaker. There are many practical applications, but the project focuses on helping with the colour of clothes.
# Implementation
IOT Architecture and Hardware architecture
![alt-text](https://github.com/aveen-d/MultiObj_Det_and_Color_Identificaion/blob/master/results/iot1.png)

![alt-text](https://github.com/aveen-d/MultiObj_Det_and_Color_Identificaion/blob/master/results/iot2.PNG)
# Results

![alt-text](https://github.com/aveen-d/MultiObj_Det_and_Color_Identificaion/blob/master/results/iot3.PNG)

## Which model to use
Use any of the below ways to build the model. Put the .h5 model in model_data
 1. Convert pjreddie's darknet model to keras using qqwweee's tool below.
 2. Use [oimodel.py](https://github.com/aveen-d/MultiObj_Det_and_Color_Identificaion/blob/master/oimodel.py) to build a model with randomly initialized weights and train it yourself.
 3. Use [oimodel.py](https://github.com/aveen-d/MultiObj_Det_and_Color_Identificaion/blob/master/oimodel.py) and comment out the setweights line to use pjreddie's weights. Then customize the layers as you wish. 
 4. Use [layer_config.json](https://github.com/aveen-d/MultiObj_Det_and_Color_Identificaion/blob/master/layer_config.json) to customize your own layers and their parameters. See keras docs for loading json config files as pre trained models.
 ## Docker Build Instructions
 On a linux machine, enter the following in the terminal

    sudo docker build -t <yourtagname> .
tagname will be of the format "username/imagename"
Push it to dockerhub by

    docker push <tagname>
Deploy :D
## Model
Download the tensorflow model from the following link [model](https://drive.google.com/file/d/1nQF4ZYxI9Tw3RF7oe-4eWw5WqPSaZzen/view?usp=sharing)
## Credits
https://github.com/qqwweee/keras-yolo3 for converting the darknet model to .h5 keras model

