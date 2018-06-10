[TOC]



### Ubuntu Chrome无法播放视频，需要安装flashplayer

1、到https://get.adobe.com/cn/flashplayer/?no_redirect 下载tar.gz（flash_player_ppapi_linux.x86_64.tar.gz）



2、到`$HOME/.config/google-chrome/PepperFlash/`目录下创建一个Chrome版本号文件夹（例如56.0.2924.87）



 ![mkdir](imgs/mkdir.png)



3、把tar.gz解压之后的文件放到版本号文件夹

 ![copyfile](imgs/copyfile.png)



4、修改chrome的desktop文件

 `sudo gedit /usr/share/applications/google-chrome.desktop`

 把Exec部分修改成如下内容，注意`/home/jh`改为自己的，且不能使用`$HOME`，两处版本号与前面创建文件夹一致。

```
Exec=/usr/bin/google-chrome-stable %U --ppapi-flash-path=/home/jh/.config/google-chrome/PepperFlash/56.0.2924.87/libpepflashplayer.so --ppapi-flash-version=56.0.2924.87
```

 ![gedit](imgs/gedit.png)



5、重启Chrome浏览器





### 使用GIMP去除水印

视频演示：http://www.uupoop.com/help/12535.html

1.打开一张图片 
2.选择图章工具，鼠标移到图片上。 
3.按住Ctrl键，点击鼠标选择复制源点，选择合适的源点很 重要。 
4.松开Ctrl键，点击水印，这时源点就被复制到水印上盖住 水印了。 
5.重复3和4步骤，把水印慢慢覆盖。如果点错了，可以在历史记录里返回上一步。

 ![Screenshot from 2018-06-11 01:01:35](imgs/Screenshot.png)

另外，

1、如果工具栏不见了，在Windows菜单下面新建一个toolbox（New ToolBox）

2、GIMP默认保存的是cfx格式，如果需要png或者jpg格式，需要导出（Export）







