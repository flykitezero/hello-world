720p数据保存在data_train_720和data_test_720文件夹下，分别代表训练集和测试集。
开始训练数据：
```python
python train.py -c config_720.json

```
完成训练后，会输出一行模型的保存路径，例如：
```python
Saving checkpoint: saved/models/NSRR-Pytorch/1113_011125/checkpoint-epoch400.pth ..
```
将该路径替换至test.py中的相对位置：
```python
checkpoint = torch.load('./saved/models/NSRR-Pytorch/1113_011125/checkpoint-epoch400.pth')
```
之后就可以进行测试，输入如下命令：
```python
python test.py -c config_test_720.json

```
完成后会输出test数据的平均loss和平均SSIM，输出的图片会保存在output_720文件夹中，包含输入和输出图片。
