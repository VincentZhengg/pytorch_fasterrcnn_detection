# MLPractice
Repositories  for machine learning 

- pytorch_fasterrcnn_detection
 该文件夹内容实现了使用torchvision自带的fasterrcnn模型来训练Pascal Voc, Coco和**Pascal格式的自定义数据集**,参考项目地址为:https://github.com/lpuglia/torchvision_voc, 主要在原项目基础上增加对自定义数据集的支持
  - 训练命令:
  `$ python3 train.py --dataset custom_voc --train-data-path /path/to/train --test-data-path /path/to/test -b 2 --output-dir ./checkpoints`
  注意训练集路径和测试集路径下的文件夹名称要和Pascal Voc数据集一致(具体原因可以查看源码)
  - 测试命令:
  `$ python3 train.py --dataset custom_voc --test-only --train-data-path /path/to/train --test-data-path /path/to/test --resume model_custom_voc_11.pth`
  
    注意上面参数--resume的作用是用于模型推理,原项目只提到了该参数用于恢复训练,但是查看pytorch官网对模型load_state_dict方法介绍可知该参数的作用亦用于模型推理(具体实现查看源码)
