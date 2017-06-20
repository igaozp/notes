```
// 创建字体目录
sudo mkdir /usr/share/fonts/oh-my-fonts 
// 将下载的字体复制到相应的目录
sudo cp 存放字体的目录/*  /usr/share/fonts/oh-my-fonts 
// 修改字体目录权限
sudo chmod 644 /usr/share/fonts/oh-my-fonts/* 
cd /usr/share/fonts/oh-my-fonts 
// 建立字体缓存
sudo mkfontscale
sudo mkfontdir
sudo fc-cache -fv
```
