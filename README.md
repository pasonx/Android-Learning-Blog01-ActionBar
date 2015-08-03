
# Action Bar
*	在Android Studio中，配置Android Action Bar 首先要到/res/values/目录下定义styles.xml文件，在\<resource\>下面的\<style\>里面定义了name和parent，name可以自己定义，在Manifest文件里面的\<application\>或者\<activity\>里面的theme页面引用名字就可以了。
如果开发者API版本较高，可以采用新的特性，但是为了使Android版本较低的用户正常使用，我们会创建两个目录，分别确定好引用那个theme，一般版本较高的情况下，Android Studio已经帮我们生成了供系统自己选择的styles.xml

![action bar](http://img.blog.csdn.net/20140531141552515?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvc2lueXU4OTA4MDc=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

其中，[1]是ActionBar的图标，[2]是两个action按钮，[3]是overflow按钮。

如果想要移除ActionBar的话通常有两种方式，一是将theme指定成Theme.Holo.NoActionBar，表示使用一个不包含ActionBar的主题，二是在Activity中调用以下方法：
``` Java

ActionBar actionBar = getActionBar();  
actionBar.hide();   

```

##通过Action Bar图标进行导航
* 启用ActionBar图标导航的功能，可以允许用户根据当前应用的位置来在不同界面之间切换。比如，A界面展示了一个列表，点击某一项之后进入了B界面，这时B界面就应该启用ActionBar图标导航功能，这样就可以回到A界面。
我们可以通过调用setDisplayHomeAsUpEnabled()方法来启用ActionBar图标导航功能，比如：

``` Java
@Override  
protected void onCreate(Bundle savedInstanceState) {  
    super.onCreate(savedInstanceState);  
    setTitle("天气");  
    setContentView(R.layout.activity_main);  
    ActionBar actionBar = getActionBar();  
    actionBar.setDisplayHomeAsUpEnabled(true);  
}  

```

重新运行程序，结果如下：
![Github](http://t2.qpic.cn/mblogpic/8bf05abfb087c7cc5dda/460)
