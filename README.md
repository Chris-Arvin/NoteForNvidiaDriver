# NoteForNvidiaDriver
## 从头开始安装
* 参考过程：https://blog.csdn.net/qq_45848817/article/details/117987514
** 注意，有两个bug。
  *** fix1: sudo chmod NVIDIA*.run --> sudo chmod 777 NVIDIA*.run
  *** 不要输入-no-opengl-files

## 因自动更新而导致的挂在失败
直接从“正式安装”这一步开始
1. ctrl+alt+F3 : arvin, a
2. cd Documents
3. sudo chmod NVIDIA*.run
4. sudo ./NVIDIA-Linux-x86_64-***.**.run –no-x-check -no-nouveau-check
5. 除了32位lib 和 automatically update之外，其实都yes
6. ctrl+alt+F2
7. 重启电脑，打开一个新的终端，输入：nvidia-smi，查看是否有内容



## Gazebo无GPU的原因
1. 查看是否是显卡驱动安装时指定了参数--no-opengl-files
2. sudo systemctl set-default graphical.target

ref: https://blog.csdn.net/qq_38853759/article/details/132522471

##### 3. ==An alternative way to force Gazebo to use Nvidia Graphic Card [It works when nvidia-smi works well but OpenGL is not Nvidia card!!]==:
```bash
export __NV_PRIME_RENDER_OFFLOAD=1
export __GLX_VENDOR_LIBRARY_NAME=nvidia
exec gazebo
```
