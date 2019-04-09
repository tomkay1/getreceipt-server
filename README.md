# getreceipt-server
这个是个人收款的服务端，搭配receiptnotice的安卓端

## 支持nodeJS与php
nodejs位于nodejs分支,PHP 位于php分支

### 才刚开始写



### 安装

在根目录或者子目录有package.json文件时，运行
`npm install`

### 配置mongodb的连接url

配置环境变量`mongodbfinaninurl`
或者直接在model/model.js中指定mongodburl（连接地址 例如mongodb://用户名:密码@地址:端口/数据库名）

### 配置post解密秘钥

如果客户端启用了des加密，请配置financepostpass变量，该变量为des加密的秘钥

### RestFul Api
| 作用 | 方式 | 请求地址 | 参数或POST data |
|-|-|-|-|
|接收客户端收款推送 | POST | /bill/getedmoney/ | 示例json {"time":"2018-09-20 23:18:00","money":"139.34","title":"微信支付","content":"测试收款","deviceid":"yourdeviceid","encrypt":"0"} |
|查询当前时间有无收款 | GET | /bill/querybill/now| |
|查询设备是否在线 | GET | /device/isonline/deviceid | 例如 /device/isonline/mi4c (deviceid为客户端设置里填写的内容) |

### 配置及安全






##### 这个可搭配安卓客户端receiptnotice
[receiptnotice](https://github.com/WeihuaGu/receiptnotice)
