---
layout: nodate
title: 开发者
---
Light OpenSource Project遵循Apache License 2.0发布全部的LOSP源代码，所有开发者都可以在我们发布的源码基础上下载、适配、编译、修改。

同步源码：  
{% highlight sh %}
repo init -u git://github.com/LOSP/platform_manifest.git -b jb43
repo sync
repo start jb43
{% endhighlight %}

提交更改：  
首先在github上对您修改过的项目进行fork操作到你自己的github，然后  
{% highlight sh %}
cd /你的项目路径
git add -A
git commit -m "修改说明"
git push https://github.com/你fork后的路径 jellybean
{% endhighlight %}
然后在你的github上对我们发起pull request

如何适配：  
你的设备必须有CM10.1或Slim的device，其他4.2ROM的device也可以，但是可能需要修改的更多。  
首先克隆你的device。  
然后切换到设备device根目录，编辑vendorsetup.sh，修改cm_xxxx-userdebug为losp_xxxx-userdebug  
改名cm.mk为losp.mk  
打开losp.mk，修改其中cm\_xxxx为losp\_xxxx  
修改vendor/cm为vendor/losp  
如果有OriginalAudio.mk这种不存在的调用，记得将其修改为AllAudio.mk  
接下来，参考米1和米2的LOSP官方适配device，修改支持编译MIUI Recovery  
然后make bacon，就可以发布啦  
