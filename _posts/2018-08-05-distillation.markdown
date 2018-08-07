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

If the speed is the hard requirement, we can only pick the weak model for deployment.
[image]
It seems like having a strong but slower model does not benefit us in this scenario. But the Model Distillation shows a way to improve the weak model by **using the strong model as a teacher**. Even in the case not having a strong model, we can always build one by almighty ensebmle methods.


### **How Distillation Works?**
To distill a model, we firstly train a strong network as a techer for the next stage.
[image]
In second stage, we take the probabilities of predictions from the strong model as the second groudn truth. The weak network then combines the original loss and the extra **soft targets** loss from the techer network. 
loss =  classification_loss + soft_target_loss

You may wonder how does the soft target loss contributes to the learining. Let's find out in next section. 

### **Why Distillation Works?**
Imagine we are doing a image classification task with four classes: [Pedestrian, Dog, Car, truck].
Given an image of a car and a trained teacher model, we may get a prediction result like this:
[image][image]

As you can see, the model made the correct prediction on car, but still gives tiny probabilities on rest of the classes. These extra probabilities provide the **knowledge of generalization** we need. The relatively higher likelihood of the truck shows that cars are more similar to turcks than to pedestrian or dogs. This information provicde 
[image]
In order to extract these knowledges, Hinton introduces **Softmax with tempture** to replace the regular softmax. It works like softmax with a hyperparameter *T*. 
$$
Softmax Functions.
$$q_i = {exp(z_i) \over \sum_{j=1}^n exp(z_j)}$$
$$



$$
Distilling Version of Softmax where $T$ is the tempture.
$$q_i = {exp(z_i/T) \over \sum_{j=1}^n exp(z_j/T)}$$
$$

Higher temperture mitigates the difference among classes thus enlarge the hidden knowledge of generalization. By mimicing the teacher network, the student network learns the extra knwoledge of generalization that missing in ground truth.
[image]

### **Extra Readings**

Here is [a great tensorflow implementation](https://github.com/DushyantaDhyani/kdtf) of Model Distillation by Dushyanta Dhyani.

Since the publication of Model Distillation, tons of related works have been done. Distilation had become an important concept escecially in the field of Neural Network Compression. 
Please refer to the [Awesome Knowledge Distillation Collection](https://github.com/dkozlov/awesome-knowledge-distillation) for the awesome related works.



