# burp-wildcard
burp-wildcard 简单修改用以支持burp2020.11.2及后续的版本主题。

# wildcard插件介绍

github  hvqzao/burp-wildcard:  https://github.com/hvqzao/burp-wildcard

1、此扩展程序试图解决(插件标签太多会使界面冗余难看)的问题

2、如果启用主题不兼容此扩展，则程序将自动关闭。

3、待所有插件加载完毕后，您可以使用本插件压缩所有插件标签。

4、为避免错误,建议将本wildcard插件移动到插件列表的最下方，wildcard将会被最后加载。

5、出于安全原因,每次加载本扩展程序时，需要显式启用此功能,允许保存为自动压缩。


# Burp新版无法加载wildcard：
1、burpsuite官方开放的扩展管理API默认只支持Nimbus主题，与其他主题不兼容。

2、wildcard是基于API默认开发的，载入时会判断是否处于Nimbus主题内，如果不是当退出插件。

3、由于2020.11.2及以上版本没有Nimbus主题，只有统一的Light主题，和Dark主题，导致wildcard插件仅支持至burp 2020.11.1及以下版本，不支持burp 2020.11.2

4、唯一的好消息是, Light和Dark主题是基于Nimbus主题进阶的，只要修修源码就能重用在这两个主题上。

具体图像说明请查看NOVASEC微信公众号文章： 暂无

# 其他

感谢原作者的开源

如果帮助到了你，关注公众号，点个star吧，嘿嘿


# 代码修改点 burp-wildcard-plus\src\hvqzao\wildcard\WildcardExtension.java

//if ("nimbu".equals(UIManager.getLookAndFeel().getName().toLowerCase()) == false) {
            if (true) {
               //已知Nimbus,Light,Dark主题兼容本插件,其他burp主题可能不兼容,遇到此类情况请更换主题.
                new PrintWriter(callbacks.getStdout(), true).println("PinYin: Yi Zhi Nimbus,Light,Dark Zhu Ti Jian Rong Ben Cha Jian,Qi Ta Burp Zhu Ti Ke Neng Bu Jian Rong ,Yu Dao Ci Lei Qing Kuang Qing Geng Huan Zhu Ti.");
                new PrintWriter(callbacks.getStdout(), true).println("English: Nimbus,Light and Dark themes are known to be compatible with this plug-in, other BurP themes may not be compatible, please change the theme in such cases.");
                //callbacks.unloadExtension();
                //return;
            }
