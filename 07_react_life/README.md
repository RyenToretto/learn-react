## react 生命周期回调函数 （生命周期钩子）
    在某个时间点上，会自动调用相应的回调函数
    如果需要添加逻辑，则重写生命周期函数
```
    常用的生命周期函数：
        ---->render(){} // 挂载 mount，提供界面 ---- 初始化/更新
        ---->componentDidMount(){} // 挂载成功后（第一次显示后） ---- 只执行一次，执行异步代码
        ---->componentWillMount(){} // 即将挂载前（第一次显示前） ---- 只执行一次，做收尾工作（清除定时器）
        ---->componentWillUnmount(){} // 即将卸载前
```

#### 初始化
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

#### 更新: 组件运行时， this.setState 状态数据发生改变
```
--->8. componentWillUpdata(){this.state={}}

--->6. render(){} // 挂载 mount

--->9. componentDidUpdata(){this.state={}}
```

#### 死亡: 组件将要卸载前
```
--->10. componentWillUnmount(){}
        (1) 清除定时器
```
