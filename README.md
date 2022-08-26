## 需要准备

​			一个服务器

​			微信测试号




## 1.服务器
如果自己有服务器可以直接使用
如果没有
    1.可以自己购买
    2.可以去三丰云注册一个
        https://www.sanfengyun.com/
##2.安装宝塔
https://www.bt.cn/new/index.html


## 3.注册一个微信公众号

https://mp.weixin.qq.com/debug/cgi-bin/sandbox?t=sandbox/login 

模板标题: 自定义，例如: 宝宝，早上好!  
模板内容参考:  

```python
{{date.DATA}}  
城市：{{city.DATA}}  
天气：{{weather.DATA}}  
最低气温: {{min_temperature.DATA}}  
最高气温: {{max_temperature.DATA}} 
{{note_en3.DATA}}
今天是我们恋爱的第{{love_day.DATA}}天  
距离小宝的生日还有{{birthday.DATA}}天  
{{note_en2.DATA}}

{{note_en.DATA}}  
{{note_ch.DATA}}
```

## 4.注册并申请天行api

https://www.tianapi.com/

## 5.修改配置文件

把config.txt中的xxx全部替换成你自己的，这里需要注意的是，如果有其他提醒，建议把源码复制再粘贴一份，也就是两个源码文件夹，两个唯一不同的就是模板ID不同，其他一模一样就好

`app_id`: 测试号信息里的appID

`app_secret`: 测试信息里的app_secret

`template_id`: 模板消息接口里的模板ID

`user`: 测试号里的用户微信号

`province`: 所在省份

`city`: 所在城市

`birthday`: 生日

`love_date`: 纪念日

## 6.安装python（这里是在Windows运行的朋友）

python3 -V
如果显示错误请自行安装python3

## 7.**输入命令**crontab -e

```python
00 9-20 * * * cd /root/weixin-remind/ && date >> log && python3 main.py >> log
```

任务格式： M(分) H(时) D(日) m（月） d（周） command

M : 表示分钟1～59 , 每分钟用*或者 */1表示

H : 表示小时1～23（

0表示0点)

D : 表示日期1～31

m : 表示月份1~12

d : 表示号星期0～6（

0表示星期天）

command : 要运行的命令

ps：我这里的意思是每天的9点到20点的00分运行一次代码，也就实现了每小时提醒喝水







# 模板修改

对于有编程基础的朋友会一看就懂，

对于没有编程基础的朋友也不要慌，

我也会以纯小白的身份为大家讲解。

## 工具

浏览器扩展插件：JSON-handle

环境：python3

cmd命令行输入：pip3 install requests

编译器：vscode

## 	接口

一个人带着目的去衣柜找衣服

​			衣柜：链接								[api.tianapi.com/tianqi/index?key=0fa5999506ed39df47b3c125e202d8fe&city=北京](http://api.tianapi.com/tianqi/index?key=0fa5999506ed39df47b3c125e202d8fe&city=北京)	

​				人：参数（可有可无）  		key和city

​			衣服：data中的数据				newslist

​			目的：data中的某个数据		area



## 	颜色查询

https://www.qtccolor.com/findColor.aspx
