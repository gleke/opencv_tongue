# opencv_tongue
使用opnccv做中医舌诊视频、图像诊断的研究

## 安装方法，基于macos 
mac版本`macOS 10.12.4 (16E195)`

### 下载opencv

### 编译安装opencv
```

```

## 执行方法

### 命令行编辑 
```
g++ colorim.cpp `pkg-config opencv --libs --cflags opencv` -o colorim
g++ <cpp文件名> `pkg-config opencv --libs --cflags opencv` -o <输出的文件>
```

### 使用make
CMakeLists.txt
```
PROJECT(Helloworld)          
# 这是建立一个工程项目（类似于我们VS中建立C++项目一样），括号里面时工程名,工程名我们可以任意给，最后程序编译出来的可执行文件就是这个名字

CMAKE_MINIMUM_REQUIRED(VERSION 2.6)
# 这是对CMake工具最低版本要求，这里我们要检查下我们的CMake工具的版本信息，我们可以使用命令“cmake --version”查看
if(COMMAND cmake_policy)
      cmake_policy(SET CMP0003 NEW)
endif(COMMAND cmake_policy)
 
FIND_PACKAGE( OpenCV REQUIRED )
# 这是cmake用来查找opencv包用的，不用改

# Declare the target (an executable)
ADD_EXECUTABLE(Helloworld  drawing.cpp)
# 这里括号里面的两个参数分别是工程项目名和我们要编译文件名的意思，记住中间一空格键隔开

TARGET_LINK_LIBRARIES(Helloworld ${OpenCV_LIBS})
# 这是我们链接到OpenCV库的环节，我们只要更改前面第一个参数位我们的工程项目名即可

MESSAGE(STATUS "OpenCV_LIBS: ${OpenCV_LIBS}")
# 好了，就修改这么点东西，保存，关闭。
```
执行命令
```
cmake .
make
```

# 参考书籍
《学习Opencv》清华大学


# TODO
* 做cpp批量编辑的shell
* 中文乱码
