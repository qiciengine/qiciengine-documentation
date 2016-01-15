# qc.WeChat

## 描述
微信接口组件

## 变量
| 变量名         |   类型      |  作用        |
| ------------- |-------------|-------------|
| shareAppId | string | 用于分享的微信公众号的唯一标志 |
| wxAppId | string　| 用于登录的微信公众号的唯一标志，通常情况下可以与ShareAppId配置相同 |
| webAppId | string | web应用的appId |
| domain | string | 存放公众号后台相关php文件的域名地址，注意：domain必须和公众号后台中配置的域名一致 |
| gameDomain | string | 游戏服务器相关php文件的域名地址 |
| extendParams | string | 微信登录时的扩展参数，可用于传递一些自定义信息 |
| redirectCurrentUrl | boolean | 是否使用游戏页面做为授权成功后的重定向地址。 |

## 参考手册
[WeChat](http://docs.zuoyouxi.com/manual/Plugin/Wechat.html)