# OpenCV-Mac
OpenCV-Mac
####步骤：
第一步：新建项目（Mac OS->Command Line Tools）
        
![](https://upload-images.jianshu.io/upload_images/2229471-cc9b6fb3462e4e09.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
注意：选择C++语言
![](https://upload-images.jianshu.io/upload_images/2229471-5ca7013b04ea8c2b.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
第二步：在项目build setting->search path进行配置
        Always search User paths : true
        Framework search path: /usr/local/lib
        Header Search Paths ：/usr/local/include
        Library Search Paths ： /usr/local/lib
![](https://upload-images.jianshu.io/upload_images/2229471-afaf0f1ccd9a62a5.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![](https://upload-images.jianshu.io/upload_images/2229471-af8d973c4254c307.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![](https://upload-images.jianshu.io/upload_images/2229471-a032ceb169e07648.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![](https://upload-images.jianshu.io/upload_images/2229471-2236b4249628b782.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![](https://upload-images.jianshu.io/upload_images/2229471-7b7854a428dc9132.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![](https://upload-images.jianshu.io/upload_images/2229471-12bd73172439e39a.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

'opencv2/core/core.hpp' file not found
在项目中右键Add Files To “xxx”，选择opencv2.framework，选择左下角Options，勾选Destination： Copy items if needed，添加后错误解决。

#二、iOS环境配置
在Mac环境配置好的前提下！
1、创建iOS工程
![](https://upload-images.jianshu.io/upload_images/2229471-9c47361304cf178a.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
2、添加OpenCV库opencv2.framework，Add Files to “”
![](https://upload-images.jianshu.io/upload_images/2229471-7ae91f61c0132e24.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![](https://upload-images.jianshu.io/upload_images/2229471-3efbbaaf29fd4862.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

3、创建一个OpenCV处理图片工具类，并把工具类的.m文件和用到工具类的地方的.m文件改为.mm，支持c++编程
![](https://upload-images.jianshu.io/upload_images/2229471-7d58a7ee1ef5f2bb.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

[Demo下载]()
