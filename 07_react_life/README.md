## react 生命周期回调函数 （生命周期钩子）
    在某个时间点上，会自动调用相应的回调函数
    如果需要添加逻辑，则重写 生命周期函数

#### 初次渲染
```
    1. 开始
    2. static defaultProps = {}
    3. static propTypes = {}
    4. constructor(){this.state={}}
--->5. componentWillMount(){} // 即将挂载前（第一次显示前）
        (1) 为第一次显示准备数据（）
--->6. render(){} // 挂载 mount
--->7. componentDidMount(){} // 挂载成功后（第一次显示后）
        此时可以用 this.refs 访问到组件元素
        (1) 执行异步代码（定时器、ajax）
```

#### 组件运行时， this.setState 状态数据发生改变
```
    constructor(){this.state={}}
```

#### 组件将要卸载前
```
    componentWillUnmount(){}
        (1) 清除定时器
```
