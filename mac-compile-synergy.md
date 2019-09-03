# Mac安装synergy

## 下载源码
````
git clone https://github.com/symless/synergy-core.git
````

## 安装依赖
brew的安装请自行百度。

````
brew install qt cmake
````

## 编译源码
````
cd Projects/synergy
mkdir build
cd build
QT_PATH=/usr/local/opt/qt
export PATH=$PATH:/usr/local/bin:$QT_PATH/bin
cmake  -DCMAKE_OSX_DEPLOYMENT_TARGET=10.10 -DCMAKE_OSX_ARCHITECTURES=x86_64 -DCMAKE_BUILD_TYPE=$CMAKE_BUILD_TYPE -DCMAKE_CONFIGURATION_TYPES=$CMAKE_BUILD_TYPE ..
make
sudo mae install
````