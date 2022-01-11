+++
author = "Arief Koesdwiady"
title = "Event-Based Data Fusion using Dempster-Shaffer Theory"
tags = [
    "project",
]
+++

In this project, we develop a technique to fuse asynchronous hard and soft data. We use the traffic prediction problem in a smart city as the case study. More specifically, we develop short-term traffic flow prediction approach that uses two types of data: streams of data, and event-based data. 

{{< rawhtml >}}
<div style="text-align:center">
  <img src="/images/stream.png" width="75%" height="75%"/>
</div>
{{< /rawhtml >}}

In this work, Deep Belief Networks (DBNs) are used to independently predict traffic flow using streams of data, i.e., historical traffic flow and weather data, and event-based data, i.e., tweets. 

Furthermore, Dempster’s conditional rule for updating belief is used to fuse evidence coming from streams of data and event-based data modules to achieve enhanced prediction. The experimental results using real-world data show the merit of the proposed framework compared to the state-of-the-art ones.

{{< rawhtml >}}
<div style="text-align:center">
  <img src="/images/dset.png"/>
</div>
{{< /rawhtml >}}

**N.B.** The details of the work can be seen in  this paper: *Ridha Soua, Arief Koesdwiady, Fakhri Karray. "Big-data-generated Traffic Flow Prediction using Deep Learning and Dempster-Shafer Theory". 2016 International Joint Conference on Neural Networks (IJCNN). (pp. 3195-3202). IEEE*. [[link]](https://ieeexplore.ieee.org/abstract/document/7727607).