# mpv播放器配置
在`mpv`所在目录下创建一个名为`portable_config`的文件夹，并在该文件下创建以下配置文件，以下为推荐配置。

`mpv.conf`
```conf
#开启缓存
cache=yes
#最大缓存大小（KiB或MiB）
demuxer-max-bytes=64MiB
#用内存而不是磁盘缓存
cache-on-disk=no

#自动加载外部字幕文件方式。（fuzzy加载同文件夹含有视频文件名的字幕文件）
sub-auto=fuzzy

#设置默认打开的窗口大小
geometry=60%x60%+50%+50%
#启动默认音量
volume=100
#程序最大音量
volume-max=100
```
