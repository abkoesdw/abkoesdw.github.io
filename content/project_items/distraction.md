+++
author = "Arief Koesdwiady"
title = "Data-Driven Driver Distraction Detection"
tags = [
    "project",
]
+++

In this project, we develop a data-driven driver distraction detection system, which consists of 3 major development stages:
* Offline Multiview Classification
* Offline End-to-End Deep Learning
* Real-time End-to-End Deep Learning 

The ultimate goal is to detect when a driver is distracted, i.e., doing activity other than driving such as texting, talking on the phone, etc, so that we can provide appropriate warning to the driver to stop him/her from being distracted.

### Driver Inattention Detection System: A PSO-based Multiview Classification Approach
In this stage, we use two types of sensors to measure the states of the driver: camera and pressure sensors. The objective is to include more information to produce greater accuracy and reliability. The overal approach is illustrated by the following figure:

{{< rawhtml >}}
<div style="text-align:center">
  <img src="/images/distract.png" width="95%" height="95%"/>
</div>
{{< /rawhtml >}}

The camera is positioned such that the upper-body and hand position of the driver are captured. To to detect the griping force and position of the driver's hand, four pressure sensors are located on the steering wheel at 10-2 o'clock position. Three paper-thin pressure sensors are attached to the right-top, left-top, and middle-bottom of the backrest to capture the driver's body movements.

{{< rawhtml >}}
<div style="text-align:center">
  <img src="/images/disdata.png" width="75%" height="75%"/>
</div>
{{< /rawhtml >}}

The experiment is carried out by participants with different ethnicities, genders, and ages. While driving in a driving simulator, we ask the participants to perform normal and distracted driving behavior.

{{< rawhtml >}}
<div style="text-align:center">
  <img src="/images/participant.png" width="75%" height="75%"/>
</div>
{{< /rawhtml >}}

***

**N.B.** The details of the work can be seen in  this paper: *Arief Koesdwiady, Ramzi Abdelmoula, Fakhri Karray, Mohamed Kamel. "Driver Inattention Detection System: A PSO-based Multiview Classification Approach". 2015 IEEE 18th International Conference on Intelligent Transportation Systems (IEEE-ITS). (pp. 1624-1629). IEEE*. [[link]](https://ieeexplore.ieee.org/abstract/document/7313356)

### End-to-End Deep Learning for Driver Distraction Recognition
In the second stage of the project,  we develop an end-to-end deep neural network (DNN) for driver distraction detection, which is motivated by the performance of DNNs in other applications. Our machine learning pipeline is illustrated in the following diagram:

{{< rawhtml >}}
<div style="text-align:center">
  <img src="/images/distraction.png" width="75%"/>
</div>
{{< /rawhtml >}}

We use only a video camera to capture the driver states. The camera is located such that the upper- body, hand positions, and rear-part of the car are captured and available to analyze. From the camera, sets of 640 × 480 - RGB video images with a frame rate 15 frames per second are obtained. In this experiment, two different cars are used in different lighting conditions. Ten drivers were involved in the experiments. Each driver was asked to perform or mimick the following driving activities: Normal/safe driving, Text messaging, Phone calling, Operating radio/navigation systems, etc.

{{< rawhtml >}}
<div style="text-align:center">
  <img src="/images/disdata2.png" width="75%"/>
</div>
{{< /rawhtml >}}

Despite the challenging aspects considered in the dataset in terms of different illumination conditions, camera positions and variations in driver’s ethnicity, and genders, the proposed end-to-end framework was able to detect different classes with a best test accuracy of 95% and an average accuracy of 80% per class.

*** 

**N.B.** The details of the work can be seen in  this paper: *Arief Koesdwiady, Safaa M Bedawi, Chaojie Ou, Fakhri Karray. "End-to-end Deep Learning for Driver Distraction Recognition". 2017 International Conference Image Analysis and Recognition (ICIAR). (pp. 11-18). Springer, Cham*. [[link]](https://link.springer.com/chapter/10.1007/978-3-319-59876-5_2)

### Real-Time End-to-End Deep Learning
At this stage, we try to test the real-time performance of our system under new environment. Our work has been covered by several media outlets, one of them is a news station in Toronto (see the picture below).

{{< rawhtml >}}
<div style="text-align:center">
  <img src="/images/online.png" width="75%"/>
</div>
{{< /rawhtml >}}