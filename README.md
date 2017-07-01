
>如何你觉得这篇文章对你有用，欢迎star，如果你有更好的自定义模板，欢迎填充完善，帮助更多的人

## Android Studio Live Templates使用详解，提高敲代码的速度


本篇将从 Live Templates简介，常用AS自带模板，自定义模板三个方面开展介绍，并且只介绍 Live Templates中java代码方面的使用，其余感觉不是很常用，看完这篇之后你可以自己研究一下。

>（温馨提示，本文图片较多建议在电脑上阅读）

一个好的程序猿应该是花更多的时间在处理业务处理上，而不是重复敲相同的代码，一行代码节约1s也是节约。看完这篇之后你会觉得AS确实越来越强大了，简直是Android程序猿的福音呀，希望推出更多提高开发效率的工具或插件。废话不多说，直接进入主题。



## 什么是 Live Templates
没有统一的翻译，代码模板、热键模板、动态模板随便叫哪个都行

###	作用

- 代码快速补全
- 提高写代码的速度

### 位置

- Settings->Editor->Live Templates

### 用法

- 全关键字型：关键字-->回车
- 后缀关键型：使用对象.关键字-->回车

### 简单使用
先来两个效果图，吊一下胃口，更加实用的还在后面

AS自带模板

>快速打印日志

logt -->快速补全TAG
loge—>快速补全Log.e(TAG,"");

