| 第四届计图挑战热身赛

# Jittor 手写数字生成赛题 baseline
本赛道将在数字图片数据集 MNIST 上训练 Conditional GAN（Conditional generative adversarial nets）模型，通过输入一个随机向量 z 和额外的辅助信息 y (如类别标签)，生成比赛 ID 图像

![主要结果](result.png)

｜展示方法的流程特点或者主要结果等

## 简介
| 简单介绍项目背景、项目特点

本项目包含了第四届计图挑战热身赛计图 - 手写数字生成赛题的代码实现。本项目的特点是：采用了 CGAN 方法对 MNIST数字图片数据集 进行了训练和处理，提交结果置信度 0.9998。

## 安装 
| 介绍基本的硬件需求、运行环境、依赖安装方法

本项目可在 1 张 3090 上运行，训练时间约为 1 小时。


#### 运行环境
- ubuntu 20.04 LTS
- python >= 3.7（我使用的是python3.8）
- jittor >= 1.3.0

#### 安装依赖
执行以下命令安装 python 依赖
```
pip install -r requirements.txt
```
(有关 jittor 的安装请参考 [jittor 官网](https://cg.cs.tsinghua.edu.cn/jittor/download/))

#### 预训练模型

已经附加在项目中，名称为`generator_last.pkl`和 `discriminator_last.pkl` ,放入与 `CGAN.py` 同级文件中即可。


## 训练
｜ 介绍模型训练的方法

单卡训练可运行以下命令：
```
python train.py
```

## 推理
｜ 介绍模型推理、测试、或者评估的方法

生成测试集上的结果可以运行以下命令：

```
python test.py
```

## 致谢
| 对参考的论文、开源库予以致谢，可选

此项目基于论文 *A Style-Based Generator Architecture for Generative Adversarial Networks* 实现，代码模板由 jittor 提供，相关代码可参考 [jittor-gan](https://github.com/Jittor/gan-jittor)。

## 注意事项

点击项目的“设置”，在Description一栏中添加项目描述，需要包含“jittor”字样。同时在Topics中需要添加jittor。

![image-20220419164035639](https://s3.bmp.ovh/imgs/2022/04/19/6a3aa627eab5f159.png)