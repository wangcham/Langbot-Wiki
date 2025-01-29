# 接入飞书机器人

## 创建机器人

前往[飞书开放平台](https://open.feishu.cn/app)，登录后，创建企业自建应用。

![alt text](/assets/image/lark_01.png)

![alt text](/assets/image/lark_02.png)

为应用添加机器人能力：
![alt text](/assets/image/lark_03.png)

在权限管理中添加图中所示权限：

![alt text](/assets/image/lark_04.png)

## 在 LangBot 中填写信息并启动

根据[填写配置信息](/deploy/quick-config/config)中的飞书适配器配置，填写相关信息。可以在`凭证与基础信息`页找到`app_id`和`app_secret`。

![alt text](/assets/image/lark_05.png)

![alt text](/assets/image/lark_06.png)

注意：`bot_name`必须与创建机器人时填写的机器人名称相同。确保`enable`为`true`。

填写完成后启动 LangBot，若成功配置，日志中会出现`[01-29 23:42:56.796] manager.py (68) - [INFO] : 初始化平台适配器 1: lark`的字样，保持 LangBot 运行。

## 配置事件订阅

前往`事件与回调`页，配置订阅方式为`长连接`：

![alt text](/assets/image/lark_07.png)

并添加事件：`接收消息`

![alt text](/assets/image/lark_08.png)

## 发布机器人

点击顶部`创建版本`，填写版本号等信息，点击下方`保存`。

![alt text](/assets/image/lark_09.png)

在飞书群中添加机器人，即可使用：

![alt text](/assets/image/lark_10.png)

![alt text](/assets/image/lark_11.png)

私聊也可以直接使用

![alt text](/assets/image/lark_12.png)