![这里写图片描述](http://img.blog.csdn.net/20170701231712136?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXExMzc3MjI2OTc=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

自定义模板

> 输入 sin 回车即自动补全单例模式所需的代码

![这里写图片描述](http://img.blog.csdn.net/20170701231848192?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXExMzc3MjI2OTc=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)


## 系统自带模板

系统自带模板从两个方面讲解，全关键字型和后缀关键型，由于篇幅的原因，这里只讲解常用的一些模板，未讲解到的可以到 Settings->Editor->Live Templates中查看

### 全关键字型

先来说说什么是全关键字型，其实就是输入关键字-->回车，eg：输入loge  回车即会自动打印出
```java
Log.e(TAG, "onCreate: ", );
```

#### **findViewById**

在此之前我们在Activity中找到一个view可能是这样写的：

![这里写图片描述](http://img.blog.csdn.net/20170701234426474?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXExMzc3MjI2OTc=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

有了fbc之后我们可以这样写：fbc  回车

![这里写图片描述](http://img.blog.csdn.net/20170701234504586?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXExMzc3MjI2OTc=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)


#### **定义常量**
以前你写整形常量是不是要一个单词的敲出： ```private static final int  。。。```

还有更快的写法：const  回车

![这里写图片描述](http://img.blog.csdn.net/20170701234809036?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXExMzc3MjI2OTc=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

字符串常量也有：key 回车

![这里写图片描述](http://img.blog.csdn.net/20170701235128741?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXExMzc3MjI2OTc=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

其他常量，目前as只提供了整形和字符串类型常量的模板，学了后面的自定义之后你就可以定义其他类型的了，当然还有一种捷径：psf  回车即可快速补全
```java
public static final
```

#### **for循环**
相信很多小伙伴也觉得每次都要写整个for循环好麻烦，as提供了：fori 回车，看对比图
>这里还有一个隐藏的模板，sout 回车 即可快速补全 System.out.printf("");

![这里写图片描述](http://img.blog.csdn.net/20170701235847504?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXExMzc3MjI2OTc=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)


#### **if判断**

- ifn  回车（推荐）

 ![这里写图片描述](http://img.blog.csdn.net/20170702000056116?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXExMzc3MjI2OTc=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

- inn  回车

![这里写图片描述](http://img.blog.csdn.net/20170702000131514?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXExMzc3MjI2OTc=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)


#### **隐藏View**
- gone

![这里写图片描述](http://img.blog.csdn.net/20170702000303462?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXExMzc3MjI2OTc=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

#### **快速在子线程中切换到主线程**
- rouiT

![这里写图片描述](http://img.blog.csdn.net/20170702000416536?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXExMzc3MjI2OTc=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)


#### **字符串格式化**
- Sfmt

![这里写图片描述](http://img.blog.csdn.net/20170702000751653?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXExMzc3MjI2OTc=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

#### **快速实现自定义View的三个构造方法**
- ViewConstructors

>个人觉得这个是一个非常实用的模板了，比快捷键还方面，不行你自己试试

![这里写图片描述](http://img.blog.csdn.net/20170702000938318?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXExMzc3MjI2OTc=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

OK 全关键字型就只讲这些常用的了，不常用的可以去设置中查看

### 后缀关键型

再来说说什么是后缀关键型，其实就是“使用对象.关键字-->回车”，继续往下看就知道是什么啦：

#### **判断**
- .notnull
- .null

![这里写图片描述](http://img.blog.csdn.net/20170702001253744?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXExMzc3MjI2OTc=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

#### **局部变量**
- .var

![这里写图片描述](http://img.blog.csdn.net/20170702001837470?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXExMzc3MjI2OTc=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

#### **全局变量**
- .field

>这个也是一个非常实用的模板，在代码量非常多的类中就更加突出了，不用跑到来的最前面定义右跑回来初始化。

![这里写图片描述](http://img.blog.csdn.net/20170702001914208?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXExMzc3MjI2OTc=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

#### **循环**
- .for  增强for循环
- .fori  正序遍历
- .forr  逆序遍历

![这里写图片描述](http://img.blog.csdn.net/20170702002448492?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXExMzc3MjI2OTc=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

还有针对下标的

![这里写图片描述](http://img.blog.csdn.net/20170702002705766?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXExMzc3MjI2OTc=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

#### **return返回**
- .return

![这里写图片描述](http://img.blog.csdn.net/20170702001711127?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXExMzc3MjI2OTc=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

#### **类型转换**
- .cast

![这里写图片描述](http://img.blog.csdn.net/20170702002754196?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXExMzc3MjI2OTc=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)


#### **抛出异常**
- .try

![这里写图片描述](http://img.blog.csdn.net/20170702002925860?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXExMzc3MjI2OTc=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

#### **字符串格式化**
- .format

![这里写图片描述](http://img.blog.csdn.net/20170702003109389?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXExMzc3MjI2OTc=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

#### **分支**
- .switch

![这里写图片描述](http://img.blog.csdn.net/20170702010002795?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXExMzc3MjI2OTc=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

后缀型的也只讲这些常用的了，快进入激动的自定义模板

## 自定义模块

我这里给出几个比较常用的自定义模板，如果你觉得有比较好的可以抽取出来的，欢迎留言。

### 单例模式

还是一开始就给出的单例模式，再来看看效果图：

![这里写图片描述](http://img.blog.csdn.net/20170701231848192?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXExMzc3MjI2OTc=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

是不是很带感，来看看怎么设置（建议先新建一个Template Group，便于管理）：



![这里写图片描述](http://img.blog.csdn.net/20170702003754459?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXExMzc3MjI2OTc=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

然后点击 Edit variables

![这里写图片描述](http://img.blog.csdn.net/20170702004215365?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXExMzc3MjI2OTc=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

下面是单例模式的模板（根据个人写单例模式的习惯来）
```java
private static $class$ m$class$ = null;
private $class$(){}
public static $class$ getInstance() {
    synchronized ($class$.class) {
        if (m$class$ == null) {
            m$class$ = new $class$();
        }
    }
    return m$class$;
}
```

来看看上面涉及到的知识：

![这里写图片描述](http://img.blog.csdn.net/20170702004310042?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXExMzc3MjI2OTc=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

更详细的**Expression** 介绍：https://www.jetbrains.com/help/idea/2016.1/live-template-variables.html

**Skip if defined** ： 如果选中，光标会直接跳到句末，不会停留在某个变量处。

### click

![这里写图片描述](http://img.blog.csdn.net/20170702004456502?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXExMzc3MjI2OTc=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

模板：
```java
public void onClick(View view) {
    switch (view.getId()) {
        case R.id.$resId$:
            $content$
            break;
        default:
            break;
    }
}
```
### 打印带定位功能的日志
新建 dl （名字自拟）为下面的模板
```
Log.e("$class$","$method$($class$.java:$line$)"+$content$);
```
![这里写图片描述](http://img.blog.csdn.net/20170702004855355?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXExMzc3MjI2OTc=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

![这里写图片描述](http://img.blog.csdn.net/20170702005128423?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXExMzc3MjI2OTc=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

为什么打印下面的代码就可以定位到指定类所在的行数呢？
```
Log.e("MainActivity","onCreate(MainActivity.java:13)我是日志内容");
```
告诉你一个小秘密，logcat中只要打印的内容中带有"(类名.java:行号)"就可以自动变为可点击的链接，点击之后就可以跳转到改类指定的行数。这样就实现了打印带定位功能的日志，但是这个是有一定的局限性的，比如打印语句之前很可能会增加代码，由于行数是固定死的，此时就会导致定位有一定的误差。怎么解决呢？这里推荐看一个日志打印的工具类，[android studio日志打印神器，日志代码跟踪器ELog](http://blog.csdn.net/qq137722697/article/details/72802800)

### Switch

快速搭建模式、防止漏掉break和default

```java
switch ($content$) {
    case $value$:
        $code$
        break;
    default:

        break;
}
```
![这里写图片描述](http://img.blog.csdn.net/20170702010234648?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXExMzc3MjI2OTc=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

### 字符串非空判断

>这也是一个非常实用的模板了
```java
TextUtils.isEmpty($content$);
```
![这里写图片描述](http://img.blog.csdn.net/20170702010418841?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXExMzc3MjI2OTc=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

## 最后

福利，这篇文章是本人在给组内同事培训时制作的ppt修改而来，我将ppt共享出来，如果你有这个需求也可以下来修改修改。下载地址：https://github.com/huangdali/livetemplates
