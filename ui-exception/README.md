# ui-exception

## 概述

Exception（异常）页面是客户端在浏览网页时，服务器无法正常提供信息、页面不存在等原因所返回的页面，告知用户其所请求的页面的异常原因，同时引导用户使用网站其他页面而不是关闭窗口离开。

## 安装

```shell
npm i --save @sdp.nd.ui/ui-exception // 安装
```

## API
| 参数     | 说明  | 类型 | 默认值                                   |
|-----------|--------|--------|-----------------------------------------|
| className | 可选参数，自定义Exception样式（即类名 ）| string | - |
|img	|可选参数，异常图片路径|	string|	"https://gw.alipayobjects.com/zos/rmsportal/KpnpchXsobRgLElEozzI.svg"|
|type	|可选参数，可选异常类型，可选403、404、500|	number/string	|"404"|
|title	|可选参数，自定义异常类型。当type不能满足需求时，可自定义异常	|string|	-|
|desc	|可选参数，异常类型的描述	|string	|"抱歉，你访问的页面不存在"|
|subDesc|可选参数，异常类型的详细描述	|string|	-|
|footer	|可选参数，自定义操作区元素。当默认的按钮，不能满足操作需要时，可以选择创建一个元素或组件|	reactNode|	-|


