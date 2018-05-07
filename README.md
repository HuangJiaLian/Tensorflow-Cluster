# Tensorflow-Cluster

Tensorflow Cluster 环境搭建

### 安装xubuntu-desktop

```
sudo apt-get install xubuntu-desktop
```

### 创建新用户

```
adduser dell01
usermod -aG sudo dell01
su - dell01
```

### ibus拼音输入法你好，显示你哈

- 面板右键首选项选择双拼，重启，选全拼，再重启

### 代理

```
sudo apt install python-pip python-setuptools
sudo pip install shadowsocks 
sslocal -s IPADDRESS -p 8388 -l 1080 -k "passwd" -t 600 -m aes-256-cfb &
添加到应用程序自启动
firefox安装switchomega 
chrome 安装switchomega: github.com/FelisCatus/SwitchyOmega/releases
chrome://extensions
```

### chrome网页版微信

### 安装 Cuda 9.0 

```
sudo dpkg -i cuda-repo-ubuntu1604-9-0-local_9.0.176-1_amd64.deb
sudo apt-key add /var/cuda-repo-9-0-local/7fa2af80.pub
sudo apt-get update
sudo apt-get install cuda-9-0
```
Download cuDNN: Download cuDNN v7.1.3 (April 17, 2018), for CUDA 9.0
cuDNN v7.1.3 Runtime Library for Ubuntu16.04 (Deb)

export PATH=/usr/local/cuda-9.0/bin${PATH:+:${PATH}}
export LD_LIBRARY_PATH=/usr/local/cuda-9.0/lib64${LD_LIBRARY_PATH:+:${LD_LIBRARY_PATH}}

Double Click libcudnn7_7.1.3.16-1+cuda9.0_amd64.deb to install 

export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/usr/local/cuda/extras/CUPTI/lib64

提示：这三个export最好要写入到.bashrc里面去。

### 安装 anocaonda 

sudo apt-get install python3-pip python3-dev python-virtualenv
cd ~
mkdir tf
virtualenv --system-site-packages -p python3 ~/tf
source ~/tf/bin/activate
easy_install -U pip
pip3 install --upgrade tensorflow-gpu
pip3 install opencv-python



待做事项：

- [ ] Tensorflow Distrubuted
- [ ] 安装词典dict
- [x] 安装Pycharm