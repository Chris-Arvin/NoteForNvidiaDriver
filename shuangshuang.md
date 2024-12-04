## 因自动更新而导致的挂在失败
直接从“正式安装”这一步开始
1. ctrl+alt+F3 : arvin, a
2. cd Documents
3. sudo ./NVIDIA-Linux-x86_64-***.**.run –no-x-check -no-nouveau-check
4. 输入密码：a，然后会车
5. 除了“32-lib” 和 “would you like to run the nvidia-xconfig utility to **automatically update** ...”之外，其实都yes
6. ctrl+alt+F2
7. 重启电脑



## Gazebo无GPU的原因
1. 查看是否是显卡驱动安装时指定了参数--no-opengl-files
2. sudo systemctl set-default graphical.target

ref: https://blog.csdn.net/qq_38853759/article/details/132522471
