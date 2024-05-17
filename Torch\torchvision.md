# torch、torchvision安装
- 在nvidia官网找到自己jetpack版本对应的torch版本（我的jetpack版本是5.0.1）
    + https://forums.developer.nvidia.com/t/pytorch-for-jetson/72048  
- 下载下来离线pip安装（我用cuda13，安装torch1.11.0和1.12.0都会出现版本不匹配；随后换了cuda14，可以完美匹配torch12）
  + 安装之前记得检查虚拟环境中的torch是否删除干净
  + 最新版本的torch和GPU不兼容，无法使用cuda加速
- 按照torch版本找对应的torchvision
  + 在这个地址找https://github.com/pytorch/vision
  + 按照tag找对应的版本
  + 下载下来之后记得**把整个文件夹的名子改成trochvision**
- cd进入torchvision文件夹
- 添加这一行命令export BUILD_VERSION=0.13.0（虽然我也不知道这是干嘛用的）
- python3 setup.py install --user（这一步会有很多警告，只要没报错，直接无视）
- 到这就可以完美使用torch和torchvision跑cv应用了

  

