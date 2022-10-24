# burp-wildcard



## 更新记录

1. 基于wildcard1.0.7简单修改，支持burp2020.11.2及后续的版本主题。
2. 基于wildcard1.0.8简单修改，解决2022.3.9等高版本上,显示布局混乱问题。(关于无法点击左边的标签问题, 未成功测试，需用户自行测试)

# release文件介绍

- wildcard-1.07.fix.1.jdk8.jar   基于1.0.7版本修改,支持版本至burp2022.3，使用jdk8打包, 可忽略

- wildcard-1.07.fix.src.zip 为对应源码文件, 可忽略

  

- 
  wildcard-1.08.fix.1.jdk8.jar  基于1.0.8版本修改，使用源码自带burp API文件，使用jdk8打包，支持版本至burp2022.X
  
- wildcard-1.08.fix.1.jdk11.jar  基于1.0.8版本修改，使用源码自带burp API文件，使用jdk11打包，支持版本至burp2022.X

- wildcard-1.08.fix.1.src.zip  为对应源码文件, 可忽略

  

- wildcard-1.08.fix.2.jdk8.jar  基于1.0.8版本修改，使用2022.3.9版本下导出的burp API文件，使用jdk8打包，支持版本至burp2022.X

- wildcard-1.08.fix.2.jdk11.jar  基于1.0.8版本修改，使用2022.3.9版本下导出的burp API文件，使用jdk11打包，支持版本至burp2022.X

- wildcard-1.08.fix.2.src.zip  为对应源码文件, 可忽略







# wildcard插件介绍

github  hvqzao/burp-wildcard:  https://github.com/hvqzao/burp-wildcard

1、此扩展程序试图解决(插件标签太多会使界面冗余难看)的问题

2、如果启用主题不兼容此扩展，则程序将自动关闭。

3、待所有插件加载完毕后，您可以使用本插件压缩所有插件标签。

4、为避免错误,建议将本wildcard插件移动到插件列表的最下方，wildcard将会被最后加载。

5、出于安全原因,每次加载本扩展程序时，需要显式启用此功能,允许保存为自动压缩。



# BUG记录

### 2022版本布局混乱BUG

![image](https://user-images.githubusercontent.com/46115146/177313557-31d24ba5-fde2-4453-a35e-7117701ae252.png)

高版本burpsuite上布局混乱  如 2022.3.9，通过删除无用的标签语句进行初步修复。



### Burp新版无法加载wildcard：

1、burpsuite官方开放的扩展管理API默认只支持Nimbus主题，与其他主题不兼容。

2、wildcard是基于API默认开发的，载入时会判断是否处于Nimbus主题内，如果不是当退出插件。

3、由于2020.11.2及以上版本没有Nimbus主题，只有统一的Light主题，和Dark主题，导致wildcard插件仅支持至burp 2020.11.1及以下版本，不支持burp 2020.11.2

4、唯一的好消息是, Light和Dark主题是基于Nimbus主题进阶的，只要修修源码就能重用在这两个主题上。

代码修改点 burp-wildcard-plus\src\hvqzao\wildcard\WildcardExtension.java  line 45,51

具体修改及编译教程查看： https://mp.weixin.qq.com/s/gDlGZLbufUTMXQ7IxMX0iQ




