Install packages from requirements.txt (Anaconda env .yaml file is also given)

```
pip install -r requirements.txt
```

Works for mini-ImageNet - ProtoTypical networks, Meta Agnostic Meta Learning (MAML). This repo assumes that you already have PyTorch-gpu set up.

**Dataset** 

Download ```miniImageNet.zip``` from this [link](https://drive.google.com/file/d/1Jv6dyZiFZreCuox9TncdlQlANLN4eiiN/view?usp=sharing), unzip and place it in ```data/```

There are 100 classes -  80 for train and 20 for test, folder names represent the classes

**Training** 

The model is defined in ```few_shot/models.py``` 

Model weights (.pth files) are saved in ```models/```

To train models, ```experiments/experiments.txt``` has the list of commands that can be run

For example, from the root folder run,
```
python -m experiments.proto_nets --dataset miniImageNet --k-test 5 --n-test 5 --k-train 20 --n-train 5 --q-train 15
```

**Approach**
- ```dataset```: {'miniImageNet'}.
- ```distance```: {'l2'}. Which distance metric to use (l2 - Euclidean)
- ```n-train```: Support samples per class for training tasks
- ```n-test```: Support samples per class for validation tasks
- ```k-train```: Number of classes in training tasks
- ```k-test```: Number of classes in validation tasks
- ```q-train```: Query samples per class for training tasks
- ```q-test```: Query samples per class for validation tasks

**Non-Euclidean**

For changes in the Non-Euclidean space, check ```models.py```

**References**

[1] [Few-Shot Algorithms](https://github.com/oscarknagg/few-shot)

[2] [FashionNet Few-Shot Implementation](https://github.com/Shandilya21/Few-Shot)

[3] [Non-Euclidean Library](https://github.com/mctorch/mctorch)

