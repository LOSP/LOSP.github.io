---
layout: default
title: LOSP manifest文件正式上传
summary: 有了manifest，各位就可以直接通过repo同步和编译LOSP的源代码了。
---
有了manifest，各位就可以直接通过repo同步和编译LOSP的源代码了。  
LOSP manifest地址：<https://github.com/LOSP/platform_manifest>  
同步命令  
{% highlight sh %}
repo init -u git://github.com/LOSP/platform_manifest.git -b jellybean
repo sync
{% endhighlight %}
