



### Ubuntu Chrome无法播放视频，需要安装flashplayer

1、到https://get.adobe.com/cn/flashplayer/?no_redirect 下载tar.gz（flash_player_ppapi_linux.x86_64.tar.gz）



2、到`$HOME/.config/google-chrome/PepperFlash/`目录下创建一个Chrome版本号文件夹（例如56.0.2924.87）



 ![mkdir](imgs/mkdir.png)



3、把tar.gz解压之后的文件放到版本号文件夹

 ![copyfile](imgs/copyfile.png)



4、修改chrome的desktop文件

 `sudo gedit /usr/share/applications/google-chrome.desktop`

 把Exec部分修改成如下内容，注意两处版本号

```
Exec=/usr/bin/google-chrome-stable %U --ppapi-flash-path=$HOME/.config/google-chrome/PepperFlash/56.0.2924.87/libpepflashplayer.so --ppapi-flash-version=56.0.2924.87
```

 ![gedit](imgs/gedit.png)



5、重启Chrome浏览器