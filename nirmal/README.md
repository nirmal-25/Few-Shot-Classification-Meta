Install packages from requirements.txt (Anaconda env .yaml file is also given)

```
pip install -r requirements.txt
```

GPU is disabled for now (had some issues with CUDA toolkit and PyTorch versions)

Works for mini ImageNet - ProtoTypical networks, Meta Agnostic Meta Learning (MAML)

**Dataset** 

Download miniImageNet.zip from the [shared project drive](https://drive.google.com/file/d/1Jv6dyZiFZreCuox9TncdlQlANLN4eiiN/view?usp=sharing) unzip and place it in data/

There are 100 classes -  80 for train and 20 for test, folder names represent the classes

**Training** 

The model is defined in few_shot/models.py 

Model weights (.pth files) are saved in models/

To train models, experiments/experiments.txt has the list of commands that can be run

For example, from the root folder run,
```
python -m experiments.proto_nets --dataset miniImageNet --k-test 5 --n-test 5 --k-train 20 --n-train 5 --q-train 15
```

**Approach**
- ```dataset```: {'miniImageNet'}.
- ```distance```: {'l2', 'cosine'}. Which distance metric to use
- ```n-train```: Support samples per class for training tasks
- ```n-test```: Support samples per class for validation tasks
- ```k-train```: Number of classes in training tasks
- ```k-test```: Number of classes in validation tasks
- ```q-train```: Query samples per class for training tasks
- ```q-test```: Query samples per class for validation tasks


Modified from this [GitHub repo](https://github.com/Shandilya21/Few-Shot)
