Transductive CNAPS - Few-Shot Image Classification 

Python =>3.5, PyTorch =>1.10.0, TesnsorFlow 2.0


## Dependencies
You can use the ```requirements.txt``` file included to install dependencies for Transductive CNAPS on mini-ImageNet Dataset. To install all dependencies, run ```pip install -r requirements.txt```. 


## Mini/Tiered ImageNet Installations & Usage
In order to re-create these experiments, you need to:
1. Dataset - [mini-ImageNet](https://drive.google.com/file/d/1zh7HoZZgEjvobsuRWbrO3UvVEuaUPkXn/view?usp=sharing) place it in "processed_images" folder
2. Pre-trained Resnet [weights](https://drive.google.com/file/d/1LBXORVnGzXJLXPLeLE_6lpLedTAUzzJy/view?usp=sharing) place it in "pretrained_resnets" folder

2. Once the setup is complete, use ```run_transductive_cnaps_mt.py``` to run mini-imagenet experiments:
    
    ```cd src; python run_transductive_cnaps_mt.py --dataset mini --feature_adaptation film --checkpoint_dir <address of the directory where you want to save the checkpoints> --pretrained_resnet_path <choose pretrained_resnets folder>```



