## install xfce4 and tigervnc-server
```
sudo apt install xfce4 xfce4-goodies
download https://bintray.com/tigervnc/stable/download_file?file_path=ubuntu-16.04LTS%2Famd64%2Ftigervncserver_1.7.0-1ubuntu1_amd64.deb

sudo dpkg -i tigervncserver_filename.deb
sudo apt-get install -f
vncserver
```

中间可能出现错误如：
>https://hk.saowen.com/a/535d93670eec3d6853da04992102cad14b105e0e01e7f93315dfd32d7db96b42
Could not connect to session bus:
Failed to connect to socket /tmp/dbus-XXXXXXXXXX:
Connection refused

修復方法
```
因為無法登陸圖形界面, 所以在ssh下修復, 具體方法如下:

登陸ssh, 關閉自己開啟的vncserver進程

備份~文檔夾下重要的隱藏文檔, 如.bashrc文檔

cp ~/.bashrc ~/bashrc.bak
刪除~文檔夾下所有隱藏文檔

rm -rf ~/.*
輸入exit註銷賬户, 再重新登陸ssh

重置~文檔夾下的默認配置文檔

cp -r /etc/skel/. /home/usrname
輸入exit註銷賬户, 再重新登陸ssh
```

> 登陆黑屏，可能是有另外一个会话存在，重启，只通过vnc桌面登陆


