# NoteForNvidiaDriver
## 从头开始安装
* 参考过程：https://blog.csdn.net/qq_45848817/article/details/117987514
** 注意，有两个bug。
  *** fix1: sudo chmod NVIDIA*.run --> sudo chmod 777 NVIDIA*.run
  *** 不要输入-no-opengl-files

## 因自动更新而导致的挂在失败
直接从“正式安装”这一步开始

## Gazebo无GPU的原因
1. 查看是否是显卡驱动安装时指定了参数--no-opengl-files
2. sudo systemctl set-default graphical.target

ref: https://blog.csdn.net/qq_38853759/article/details/132522471
