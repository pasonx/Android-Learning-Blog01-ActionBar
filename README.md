# Action Bar
* 在Android Studio中，配置Android Action Bar 首先要到/res/values/目录下定义styles.xml文件，在<resource>下面的<style>里面定义了name和parent，name可以自己定义，在Manifest文件里面的<application>或者<activity>里面的theme页面引用名字就可以了。
如果开发者API版本较高，可以采用新的特性，但是为了使Android版本较低的用户正常使用，我们会创建两个目录，分别确定好引用那个theme，一般版本较高的情况下，Android Studio已经帮我们生成了供系统自己选择的styles.xml

* 其中，[1]是ActionBar的图标，[2]是两个action按钮，[3]是overflow按钮。

[action bar](http://img.blog.csdn.net/20140531141552515?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvc2lueXU4OTA4MDc=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)
