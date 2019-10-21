# MLPractice
Repositories  for machine learning 

- pytorch_fasterrcnn_detection
 该文件夹内容实现了使用torchvision自带的fasterrcnn模型来训练Pascal Voc, Coco和**Pascal格式的自定义数据集**
  - 训练命令:
  `$ python3 train.py --dataset custom_voc --train-data-path /home/gaoya/Documents/quexianjiance/GAN.NO2/train_GAN_twoclass --test-data-path /home/gaoya/Documents/quexianjiance/testGAN_twoclass_clear_all -b 2 --output-dir ./checkpoints`
  - 测试命令:
  `$ python3 train.py --dataset custom_voc --test-only --train-data-path /home/gaoya/Documents/quexianjiance/GAN.NO2/train_GAN_twoclass --test-data-path /home/gaoya/Documents/quexianjiance/testGAN_twoclass_clear_all --resume model_custom_voc_11.pth`
  
    注意上面参数--resume的作用是用于模型推理
