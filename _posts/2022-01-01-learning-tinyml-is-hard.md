---
layout: post
title:  "Learning TinyML is Hard. Here is what ScaleDown is trying to do about it"
author: soham 
categories: [ education ]
image: assets/images/learning_tinyml/scaledown-blogs.png
tags: [ featured, sticky ]
---
A few days ago, we announced that our [project received the No Starch Press Foundation grant](/_posts/2021-12-21-nspf.md). Their decision has given us the motivation to continue working on this project and the confidence that our goal to make TinyML education easier is a challenge that is worth pursuing and an important contribution to the FOSS community.

When we started this project (and applied for the grant), our vision was clear: TinyML will be an important field (in the industry and academia) soon, but learning TinyML is hard. Our goal was simple: Democratize TinyML Education.

In this blog, I want to discuss why we think TinyML is hard to learn and highlight how we plan to make it easier. Let’s first start with why it is hard.

# Why Learning TinyML is Hard
TinyML combines techniques from software/embedded development, machine learning, and electronics engineering to run ML models on embedded devices. As a TinyML engineer, you could specialize in one of those fields, but it is important to know a bit about all of them (and also how they interact and link together) to build projects and to appreciate the challenges and complexities of this field.

> When we started this project, our vision was clear: TinyML will be an important field soon, but learning TinyML is hard. Our goal was simple: Democratize TinyML Education.

I know mainly about ML and electronics engineering and very little about developing software for embedded devices. I am sure that many of you also know one or two of the fields and are looking to learn more about the others but have no idea where to start or have been suggested extensive and in-depth learning resources (or maybe even college courses). And this is the first problem of learning TinyML:

- **Few Educational Resources:** You might have been told that to be a TinyML engineer, you need to be an expert at machine learning, electronics engineering, and embedded development. These are vast areas of study that can take years to master, but the truth is that you only need to know specific parts of those fields to learn TinyML! For instance, if you are an embedded engineer looking to learn ML, you don’t need to know about transformers or graph-based neural networks or GANs since it will be a while (if ever) that they are used for TinyML.

	The problem is that there aren’t many resources focused solely on teaching the relevant TinyML concepts, and it can be easy to get lost or stuck when learning these fields with the typical learning resources.

- **Need for Hardware:** An integral part of learning TinyML is to try to deploy a model to an embedded device. Nowadays, many cloud services provide remote access to hardware to deploy models. For instance, you can use the [Intel DevCloud](https://www.intel.com/content/www/us/en/developer/tools/devcloud/edge/overview.html) to deploy to Intel devices. You can also use [Edge Impulse](https://www.edgeimpulse.com/) to deploy to your smartphone.

	Unfortunately, you cannot physically manipulate the device with hosted hardware, which is essential if your project uses sensors like an IMU, pressure sensor, or accelerometer. Moreover, having physical hardware access helps you learn the intricacies of properly powering them, collecting data, attaching sensors, and integrating with other systems.

	Moreover, while TinyML hardware may seem cheap, they are still expensive and inaccessible to a large group of people. For instance, in India, the cost of a US$ 35 Raspberry Pi is equivalent [to a large chunk of (or even more than)](https://timesofindia.indiatimes.com/business/india-business/top-1-hold-22-of-income-india-among-most-unequal-nations-shows-report/articleshow/88149699.cms) the monthly income of most families! And I am sure this is the case in many other countries as well. If you include the cost of sensors, wires, resistors and caps, batteries, breadboards, and power devices, then the price quickly becomes unaffordable. Even free hardware (like those from hackster competitions) are usually new devices and not ideal for beginners.

	We believe that this is one of the most significant factors stopping more people from learning TinyML and is one of the primary reasons we created ScaleDown.

- **Hardware and Software Ecosystem:** The TinyML hardware-software ecosystem has many companies, researchers, and open-source projects building tools, compilers, hardware, and frameworks. This environment is rare in most fields and is something I love about TinyML. It allows developers to try out multiple solutions and choose the most optimized solutions for their projects.

	On the other hand, this makes it a nightmare for beginners who don’t know which tools, frameworks, and hardware to use. For instance, if you are using TFLite, that won’t work with Intel edge devices requiring OpenVINO, and OpenVINO does not support non-Intel devices. So a beginner with only a Raspberry Pi has no way to evaluate the performance of their model using the MKL DNN library.

	Finally, we feel that there is a disconnect between academia and the TinyML tools available to developers. For instance, new methods of quantizing and pruning models are published regularly. But as a developer, I cannot integrate and evaluate them into an existing project quickly.

# How is ScaleDown Trying to Help?
Not too long ago, we were beginners and faced similar issues when learning TinyML. This motivated us to find a way to provide the community with easy ways to learn TinyML and become TinyML engineers.

Here are the ways we plan to solve these challenges and help democratize TinyML education:

- **Free Educational Resources:** One of the main goals of our project is to provide the community with free and open-source resources they can learn from. These will include not only written materials like blogs, books, and articles but also video tutorials and study groups to learn together. We want these resources to be a healthy mix of academia and industry, so we will also do paper reviews and create tutorials for projects.

	We plan to create educational resources not only for beginners and early career professionals but also for mid-career professionals who want to level up their skills and keep in touch with the latest advances in the field. You can check out these resources [here](https://scaledown-team.github.io/learn/).

- **Hardware Library:** To help reduce the financial burden on beginners, we want to build a worldwide hardware library. The library will be free so users can borrow hardware to learn, practice, and develop and test projects.

	The hardware cost was a significant bottleneck for me during my learning journey, which is why creating this library is very close to my heart. I had to borrow Raspberry Pi’s from other people and buy unreliable knock-off Arduino boards and sensors that would break often. It was only due to the generosity of the maker/hacker community around me that I was able to learn about this field, and this is our way of helping the next generation of engineers!

> We plan to create educational resources not only for beginners and early career professionals but also for mid-career professionals who want to level up their skills and keep in touch with the latest advances in the field

- **ScaleDown Framework:** Finally, we want to create a software framework that is a wrapper over the common TinyML frameworks. The framework will make it easy for beginners with knowledge of different frameworks/toolkits by providing them with a standard API to do similar tasks regardless of the frameworks they know or use. We hope to make our framework hardware and software agnostic by adding support for new TinyML algorithms, the latest hardware and software tools, and TinyMLOps tools.

	We hope that this will reduce the barrier to entry for beginners and help them focus on learning TinyML principles instead of learning framework-specific code.


# How Can You Help?
This project is a huge undertaking, and we need all the help we can get. If you are someone who is interested and wants to help out, here are some of the ways you can get involved:

- **Educational Material:** Help us create educational materials. We need help writing blogs, articles, building projects, and doing paper reviews. 

- **Hardware Library:** You can help out here by starting a library in your city, school, or university. We also need help figuring out the logistics and operations of a hardware library.

- **ScaleDown framework:** You can help us by adding support for different hardware, software toolkits, and algorithms.

To help out, check out our guide. Feel free to also reach out to us via email or join our weekly call. We hope to see you there soon!
