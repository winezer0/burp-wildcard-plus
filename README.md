# wildcard 维护分支



## 更新记录

##### 文件下载

```
release文件夹
```

##### 顽固问题

```
1、MAC系统下,间歇性无法点击左边的标签问题, 暂未成功解决 https://github.com/hvqzao/burp-wildcard/issues/7
2、Burpsuite v2022.9.5及以上版本API修改,启用插件不生效. https://github.com/hvqzao/burp-wildcard/issues/8
```

##### wildcard-1.07.fix.1

```
基于wildcard v1.0.7简单修改，支持burp2020.11.2及后续的版本主题。
具体修复： https://mp.weixin.qq.com/s/gDlGZLbufUTMXQ7IxMX0iQ
```

##### wildcard-1.08.fix.1

```
基于wildcard v1.0.8 修复解决Burpsuite v2022.3.9及以上版本显示布局混乱问题。
```



## 中文介绍

1、此扩展程序试图解决(插件标签太多会使界面冗余难看)的问题

2、如果启用主题不兼容此扩展，则程序将自动关闭。

3、待所有插件加载完毕后，您可以使用本插件压缩所有插件标签。

4、为避免错误,建议将本wildcard插件移动到插件列表的最下方，wildcard将会被最后加载。

5、出于安全原因,每次加载本扩展程序时，需要显式启用此功能,允许保存为自动压缩。



## 原版介绍

 hvqzao/burp-wildcard:  https://github.com/hvqzao/burp-wildcard

There is number of great Burp extension out there. Most of them create their own tabs. Too many of them makes the interface heavy and ugly. This extension tries to address this issue. It provides ability to hijack tabs belonging to other extensions (it is not oficially supported by Burp Extensions). For safety reasons, in order to work, this feature must be explicitly enabled on Options tab each time extension is loaded.

Before:

![wildcard-1](https://cloud.githubusercontent.com/assets/4956006/9557495/b4b1de86-4ddc-11e5-9b7a-d6bec8af7681.png)

After:

![wildcard-2](https://cloud.githubusercontent.com/assets/4956006/9557497/b84756a2-4ddc-11e5-91a7-01c655147adb.png)

Extension also provides CSRF Handling mini-extension source (Python) which could be saved as a file, customized and loaded into Burp later on. Newly added extension will handle application specific CSRF tokens.

This extension will automatically turn off if dark theme "Darkula" (BurpSuite 2+) is enabled as it is not compatible with it.

Requires Java 8.

This extension _DOES NOT_ require Burp Suite Professional



## NEED STAR And ISSUE

```
1、右上角点击Star支持更新.
2、ISSUE或NOVASEC提更新需求
```

![NOVASEC](doc/NOVASEC.jpg)