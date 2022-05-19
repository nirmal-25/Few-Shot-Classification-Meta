# Few-Shot Image Classification
Popular few-shot algorithms are trained on the mini-ImageNet dataset in both Euclidean and Non-Euclidean spaces. From our experiments we find that the non-Euclidean geometry has improved the results for some tasks as shown in the table below. Furthermore, the use of non-Euclidean space can improve the model performance where there are implicit hierarchical relations in the input. 

#### Experiments on the mini-ImageNet dataset
 - Transductive CNAPS
 - Model-Agnostic Meta Learning (MAML)
 - Matching Networks

```mini-ImageNet-1``` has implementations for MAML and Matching Networks, whereas ```mini-ImageNet-2-Transductive-CNAPS``` consists of the Transductive CNAPS implementation, in which we obtain the highest test accuracy of 71.4 % for 5-way 5-shot image classification using our non-Euclidean model. 


*5-Way 5-Shot Learning on mini-ImageNet Dataset*

<img src="https://user-images.githubusercontent.com/51696913/169417494-c8d3365b-3764-466f-a39b-f56a2b5ffb8e.png" width="600">

