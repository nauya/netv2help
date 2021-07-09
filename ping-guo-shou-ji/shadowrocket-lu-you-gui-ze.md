# Shadowrocket路由规则

{% hint style="info" %}
如果你不了解这是什么东西，请略过，懂的这个是什么东西的自行操作。
{% endhint %}

### 白名单过滤 + 广告

白名单中包含了境外网站中可以访问的那些，对不确定的网站则默认代理。

* 直连：top500 网站中可直连的境外网站、中国网站
* 代理：默认代理其余的所有境外网站
* 包含广告过滤

规则地址：[https://pan.ututools.com/onedrive/03\_%E8%B5%84%E6%96%99/netv2.top.conf](https://pan.ututools.com/onedrive/03_%E8%B5%84%E6%96%99/netv2.top.conf)

![](../.gitbook/assets/image%20%289%29.png)

### 使用方法

{% tabs %}
{% tab title="扫码添加" %}
打开shadowrocket，点击配置，点击左上角扫码，扫描上方二维码

![](../.gitbook/assets/image%20%288%29.png)

扫描后在下方远程文件会显示出新的配置文件，然后点击选择使用配置

![](../.gitbook/assets/image%20%287%29.png)
{% endtab %}

{% tab title="链接添加" %}

{% endtab %}
{% endtabs %}

### 添加与更改路由规则

{% tabs %}
{% tab title="添加规则" %}
点击本地规则文件，编辑配置。

![](../.gitbook/assets/image%20%2812%29.png)

进入编辑配置后，打开添加规则

![](../.gitbook/assets/image%20%2814%29.png)

在此处添加规则即可。具体类型和选项的说明可以看本tab的第三项和第四项说明
{% endtab %}

{% tab title="修改规则" %}


点击本地规则文件，编辑配置。

![](../.gitbook/assets/image%20%2812%29.png)

点击规则，搜索youku\(这里拿优酷举例\)

![](../.gitbook/assets/image%20%2813%29.png)

点击youku.com 

![](../.gitbook/assets/image%20%286%29.png)

这里看到选项是DICECT就是直连的意思，表示youku.com是不通过代理的，如果我们想改成直连可以吧选项更改成PROXY（PROXY意思是代理）

![](../.gitbook/assets/image%20%2810%29.png)

返回后重新启动shadowrocket规则就生效了。
{% endtab %}

{% tab title="规则类型说明" %}
![](../.gitbook/assets/image%20%2816%29.png)

DOMAIN-SUFFIX意思是包含所有子域名

举例输入baidu.com就包含1.baidu.com，2.baidu.com，\*\*\*.baidu.com

DOMAIN-KEYWORD意思是包含域名的关键词，

举例输入baidu 就包含所有baidu这个单词的域名，baidu.com，baidu.xixihaha.com

DOMAIN就是只有当前域名，输入说明域名就是什么不包含其他。

其他暂时不做介绍。很少用到。
{% endtab %}

{% tab title="规则选项说明" %}
![](../.gitbook/assets/image%20%2815%29.png)

PROXY表示代理，

DIRECT表示直连。

举例如果添加了域名后，选项选择PROXY就代表这个域名通过shadowrocket流量走代理

如果添加域名后，选项选择DIRECT就代表这个域名不通过shadowrocket流量，走直连不挂代理。

REJECT代表此域名返回404，可以通过添加广告域名，来屏蔽广告。
{% endtab %}
{% endtabs %}

