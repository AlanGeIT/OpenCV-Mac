# Mac配置OpenCV环境
## 第一步：下载OpenCV开发包（Mac环境）
下载地址：http://opencv.org
## 第二步：安装Homebrew
    安装文档地址：http://brew.sh/index_zh-cn.html
    
## 第三步：安装CMake（安装好Homebrew之后，可以执行以下命令安装）
    CMake是什么：是一个跨平台编译工具
    第一种安装方式：下载安装（推荐使用下载安装）
        下载官方：https://cmake.org/download/
    第二种安装方式：执行命令安装（但是需求提前安装Homebrew）
        brew install cmake
## 第四步：安装OpenCV
    1. 进入下载OpenCV解压之后的文件夹
    2. 执行命令（依次执行以下命令进行安装）
        命令一：mkdir build
        命令二：cd build
        命令三：cmake -G "Unix Makefiles" ..
        命令四：make
        命令五：sudo make install
    3. 执行完命令，OpenCV安装完成
    4. 检查：command + shift + g 到/usr/local/lib目录下查看是有OpenCV库文件
    

## 第五步：新建项目测试
    1、新建项目（Mac OS->Command Line Tools）
        注意：选择C++语言
    2、在项目build setting->search path进行配置
        Always search User paths : true
        Framework search path: /usr/local/lib
        Header Search Paths ：/usr/local/include
        Library Search Paths ： /usr/local/lib
    
    3、在项目中新建一个文件夹，选"Add files to ..."，按 command+shift+g 输入路径 /usr/local/lib，把所有的dylib库导入项目
    4、测试运行，以下为测试Demo（直接Copy代码运行）
    
    #include <opencv2/core/core.hpp>
    #include <opencv2/imgcodecs.hpp>
    #include <opencv2/highgui/highgui.hpp>
    #include <iostream>
    #include <string>
    
    using namespace cv;
    using namespace std;
    
    int main( int argc, char** argv ){
        string imageName("/Users/yangshaohong/Desktop/2.jpg"); // by default
        if( argc > 1) {
            imageName = argv[1];
        }
        Mat image;
        image = imread(imageName.c_str(), IMREAD_COLOR); // Read the file
        if( image.empty() ){
            cout <<  "Could not open or find the image" << std::endl ;
            return -1;
        }
        namedWindow( "Display window", WINDOW_AUTOSIZE ); 
        imshow( "Display window", image );                
        waitKey(0); 
    
        return 0;
    }

[Demo下载](https://pan.baidu.com/s/1fyjs1cF0OjbcTV0vu7YCXQ)提取码: mxuw
