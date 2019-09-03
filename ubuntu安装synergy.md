# ubuntu安装synergy
## 下载源码
````
git clone https://github.com/symless/synergy-core.git
````

## 安装依赖
````
sudo apt install qtcreator qtbase5-dev cmake make g++ xorg-dev libssl-dev libx11-dev libsodium-dev libgl1-mesa-glx libegl1-mesa libcurl4-openssl-dev libavahi-compat-libdnssd-dev qtdeclarative5-dev libqt5svg5-dev libsystemd-dev
````

## 添加boost根目录
编辑源码目录下文件`Build.properties`,添加如下内容：
````
#BOOST_ROOT=/home/<user>/boost
BOOST_ROOT=/home/pingan/boost
````

## 编译源码
````
cd Projects/synergy
mkdir build
cd build
cmake ..
make
sudo mae install
````

### 关闭防火墙
如果ubuntu做为服务端，需要关闭防火墙或者打开相应的端口24800。
````
# 打开24800端口
sudo ufw allow 24800/tcp
# 关闭防火墙
sudo ufw disable
````