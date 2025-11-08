#  悠哉 电报 TG @fuchenyouzaibot
# Cloudflare新建page部署cf节点

## 0获取 uuid  复制uuid备用
点击 打开 [获取 uuid ](https://www.uuidgenerator.net/)
打开后Copy复制，那一行uuid即可。
复制后，做好记录备用，别整没了部署时用
#
#

## 1 注册 github 账号
  
点击 打开 [注册 github 账号](https://github.com/signup?source=form-home-signup&user_email=)

github账号注册＝
注册时可选谷歌账号快捷登录。
一个github可验证一次dpdns域名注册共得两个域名
 
#
#
#
 
## 2 注册 cloudflare cf账号
  
点击 打开 [注册 cloudflare 账号](https://dash.cloudflare.com/sign-up)

Cloudflare账号注册=
注册时可选
谷歌账号快捷登录
苹果账号快捷登录
github账号快捷登录
然后再部署cf。

#
#
#

## 3 注册号 dpdns 域名账号
  
点击 打开 [注册 dpdns 账号](https://dash.domain.digitalplat.org/auth/register)

dpdns账号注册=
必须有github账号才能完成dpdsn账号注册。

### 1-注册域名账号时需要用到的地址和手机号
Montana Ave,500,Havre,Montana,United States
手机号格式 +1-3214416161

### 2-注册中时需要跳转至github.com账号验证注册。
1 浏览器设置翻译为中文

2 菜单里选择注册域名，起个英文或加点数字的域名，确定可用后，别关页面，留着填写cf托管时获得的1和2地址。

3 打开Cloudflare，填写域名转入，托管域名，填写你起的dpdns域名，托管域名至CF，选择免费计划，继续自动查找dns，去激活，获取两个地址1和2。

4 复制1和2，填写1和2两个地址，至dpdsn，注册域名的页面1和2里。然后保存即可。注册域名完成
##  复制好域名备用

【dpdsn域名那个页面有个活动点进去后，按照提示可以额外获得一个域名注册资格，去他的仓库点收藏那个五角星⭐给点亮了，然后回那个活动页面点验证，即可多获得一个域名注册资格。这样就可以部署到两个cf账号上！！！】

#
#
#

## 4 部署Cloudflare page

Cloudflare  cf  里左侧菜单点worker和page按钮 ， 
进入后，新建page应用项目，   
起项目名英文加数字能起上就行随意，  
下载  _worker.zip   压缩包，  
选择从计算机或设备上传，  
选择 _worker.zip，压缩包上传，保存部署。

选择，自定义域名，输入域名，继续激活，显示初始化，会自动完成dns设置，大约2分钟 刷新 页面，完成后显示为活动。

然后，项目页面里，点设置，点变量和密钥，  选，密钥，输入名为 :  uuid   ,值为你之前获取的 uuid 保存提交。

最后 项目页面里点部署，点创建新的部署，在上传一下 _worker.zip，压缩包，然后提交即可。


到此为止，部署就完成了。关闭页面即可。
#
#
#


# 手搓，v2 单节点  示例


## 手搓单节点，可用于 v2

```json


vless://提示开始你的uuid填这里提示结束@提示开始你的优选ip填这里提示结束:443?path=%2Fpyip%3D提示开始你的pyip填这里提示结束&security=tls&encryption=none&host=提示开始填写不带前缀https的纯域名指示结束&fp=chrome&type=ws&sni=提示开始填写不带前缀的纯域名提示结束#提示开始填写不带前缀的纯域名提示结束。

```


指示开始至提示结束 的所有内容都不要。换为你的uuid和域名和优选ip和pyip


```json


vless://空@空?path=%2Fpyip%3D空&security=tls&encryption=none&host=空&fp=chrome&type=ws&sni=空#空。


```


```json


vless://你的uuid@104.26.1.182:443?path=%2Fpyip%3D38.244.198.107:443&security=tls&encryption=none&host=你的域名&fp=chrome&type=ws&sni=你的域名#你的域名


```


其中是优选ip

104.26.1.182:443

具体端口根据你的优选ip是哪个就写哪个。



其中是pyip

38.244.198.107:443

具体端口根据你的pyip是哪个就写哪个。

不过，使用单节点，v2  客户端，需要设置一堆东西。。。还是直接用苍井空配置文件比较实用。


### 纯域名，不带，https://www.前缀的。

### 示例 域名.dpdsn.org




#  
#
#
#

# 悠哉   苍井空配置文件.yaml  使用方法 

## 下载  cangjingkong.yaml  配置文件

### 使用方法
电脑用 记事本 打开文件编辑。

手机用这个app打开文件编辑。

菜单，

点查找，

查找目标填写: 你的域名 

替换为: 填写你注册的域名地址 

✓循环查找

 替换全部 

保存文件


菜单，

点查找，

查找目标填写: 你的uuid 

替换为: 填写你uuid

✓循环查找 

替换全部

 保存文件

  
纯域名，不带，https://www.前缀的。

示例  域名.dpdsn.org


#
#
#






# 测试，ip和dns。只可以用edge浏览器测。⚠️

## 手动选择分组中，选择一个节点。然后打开edge浏览器。测试。

### https://whoer.net



## ip和dns位置测试 防止dns和ip位置不一样！

选择，配置文件，节点选择里的节点，然后打开网址检测

点击 打开 [检测ip和dns ](https://whoer.net/)

当dns和ip不一致时，更换pyip，默认端口443

    path: "/pyip=185.148.14.85"

当pyip 指定了端口的pyip时填写上端口。
    path: "/pyip=185.148.14.85:实际的端口"



V2代理软件中单节点更换pyip示例
           /pyip=185.148.14.85
          /pyip=45.149.186.112:8080



优选ip   等于 ＝ server

uuid

proxyip 等于 ＝  pyip


#
#
#


clash 示例
```json

- name: 地区17
  type: vless
  server: 优选ip
  port: 443
  uuid: 你的uuid
  tcp:  true
  udp: true 
  tls: true
  network: ws
  servername: 你的域名
  ws-opts:
    path: "/pyip=pyip地址:有端口号的加上端口号例如9527"  
    headers:
      Host: 你的域名


```


