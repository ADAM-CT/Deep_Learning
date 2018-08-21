### GAN与DCGAN

代码环境 windows10 + python3.6 + tensorflow 1.4.0

**1 生成MNIST图像**

下载MNIST数据集：
```
python download.py mnist
```

训练：
```
python main.py --dataset mnist --input_height=28 --output_height=28 --train
```

生成图像保存在samples文件夹中。

**2 使用自己的数据集训练**

在数据目录data/中已经准备好了一个动漫人物头像数据集。在源代码的data目录中再新建一个anime目录（如果没有data 目录可以自行新建）。

训练命令：
```
python main.py --input_height 96 --input_width 96 \
  --output_height 48 --output_width 48 \
  --dataset anime --crop -–train \
  --epoch 300 --input_fname_pattern "*.jpg"
```

生成图像保存在samples文件夹中。
