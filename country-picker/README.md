# country-picker

## 概述

控件说明：选择国家、地区的控件


使用情境：可以根据业务需求配置是否显示国际区号，来适配不同的应用情景。

需要国际区号时，常用于选择国际区号；不需要显示国际区号时，常用于切换当前的国家/地区, 提供该地区对应的服务。

## 安装
```shell
npm i --save @xxx.ui/country-picker // 安装
```

## API
| 参数     | 说明  | 类型 | 默认值                                   |
|-----------|--------|--------|-----------------------------------------|
| className | 可选参数，自定义CountryPicker样式（即类名）| string | - |
| showSearch	| 可选参数，是否显示搜索框	| boolean| 	false| 
| showTel	| 可选参数，是否显示国际区号	| boolean| 	false| 
| countries	| 可选参数，自定义国家/地区列表【需要按照固定格式，tel按需填写】	| []，格式： [{  sort: '分类（eg.A）'  country: [{ name: '国家/地区名', tel: '国际区号'},{},...]  },{},...]| 	默认配置文件countryConfig.js
| inputPlaceholder	| 可选参数，自定义搜索框占位符	| string| 	"搜索地区"| 
| loading | 可选参数，国家/地区列表是否加载中 | boolean | false | 
| onSearch	| 可选参数，搜索框输入值/点击搜索按钮时触发的回调	| (value)=>void	| -| 
| onSelect| 	可选参数，选中国家/地区时触发的回调| 	(value)=>void	| -| 
