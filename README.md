# Sensor Based Human Action Recognition using Smartwatch

Simple sensor based human action recognition end-to-end pipeline using Bi-LSTM model. We collect the dataset using our own smartwatch wear os sensor data collecter as you can check [here](https://github.com/farhantandia/Wearable-Sensor-Data-Collector). Our dataset consists of accelerometer and gyroscope from smartwatch data with the action of Walking, Standing, Jumping, and Falling, you can make and use your own dataset as well.

## Dependencies
- Tensorflow 1.14

## Method
<p align="center">
<img src="https://github.com/farhantandia/Sensor-HumanActionRecognition-Training/blob/master/sw-method.png"><br>
</p>

Human action recognition for wearable sensor data is conduct by using bidirectional long-short term memory (Bi-LSTM) to capture the long-term dependencies of hand movement and automate feature extraction from raw sensor inputs and multilayer perceptron as the classifier of each activity classes. In order to train our Bi-LSTM model, we do not perform any hand-crafted feature pre-processing and directly split each collected data into a number of windows. Through the experiment of different window sizes, in our case, we find the optimal window size is about 120 Hz with a step size of 20Hz. The Bi-LSTM learns to map and predict each window sensor data to an activity as shown in figure above.

## Deployment
You can save the model as frozen protobuf file and use our action recognition wear os application [here](https://github.com/farhantandia/Smartwatch-action-recognition) <br>.
