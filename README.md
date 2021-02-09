# pysyft-test
我们这里演示安装syft==0.2.8,因为我只找到了基于0.2.8版本的syfertext，blog里说的0.2.5我没有找到

## 步骤
- [pysyft-test](#pysyft-test)
  - [步骤](#步骤)
  - [1.安装anconda](#1安装anconda)
  - [2.创建虚拟环境](#2创建虚拟环境)
  - [3.安装microsoft c++ build tool](#3安装microsoft-c-build-tool)
  - [4.安装pytorch](#4安装pytorch)


## 1.安装anconda

1.1[下载anaconda](https://www.anaconda.com/products/individual)
下载好后，一键安装即可

2.1设置环境变量
在path环境变量里添加anaconda安装目录的Scripts目录，比如说E:\anconda\Scripts。这是为了conda命令能够在cmd这样的终端中直接使用

## 2.创建虚拟环境
初始化
```
conda init  //执行后请关闭终端，重新启动
```

创建虚拟环境
```
conda create -n syft-test python==3.8
```
激活虚拟环境
```
conda activate syft-test
```
## 3.安装microsoft c++ build tool
python库有一些是用c++写的所以安装的时候需要编译c++
[下载](https://pan.baidu.com/s/1CeWqdAzQRqgyk4TpBahALw)一键安装即可

## 4.安装pytorch
这里是安装pytorch1.4.0,自己选择cpu或者gpu版安装

CPU版本
```
pip install torch===1.4.0+cpu torchvision===0.5.0+cpu -f https://download.pytorch.org/whl/torch_stable.html -i https://pypi.tuna.tsinghua.edu.cn/simple some-package
```

GPU版本
```
pip install torch===1.4.0 torchvision===0.5.0 -f https://download.pytorch.org/whl/torch_stable.html -i https://pypi.tuna.tsinghua.edu.cn/simple some-package
````

## 5.安装syft

### 5.1克隆代码
```
git clone git@github.com:OpenMined/PySyft.git
```

### 5.2切换分支并安装

切换分支并安装
```
cd pysyft   //进入项目目录
git chekcout v0.2.8  //切换分支
python setup.py install  //执行安装程序
```
最后显示安装成功即可

查看安装的syft包
```
pip list
```



