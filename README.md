# Linux-常用命令

shadowsock启用
```
./root/ssr.sh
```
编译.so文件
```
gcc -std=c99 -o lic.so -shared -fPIC LIC.c
```
查看后台python进程
```
ps -ef|grep py
jobs
```
# CMAKE

指定package路径
```
set(OpenCV_ROOT "/usr/local/opencv2.0/build")

set(OpenCV_DIR "/usr/local/opencv3.0/build")

find_package(OpenCV REQUIRED
              NO_MODULE # should be optional, tells CMake to use config mode
              PATHS /usr/local # look here
              NO_DEFAULT_PATH) # and don't look anywhere else
```
OpenCV_ROOT设定后，find_package()的config模式会在OpenCV_ROOT目录及其子目录下寻找cmake的config文件；

而设定Open_DIR则很傻，不会在子目录中寻找，是config模式特有的缓存变量。

如果定义了DIR，则ROOT不起作用，使用3.0
