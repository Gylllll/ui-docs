# 代码演示

## 基本用法

默认用法

```jsx
/* react */
<script>
export default class App extends React.Component {
  render () {
    return <Exception />
  }
}
</script>
```

## 可选异常类型

type可选：403,404,500，默认404。可在下面的代码中修改type值，实时预览效果

```jsx
/* react live*/
<script>
export default class App extends React.Component {
  render () {
    return <Exception type="403" />
  }
}
</script>
```

## 自定义异常类型

当上述三个异常类型无法满足需要时，可使用title自定义异常类型，desc定义异常类型的描述，subDesc定义异常类型的详细描述。可修改代码预览效果。


```jsx
/* react live */
<script>
export default class App extends React.Component {
  render () {
    return(
        <Exception 
           title="400" 
           desc="抱歉，请求错误" 
           subDesc="The plain HTTP request was sent to HTTPS port"
        />
    )}
}
</script>
```
