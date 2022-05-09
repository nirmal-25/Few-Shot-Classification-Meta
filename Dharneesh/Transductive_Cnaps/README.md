# Enhancing Few-Shot Image Classification with Unlabelled Examples

Python =>3.5, PyTorch =>1.10.0, TesnsorFlow 2.0


## Dependencies
You can use the ```requirements.txt``` file included to install dependencies for Transductive CNAPS on mini-ImageNet Dataset. To install all dependencies, run ```pip install -r requirements.txt```. 


## Mini/Tiered ImageNet Installations & Usage
In order to re-create these experiments, you need to:
1. Dataset - [mini-ImageNet] (https://drive.google.com/file/d/1zh7HoZZgEjvobsuRWbrO3UvVEuaUPkXn/view?usp=sharing) place it in "processed_images" folder
2. Pre-trained Resnet weights (https://drive.google.com/file/d/1LBXORVnGzXJLXPLeLE_6lpLedTAUzzJy/view?usp=sharing) place it in "pretrained_resnets" folder
1. First clone https://github.com/yaoyao-liu/mini-imagenet-tools, the mini-imagenet tools package used for generating tasks, and https://github.com/yaoyao-liu/tiered-imagenet-tools, the respective tiered-imagenet tools package under ```/transductive-cnaps-src```. Although theoretically this should sufficient, there may be errors arising from hard coded file paths (3 to 4 of which was present at the time of creating our set-up, although they seem to have been resolved since) which you can easily fix. Alternatively, we have included tested copies of both of these repositories within this director (see [miniimagenettools](https://github.com/plai-group/simple-cnaps/tree/master/transductive-cnaps-src/miniimagenettools/)

2. Once the setup is complete, use ```run_transductive_cnaps_mt.py``` to run mini\tiered-imagenet experiments:
    
    ```cd src; python run_transductive_cnaps_mt.py --dataset <choose either mini or tiered> --feature_adaptation film --checkpoint_dir <address of the directory where you want to save the checkpoints> --pretrained_resnet_path <choose resnet pretrained checkpoint>```



