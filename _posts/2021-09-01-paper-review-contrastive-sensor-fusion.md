---
layout: post
title:  "Contrastive Sesion Fusion and its Applications in TinyML"
author: archana 
categories: [ paper review ]
image: assets/images/paper-review-csf/csf-cover.png
tags: [ featured ]
---

Often times the data your model is trained with will be different from the data it received when deployed. For instance, in an image classification task, your training data may have been captured with a camera resolution or in a lighting condition that is different from the actual conditions when deployed. How do you train your model to account for these differences?

**This article was originally published in Edge Impulse [here](https://www.edgeimpulse.com/blog/paper-review-contrastive-sensor-fusion-method-and-its-potential-applications-to-tinyml)**

The authors of the paper *[Representation Learning for Remote Sensing: An Unsupervised Sensor Fusion Approach](https://arxiv.org/pdf/2108.05094.pdf)*, realised that this is a major issue especially for remote sensing data where images can be captured with sensors of different resolutions and channels. Moreover, images of the same location can change significantly over a short period of time, even if they have been taken by the same sensor. Finally, since most objects in these images are really small, labelling is a huge challenge.

With these problems in mind, the authors tried to train a model that can create meaningful representation from unlabelled images that can learn from multiple combination of sensors and channels (even if certain sensors or channels are missing). The authors show that their technique can generate useful representations and even outperform models with ImageNet weights.

You can read a more in-depth review of the paper at *[this blog by Edge Impulse](https://www.edgeimpulse.com/blog/paper-review-contrastive-sensor-fusion-method-and-its-potential-applications-to-tinyml)* and you can find the full code for the paper *[here](https://storage.cloud.google.com/public-published-datasets/csf_code.zip)*.

## How can this help with TinyML?
Even though this is not a TinyML paper and the authors of the paper never mention TinyML, it is still really exciting for me because of its immense potential for applying it to TinyML.

The biggest application for this is how it can be used to make trained models more robust to changes in sensor configurations like lighting and resultion (in case of cameras) or precisions and ranges (in case of most other sensors). It could make systems more resilient to damaged sensors as well. Another application is how it can be used to switch off sensors one at a time when battery is running low. This would allow for graceful degradation of devices.

You can read in more detail about potential application in TinyML *[here](https://www.edgeimpulse.com/blog/paper-review-contrastive-sensor-fusion-method-and-its-potential-applications-to-tinyml#future-work-and-potential-areas-of-expansion-to-tinyml)*
