# 代码演示

## 基本用法

默认用法

```jsx
/* react */
<script>
export default class App extends React.Component {
  render () {
    return <CountryPicker />
  }
}
</script>
```

## 显示国际区号

设置showTel，默认false。可修改代码，实时预览效果

```jsx
/* react live*/
<script>
export default class App extends React.Component {
  render () {
    return <CountryPicker showTel/>
  }
}
</script>
```

## 显示搜索框

设置showSearch显示搜索框，默认false；可使用inputPlaceholder自定义搜索占位符，默认“搜索地区”。可修改代码，实时预览效果

```jsx
/* react live*/
<script>
export default class App extends React.Component {
  render () {
    return <CountryPicker showSearch />
  }
}
</script>
```

## 自定义国家/地区列表

使用countries属性自定义国家/地区列表，格式如下： 

[{


sort: '分类（eg.A）'


country: [{ name: '国家/地区名', tel: '国际区号'},{},...]


},{},...]


可修改代码，实时预览效果
```jsx
/* react live*/
<script>
export default class App extends React.Component {
  render () {
    const config = [
      {
        sort: 'A',
        country: [{
          name: '安圭拉岛',
          tel: '1264'
        },
        {
          name: '安提瓜和巴布达',
          tel: '1268'
        }]
      },
      {
        sort: 'B',
        country: [
        {
          name: '巴哈马',
          tel: '1242'
        },
        {
          name: '巴巴多斯',
           tel: '1246'
        }]
      }]
    return <CountryPicker countries={config} showTel/>
  }
}
</script>
```

## 远程加载数据

注意，数据格式需如下： 

[{


sort: '分类（eg.A）'


country: [{ name: '国家/地区名', tel: '国际区号'},{},...]


},{},...]


可修改代码，实时预览效果
```jsx
/* react live*/
<script>
export default class App extends React.Component {
  state = {
    data: [],
    loading: false
  }

  componentDidMount() {
    this.setState({ loading:true});
    const req = request()
    req.get('https://mock.gem-mine.tech/mock/74/country').then((data) => {
        setTimeout(() => {
           console.log('请求成功',data)
           this.setState({data,loading:false})
        }, 5000)
    })
  }
  render () {
    return <CountryPicker countries={this.state.data} loading={this.state.loading} showTel />
  }
}
</script>
```



