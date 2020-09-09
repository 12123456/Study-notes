1、诞生

2、设计思想

​	vue：渐进式框架、声明式渲染、组件。支持数据双向绑定

​	react：函数式编程、数据不可变、单项数据流。（onChange、setState实现双向数据流）

3、编写与法

​	

4、构建工具



5、数据绑定



6、diff算法



7、指令



8、性能优化



9、原生渲染native



10、ssr渲染



11、生命周期



react : 【初始化阶段】

​			①、**getDefaultProps**:为组件的实例挂载默认的属性（只执行一次）

​			②、**getInitialState**:为实例挂载初始状态，且每次实例化都会执行

​			③、**componentWillMount**(Vue中created+beforeMount):这里实在渲染之前最后一次更改数据的机会，在这里更改的话是不会触发render的重新执行。

​			④、render:渲染dom，render()方法必须是一个纯函数，不应该改变state，也不能直接和浏览器交互，事件放在生命周期内。

​			⑤、componentDidMount(Vue中的mounted):多用于操作真是dom

​			【运行阶段】：只在数据（属性、状态）发生改变的时候才会执行

​			①、**componentWillReceiveProps**(nextProps,nextState):父组件传入的属性改变，触发子组件执行此钩子。执行时，子组件接受到新的参数，未同步至this.props,**多用于判断新属性和原有属性的变化，更改组件状态。**

​			②、shouldComponentUpdate(nextProps,nextState):当属性或状态发生改变控制组件是否更新。根据接受到的nextProps,nextState判断组件是否需要更新，如果返回false，则componentWillUpdate,render和componentDidUpdate不会被调用。

​			③、componentWillUpdate()==Vue中beforeUpdate:即将重新render,**千万千万不要在这里修改状态，会陷入死循环**.

​			④、render:重新渲染更新render

​			⑤、componentDidUpdate()==Vue中的updated:在这里，新的dom结构已经诞生了。

​			【销毁阶段】

​			①、componentWillUnmount()==Vue中的beforeDestroy:善后，例如使定时器无效，取消网络请求和清理监听

12、销毁组件



13、状态集管理工具