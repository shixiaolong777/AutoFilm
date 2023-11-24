# AutoFilm-推荐使用jellyfin
**一个为Emby、Jellyfin服务器提供直链播放的小项目**

利用Nastools或moviepliot对alist挂载的阿里云盘、Onedrive等可以使用302重定向的网盘进行重命名和刮削

## 优点
- [x] 轻量化Emby服务器，降低Emby服务器的性能需求以及硬盘需求
- [x] 运行稳定
- [x] 相比直接访问Webdav，Emby、Jellyfin服务器可以提供更好的视频搜索功能以及自带刮削器，以及多设备同步播放进度
- [x] 提高访问速度，播放速度不受Jellyfin服务器带宽限制
## TODO LIST
- [x] Github Workflows自动下载打包上传至Release
- [x] 从config文件中读取多个参数
- [ ] 优化程序运行效率
- [ ] 对接TMDB实现分类、重命名、刮削等功能


使用步骤
例：python3 .\autofilm.py --webdav_url https://alist.example.com:666/dav/视频/动漫/ --username myAlist --password Alistpwd  --output_path D:电影//动漫//

必要参数
webdav_url：webdav服务器地址
username：webdav账号
password：webdav密码

非必要参数
output_path：输出文件目录，默认为当前文件夹的子目录Media
subtitle：是否下载字幕文件，默认true
nfo：是否下载NFO文件，默认false
img：是否下载JPG和PNG图片文件，默认 false
