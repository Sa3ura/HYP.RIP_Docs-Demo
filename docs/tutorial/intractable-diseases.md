# 疑难杂症解决

此页面为解决一些人存在的疑难杂症。

### Q：我添加了服务器，但是显示不能连接服务器怎么办？

A：下载交流群内的DnsJumper压缩包，并解压，选中DnsJumper.exe并右键以管理员身份运行。

{% hint style="success" %}
您可以完全放心，DnsJumper无任何后门病毒。

只是一个为您挑选优质DNS，并且增快DNS解析的工具。
{% endhint %}

打开之后，请选择您主板的网络适配器。(一般为第一个)

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

之后点击最快DNS，之后点击开启DNS测试。这时程序为自动测试并挑选解析延迟最低的DNS服务器。

<figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

等待测试完成，点击应用DNS服务器。程序会自动帮您在系统内设置测试最快的DNS服务器。

<figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

听到提示音后，说明DNS已经更换成功，之后右键左下角的Windows图标，选择终端(管理员)

之后在终端内输入

```
netsh winsock reset
ipconfig /flushdns
```

<figure><img src="../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

之后重启您的计算机，然后重新打开客户端，即可修复无法连接服务器的问题。

### Q：为什么控制台进不去了？

A：有傻逼在DDoS。

### Q：我添加了服务器，但是显示不能解析主机名怎么办？

A：确定你使用的是Java8来启动的客户端，并且你的客户端需支持SRV解析。

如果你满足以上两个条件还是不能解析，那么使用DnsJumper或把DNS更改到8.8.8.8和8.8.8.4即可。
