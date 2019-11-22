
注意：本项目已经停止维护，新版访问：https://github.com/CodeNeedWho/JsDroidCmd/

### 简介
本项目是JsDroid的核心代码，编译后是一个通过app_process启动的命令apk，类似uiautomator.apk(/system/framework/uiautomator.jar)。<br><br>
JsDroid是将uiautomator搬出来，结合Rhino的javascript引擎，升级打造的一款全新的安卓自动化框架，在原生功能的基础上实现了中文输入、屏幕找图、远程执行等功能。<br><br>
既然有uiautomator，为啥还要JsDroid呢，JsDroid=Js+Droid,js机器人,js（JavaScript）帮助您完成自动化操作，您只需要会js，就能完成uiautomator的所有功能。<br><br>
JsDroid更倾向于脚本化，开发更快速，更便捷，网络传输更小巧，热更新，快速部署，如果能够开发成熟，远程控制多种设备，实现云测系统。<br><br>
为了让大家更加容易使用jsdroid，本人也是开发了一款编辑器，叫做JsDroidIDE，借用了RSytaxTextArea语法高亮编辑器，智能代码提示，模仿uiautomatorviewer实现了截屏工具，截屏工具增加了找图找色的工具面板。<br>

### 使用
1.启动jsdroid服务
~~~adb push jsdroid_cmd.apk /data/local/tmp/jsdroid.apk
    //无root
    adb shell app_process32 -Djava.class.path=/data/local/tmp /data/local/tmp jsdroid_cmd.apk
    //有root
    adb shell su -c "app_process32 -Djava.class.path=/data/local/tmp /data/local/tmp jsdroid_cmd.apk"
    //runjs
    adb shell runjs -start
~~~
2.调用方式
~~~
    //无root（短调用）
    adb shell curl http://127.0.0.1:9800/?js='hello world!'
    //有root（短调用，会添加SystemService）
    adb shell dumpsys jsdroid_service /data/local/tmp/main.js
    //runjs（长调用）
    adb shell /data/local/tmp/runjs -file /data/local/tmp/main.js
~~~
3.JsDroidIDE<br>
JsDroidIDE是专门用来编写jsdroid脚本的编辑器。
JsDroidIDE目前具有代码预览界面、截屏分析、运行与停止和打包apk等功能。


### 联系方式
    qq：980008027
    
