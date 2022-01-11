+++
author = "Arief Koesdwiady"
title = "GAN for Multi-Step Time Series Prediction"
tags = [
    "project",
]
+++

Multi-step time series prediction is known to suffer from increasing performance degradation the farther in the future the predictions are made. In this work, we introduce two approaches to address this weakness in recursive and multi-output prediction models. 

One weakness of the recursive prediction is that it does not take into consideration the number of steps predicted by the model so far. The amount of correction the model needs to add differs from time-step to another along a multi-step prediction trajectory, since the deviation from ground truth is less acute in early steps. Therefore, the model stands to benefit from having information about the current time-step along the prediction trajectory. In particular, the amount of correction the model needs to add is affected by the number of time-steps that have passed in which the model used its prediction as input to the next time-step.

Based on this, we propose a time-step-augmented (TSA) recursive model, in which the input is augmented with a representation of the current time-step.

{{< rawhtml >}}
<div style="text-align:center">
  <img src="/images/tsa.png" width="75%" height="75%"/>
</div>
{{< /rawhtml >}}

In some applications, recursive models do not perform well compared to other approaches such as multi-output models. Nonetheless, the performance of multi-output models
suffers degradation as the prediction time-step increases. We introduce a Conditional-Generative Adversarial Network (C-GAN) based data augmentation approach to improve multi-output multi-step time series prediction.

{{< rawhtml >}}
<div style="text-align:center">
  <img src="/images/gan.png" width="75%" height="75%"/>
</div>
{{< /rawhtml >}}

We develop GAN models that generate historical data conditioned on the future data. This way, we can enrich our datasets with an infinite amount of historical-future pairs of data for training purposes. The experiments show that the proposed approaches are able to improve multi-step time series predictions relative to their baselines. The degree of improvement however is dependent on the context. For example, the TSA model reduces errors most significantly in the farther time steps, while it performs
comparatively to the recursive baseline in the immediate future.

On the datasets we use (which are real-world datasets from applications such as traffic flow to currency markets), the multi-output models generally perform better than the recursive ones. More specifically, C-GAN based approach outperforms other approaches in all the datasets and has shown significant improvement on the predictions.

{{< rawhtml >}}
<div style="text-align:center">
  <img src="/images/multi-res.png" width="75%" height="75%"/>
</div>
{{< /rawhtml >}}

*** 

**N.B.** The details of the work can be seen in  this paper: *Arief Koesdwiady, Alaa El Khatib, and Fakhri Karray. "Methods to Improve Multi-Step Time Series Prediction". 2018 International Joint Conference on Neural Networks (IJCNN). (pp. 1-8). IEEE*. [[link]](https://ieeexplore.ieee.org/abstract/document/8489402)