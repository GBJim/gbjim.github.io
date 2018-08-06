---
layout: post
title:  "Paper Reading: Distilling the Knowledge in a Neural Network"
date:   2018-08-30 00:59:29 +0800
categories: algorithm
ref: distilling
lang: en
comments: true
---
### **Abstract**
This paper is written by the Deep Learning Pioneer, Geoffrey Hinton at Google. I would like to concluded the main idea as follows. **A strong Neural Network can teach a weak Neural Network that helps the weak model learns better**. Please refer to the original publication: [Distilling the Knowledge in a Neural Network](https://arxiv.org/abs/1503.02531) for complete understanding.

### **Motivation: The Trade-off between Accuracy and Speed**
Be accurate or be fast, there is always a trade-off. Considering a scenario, we have a weak model that inferences fast and a strong model that works slow.
[image]

If the speed is the hard requirement, we would just pick the weak model and do the training.
[image]
It seems like having a strong but slower model does not benefits in this scenario. But the model distillation gives a way to improve the weak model by using the strong model as a teacher.


### **How Distillation Works?**


### **Why Distillation Works?**


<br />
$$
Softmax Functions.
$$q_i = {exp(z_i) \over \sum_{j=1}^n exp(z_j)}$$
$$



$$
Distilling Version of Softmax where $T$ is the tempture.
$$q_i = {exp(z_i/T) \over \sum_{j=1}^n exp(z_j/T)}$$
$$

### **Main Idea**
A great beginning that goes down.
After the intro of awesome electronic music and Dubstep, Robin Li, CEO of Baidu, started the presentation. His smooth tone and good-looking gives him the great charisma on the stage. During his presentation, a live stream shows the moment of the 100th production of self-driving L4 minibus in Xiamen factory. This is truly a shocking moment to me.
After the CEO opening, each presentations got worse and even more. The contents keep repeating it's self and speakers were not able to talk naturally. There were even a speaker recites the whole presentation. I believe the Baidu talking bot can do a better job.
In the other hand, the organization of events are confusing. The traffic flow was badly managed and the some of the agenda were modified without any notifications. I would say this disappointing for a Chinese leading company like Baidu.
Nevertheless, I had learned lots of lessons from the conference. Let's get started.

### **Four Opend Platforms**
The cores of this conference are the following open platforms:

#### **DuerOS**
It's simply an interactive voice system similar to Amazon Alexa and Google home. Baidu was convincing developers and customers to join the ecosystem of DuerOS.
What I do not see, is the business potential of this kind of systems. It might be convenient for a driver to query the system with his voice while his hands are busy at steering. But a smart phone can simply do this and does it even better. As for the smart speakers, I truely consider them as some redundant products you will buy and then forget.
It's worth mentioning that Voice Interaction is simply an UI. The role of Voice Interaction is as same as a keyboard or a mouse. The intelligent behaviors of the machine depend on something more complicated than UI.

#### **Baidu Brain**
A platform with more than 200 Machine Learning features. It has every kind of tools you may think of.
Baidu Brain is suitable for those well-defined classical Machine Learning problems. A developer without ML knowledge can solve simple ML problem using Baidu Brain. **Simple problems can be extremely critical and invaluable**
During Robin Li's presentation, a Doctor from Tibet were invited to share his developing experiences. He built a predictive model that classifies parasites in water. The accurate model can replace the classification from professional parasite expert. In a vast place like Tibet, this invention saves peoples lives from the infection of parasites.
I were touched when during the doctor's presentation. He used the technology to make the world better. This is especially worthy in the era that smartest developers are designing more annoying Advertisement and more luxury smart phones.
![doctor](/assets/img/bc-doctor.jpg){:class="img-responsive"}
*The Tibet Docotr who built the parasite classifier, This world needs more people like him*
<br />

#### **Baidu Mini Programs**
In simple words, Baidu intends to build a huge APP platform that has every service you need. The idea is similar to WeChat Mini Programs.
The speaker mentions an interesting phenomenon: **Greenhouse Garden**. It describes that Internet were free and open in the beginning, but was eventually monopolized by few enterprises. Those enterprises provides all the services you need in their platforms, meaning the users can do everything within a platform. The Internet becomes split and isolated.
The speaker claimed that Biadu Mini Programs can breaks this isolation and returns the free and opened Internet. **This does not make any freaking sense.** Anyone can tell that Baidu want to build it's own Greenhouse Garden.
<br />
![lie](/assets/img/bc-lie.jpeg){:class="img-responsive"}
<br />

#### **Apollo**
This is the highlight of the conference. Baidu presented the Apollo shuttle bus, an vehicle co-produced with King-Long Bus. In the other hand, some startups extended Apollo to robotics field. Apollo cleaning robot and Apollo spray truck are introduced in the conference as well.
In the following section, I will stress on the the development of Apollo.
<br />
<br />

### **Production of Mini Shuttle Bus**
![bus](/assets/img/bc-bus.jpg){:class="img-responsive"}
*The blue print of minibus and it's sensors*
<br />
The Baidu minibus can only cruise in closed areas such like Science Parks or Factories, meaning the autonomous level does not reach the urban-L4 we expected. Nevertheless, this production experience are extremely important to Baidu.
Production is much more demanding than building a demo machine. Production requires an efficient and strict standard to produce high quality products in low cost. The speaker gave two technical examples of sensor calibrations in productions. The calibration between camera and LiDAR; and the calibration between GPS and LiDAR.

<br />

![sesonr1](/assets/img/bc-sensor-cali1.jpg){:class="img-responsive"}
*The calibration room in Ximen factory. The QR codes on the wall are markers for correcting the difference between cameras and LiDARs*
<br />

![sensor2](/assets/img/bc-sensor-cali.jpg){:class="img-responsive"}
*Calibration between GPS and LiDAR is done by driving an 'eight' shape *
<br />
The generation of massive data from minibus is the benefits of massive productions as well.
<br />


### **From Cars to Robots**
Compare to car manufacturers, Internet companies can extends the scope of Autonomous Driving in a more flexible way. There are two startups leverages Apollo to build robots.
The Cowa Robot from Shenzhen release their road cleaning robots to supply the huge demands of Chinese Cleaning Market.
Ther other company from Qingdao demonstrates their self-driving spray vehicle. An awesome example combining Agriculture and technology.

![cow](/assets/img/bc-cow.jpg){:class="img-responsive"}
*The spray vehicle is working in Qingdao*
<br />

### **The codes evolve with Business Model**
Since July 2017, Apollo was released, Baidu already had the idea to establish the self-driving ecosystem. In that moment, Apollo-1.0 only had defined the modules and interfaces without much implementations. Developers consider it as Business Promotion rather than a practical tool.
After a year, the solutions for low cost sensors and production concept were integrated into Apollo. This actually reflects Baidu's exploration in Business Model. In the beginning, Apollo serves as a business promotion without a clear target. Then, Baidu determines the clear goal of minibus production. All these business directions can be seen in the development of Apollo.
We will observe this reflection between code and business in future.
![evolve](/assets/img/bc-evolve.png){:class="img-responsive"}
*Evolution of Apollo*
<br />
<br />
### **The Ambition to become Chinese Standard**
Baidu's plan to build a league of Apollo goes smoothly. A Chinese car company BYD declares to join Apollo on the conference. Besides, the other car companies also have cooperations with Baidu on different scales. For example, Hyundai and KIA have vehicles with DuerOS installed. Some sensor companies provide the hardwares that support Apollo.
Baidu even proposed the ideas of Hardware Integration Platform and Apollo Vehicles Certifications. The ambition to become the Chinese standard is clear.

![number](/assets/img/bc-number.jpeg){:class="img-responsive"}
*The Statistics of the Apollo league*
<br />
<br />
Even though Baidu does not have the ability to produce it's own vehicles. It has the fast development pace and quick iterations on products. With Apollo, Baidu had established a self-driving league in one year. Even this league does not return cash directly to the company. It lays the foundation for the long term future.

![for-all](/assets/img/bc-for-all.jpg){:class="img-responsive"}
*The ambition of Baidu*
