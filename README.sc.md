# neural_style

[![AppVeyor](https://img.shields.io/badge/Language-EN-brightgreen.svg)](https://github.com/Wanguy/neural_style/blob/master/README.sc.md)[English Documentation](https://github.com/Wanguy/neural_style/blob/master/README.md)

在TensorFlow中实现 [neural style](http://arxiv.org/pdf/1508.06576v2.pdf)。

TensorFlow 不支持 [L-BFGS](https://en.wikipedia.org/wiki/Limited-memory_BFGS)（原作者使用的），所以我们使用[Adam](http://arxiv.org/abs/1412.6980)。为了获得更好的效果，需要对更多的一些参数进行调整。

## 相关项目

在[这里](https://github.com/lengstrom/fast-style-transfer)可以看到TensorFlow 中快速（前馈）神经样式（ [fast (feed-forward) neural style](https://arxiv.org/pdf/1603.08155v1.pdf)）的实现。

## 要求

### 数据文件

- [经过预先训练的VGG网络](https://github.com/fchollet/deep-learning-models/releases/download/v0.1/vgg16_weights_tf_dim_ordering_tf_kernels_notop.h5)（vgg16_weights_tf_dim_ordering_tf_kernels_notop.h5），将其放在根目录`/Users/YOURNAME/.keras/models`下，或使用`--network`选项指定其位置。

### 依赖

你可以通过`pip install -r requirements.txt`来安装相关的依赖，或是手动安装下列的包：

- [TensorFlow](https://www.tensorflow.org/versions/master/get_started/os_setup.html#download-and-setup)
- [H5PY](http://www.h5py.org/)
- [Pillow](http://pillow.readthedocs.io/en/3.3.x/installation.html#installation)
- [Kera](https://keras-cn.readthedocs.io/en/latest/)

## 运行

`python neural_style_transfer.py "<目标文件>" "<模板文件>" "<输出文件>"`

> `<输出文件>` 不需要写扩展名。

通过 `python neural_style.py --help` 查看所有的控制选项。

使用 `--checkpoint-output` 和 `--checkpoint-iterations` 保存检查点图像。

## 许可

Copyright (c) 2015-2017 Wanguy. Released under GPLv3. See [LICENSE.txt](https://github.com/Wanguy/neural_style/blob/master/LICENSE) for details.