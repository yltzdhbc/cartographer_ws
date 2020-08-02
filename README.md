# cartographer_ws

# 2020.08.02
国内安装cartographer十分困难，因此我将其下载放入工作空间中

兼容：已经测试: Ubuntu16.04+Kinetic

使用方法：下载or克隆到朱目录下
```sheel
cd ~
```
## 1.国外：Github
```sheel
git clone https://github.com/yltzdhbc/cartographer_ws.git
```
## 1.国内：Gitee
```sheel
git clone https://gitee.com/yltzdhbc/cartographer_ws.git
```
## 2.然后进入工作工作空间编译
```sheel
cd ~/cartographer_ws
catkin_make_isolated --install --use-ninja
```
## 3.声明工作空间
```sheel
echo "source ~/cartographer_ws/install_isolated/setup.bash" >> ~/.bashrc
```
## 4.测试 下载bag运行
```sheel
wget -P ~/Downloads https://storage.googleapis.com/cartographer-public-data/bags/backpack_2d/cartographer_paper_deutsches_museum.bag
```
```sheel
roslaunch cartographer_ros demo_backpack_2d.launch bag_filename:=${HOME}/Downloads/cartographer_paper_deutsches_museum.bag
```
## 5.如果能运行则安装成功
## 6.enjoy!
