# 部署微信公众号机器人

部署微信公众号机器人接入 LangBot 。

## 创建机器人

进入[微信公众平台](https://mp.weixin.qq.com/)，如果已经有公众号账号，那么直接扫码登录，进入控制台。
如果之前没有注册过公众号，那么点击立即注册，选择 `公众号`，依次填写信息，进入控制台。控制台是这样的：
![控制台页面](/assets/image/oa1.png)


## 设置回调地址

### 获取配置项 

点击`设置与开发`，`开发接口管理`，出现这样的页面：
![设置开发项](/assets/image/oa2.png)

记录下来`开发者ID（AppID）`，`开发者密码（AppSecret）`，并将部署 LangBot 的服务器添加入`IP白名单`。

### 设置反向代理

由于微信公众号的只支持http（80端口），https（443端口），所以本文假设80端口已被占用，使用443端口反向代理至 LangBot 。<br>
具体的反向代理配置教程与[QQ官方机器人反向代理配置](/deploy/platforms/qq/official_webhook.md#操作caddy流程)相同，只是将`reverse_proxy 127.0.0.1:2284`改为`reverse_proxy 127.0.0.1:2287`。

### 保存回调地址

点击设置服务器配置，输入`Token`，`EncodingAESKey`，并将消息加解密方式改为`安全模式`。<br>
至此，将获取到的四个配置项( AppID , AppSecret , token , EncodingAESKey )填入[微信公众号配置项](/deploy/quick-config/config.md#微信公众号适配器)。填写成功后，**启动 LangBot 。**<br>

将 URL 填写为`https://your_domain_name/callback/command`，其中的 `your_domain_name` 就是 Caddy 中填写的域名。点击保存。如果可以保存成功，那么意味着部署成功。如果出现**系统发生错误，请稍后重试**，那么请重新检查以上配置内容是否填写正确。

