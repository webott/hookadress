QQ：2645542961

用代码实现hook拦截获取到微信二维码，用到的工具有 ce od。
1.	先看下图片在内存里面的表现形式，微信登陆的二维码是一个png的格式，看下png在内存的表现形式，看下图，就是png在内存里面的格式，开头都是固定的格式。百度搜索“UltraEdit”下载，然后打开一个png图片查看。

![image](https://user-images.githubusercontent.com/73727649/118352760-b799da00-b595-11eb-868b-983a1d5a657d.png)
接下来找微信二维码的数据，先打开CE工具，附加微信进程，找到时候有技巧，打开微信的时候不要显示二维码的界面，显示登陆历史微信的界面，然后选择未初始的值，点击扫描，最后出来很多结果，然后点击切换账号，显示出来二维码，然后选择 改变的值，点击“Next Scan”，这样少了很多数据，然后再用自己微信扫，再还选改变的值，继续点击“Next Scan”，这样来回几次，过滤出来的数据会越来越少
![image](https://user-images.githubusercontent.com/73727649/118352764-c08aab80-b595-11eb-8a73-f5c8526d0508.png)
最后把基址放到下面，然后手动记录下他的值，放到备注里面，然后最终留下描述没有变化的值，就是基址了。
![image](https://user-images.githubusercontent.com/73727649/118352770-c8e2e680-b595-11eb-80f6-7e3211e35b8b.png)
4找到基址后，在OD下断点，最终就可以找到登陆二维码
![image](https://user-images.githubusercontent.com/73727649/118352773-ce403100-b595-11eb-9550-f6aaf764add0.png)
现在已实现很多有趣的功能，可提供接口二次开发，欢迎技术交流。
QQ：2645542961
![image](https://user-images.githubusercontent.com/73727649/118352780-dc8e4d00-b595-11eb-82d1-3fafeb9f1785.png)
