# ublox
## インストール・ビルド
```ruby:インストール・ビルド
mkdir -p ~/ublox/src
cd ~/ublox/src
catkin_init_workspace

git clone https://github.com/KumarRobotics/ublox.git
git clone https://github.com/tilk/rtcm_msgs.git

cd ..
catkin_make
```
## 実行
### ttyACM0にアクセスする権限を与える
```
sudo su 
cd /
cd dev
chown $USER_NAME$ ttyACM0
```
### デバイス名を指定して実行
```
roslaunch ublox_gps ublox_device.launch param_file_name:=zed_f9p
```