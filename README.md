# IPTV-GO
通过Vercel部署自己的无服务器go环境用以观看IPTV
- forks项目
- 访问https://vercel.com 选择Github的IPTV-GO并构建
## 详细使用方法
## **虎牙、斗鱼、YY实时M3U获取：**
### 虎牙一起看：
```
http://你的IP:35455/huyayqk.m3u
```
### 斗鱼一起看：
```
http://你的IP:35455/douyuyqk.m3u
```
### YY轮播：
```
http://你的IP:35455/yylunbo.m3u
```
### 如果使需要自定义M3U文件中的前缀域名，可以传入url参数（需要注意的是，当域名中含有特殊字符时，需要对链接进行urlencode处理）：
```
http://你的IP:35455/xxxyqk.m3u?url=http://192.168.10.1:35455
```
## **抖音：**
### 1，抖音手机客户端进入直播间后，点击右下角三个点，点击分享，点击复制链接，然后运行并访问：
```
http://你的IP:35455/douyin?url=https://v.douyin.com/xxxxxx(&quality=xxxx)
```
其中&quality参数默认origin原画，可以省略，也可以手动指定：uhd、origin、hd、sd、ld
### 2，抖音电脑端需要打开抖音网页版复制`(live.douyin.com/)xxxxxx`，只需要复制后面的xxxxx即可：
```
http://你的IP:35455/douyin/xxxxx
```
## **斗鱼：**
### 1，可选m3u8和flv两种流媒体传输方式【`(www.douyu.com/)xxxxxx 或 (www.douyu.com/xx/xx?rid=)xxxxxx`，默认m3u8兼容性好】：
```
http://你的IP:35455/douyu/xxxxx
```
### 2，选择flv时可选择不同cdn（需要加`stream`和`cdn`参数，不加参数默认`hls`和`akm-tct.douyucdn.cn`）
```
http://你的IP:35455/douyu/xxxxx(?stream=flv&cdn=hw-tct)
```
## **BiliBili`(live.bilibili.com/)xxxxxx`：**
### 1，平台platform参数选择（默认web，如果有问题，可以切换h5平台）：
```
"web"   => "桌面端"
"h5"    => "h5端"
```
### 2，线路line参数选择（默认线路二，如果卡顿/看不了，请切换线路一或者三，一般直播间只会提供两条线路，所以建议线路一/二之间切换）：
```
"first"  => "线路一"
"second" => "线路二"
"third"  => "线路三"
```
### 3，画质quality参数选择（默认原画，可以看什么画质去直播间看看，能选什么画质就能加什么参数，参数错误一定不能播放）：
```
"30000" => "杜比"
"20000" => "4K"
"10000" => "原画"
"400"   => "蓝光"
"250"   => "超清"
"150"   => "高清"
"80"    => "流畅"
```
### 4，最后的代理链接示例：
```
http://你的IP:35455/bilibili/xxxxxx(?platform=h5&line=first&quality=10000)
```
## **虎牙`(huya.com/)xxxxxx`：**  
### 1，查看可用CDN：
```
http://你的IP:35455/huya/xxxxx?type=display
```
### 2，切换媒体类型（默认flv，可选flv、hls）： 
```
http://你的IP:35455/huya/xxxxx?media=hls
```
### 3，切换CDN（默认hwcdn，可选hycdn、alicdn、txcdn、hwcdn、hscdn、wscdn，具体可先访问1获取）：
```
http://你的IP:35455/huya/xxxxx?cdn=alicdn
```
### 4，最后的代理链接示例：
```
http://你的IP:35455/huya/xxxxx(?media=xxx&cdn=xxx)
```
## **YouTube:**
```
https://www.youtube.com/watch?v=cK4LemjoFd0
Rid: cK4LemjoFd0
http://你的IP:35455/youtube/cK4LemjoFd0(?quality=1080/720...)
```
## **YY（默认最高画质，参数为4）:**
```
https://www.yy.com/xxxx
http://你的IP:35455/yy/xxxx(?quality=1/2/3/4...)
```
## 本仓库源码内容全部来自于友善的肥羊，仅用于学习交流，绝不用于其他商业用途

