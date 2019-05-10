# Vue学习笔记
## Vue模板语法——插值

1. **文本插值**：在节点中加入{{数据名称}}，或使用`v-text="data"`指令
2. **HTML插值**：`v-html="data"`指令
3. **属性插值**：`v-bind:attri="data"`指令
4. **JS表达式**：在模板花括号中可以写JS表达式

## Vue计算属性——computed

- 为什么需要计算属性？
{{}}放入大量逻辑代码会变得过重，难维护。

**基本写法（默认get）**
```JavaScript
  computed: {
    属性名称: function() {
      return this.data;
    }
  }
```
**完整写法**
```JavaScript
  computed: {
    属性名称: {
      get: function() {

      },
      set: function() {

      }
    }
  }
```
- 类似计算属性作用的还有：侦听器、方法。
- 计算属性最重要的一点是**可缓存**。

## Vue指令

- 是带有`v-`前缀的特殊属性，是系统自带的。
- 有一些是可以简写的，有一些还可以加入参数，有一些也可以添加修饰符。

## Vue中class绑定

1. 使用`v-bind`进行class绑定`:class=`
2. 使用对象写法，`:class="{bg:true}"`也可以是data属性。多个类绑定对象写法：`:class="{bg:true,isActive:false}"`也可以是data属性。变量就是类名。
3. 数组语法：`:class="[bg, isActive]"`，其中的变量都是实际的类名。

## style绑定
1. `v-bind`：`:style="{color: data, fon-size: data}"`
2. 样式对象写法：`:style="styleObject"`其中styleObject是一个样式对象。
3. 数组写法：`:style=[styleObj1, styleObj2]`,两个样式对象同时放到数组中

## 条件渲染

- v-if,v-else-if,v-else,v-show

## 列表渲染

- v-for,对象数组遍历
- 对象和数组更改检测注意事项

## 事件处理

- v-on,@事件名称="方法名称(parm1, parm2)"。

- 事件修饰符，比如阻止冒泡`stop`，取消默认行为`prevent`。

- 按键修饰符，@keyEvent.按键修饰符="方法名称"。

## 表单输入绑定

## Vue交互

- 交互，也就是数据交互
- Jquery: $.ajax
- js :axios
- vue :vue-resource

## 路由

- 更加网址不同，返回不同的内容给用户
- `<router-view/>`显示的是当前路由地址对应的内容

## 双向数据绑定原理

1. 实现原理：`defineProperty`
2. 实现过程：`@input :value`

## 全局组件和局部组件

1. 全局组件也就是公共组件，全局组件能被所有的组件使用。
2. 局部组件只能在已经挂载的组件上使用，使用方式是：声明局部组件，挂载局部组件，使用局部组件。

## 父组件通信到子组件

1. 在父组件中，先绑定`:自定义的属性 = posts`
2. 子组件要声明`posts:['自定义属性名']`来接收
3. 收到了就是自己的了，可以任意使用

## 过滤器

1. 过滤器的作用：对当前的数据添油加醋。

2. 分为全局过滤器和局部过滤器。声明的方式和局部组件和全局组件类似。
```js
// 全局
Vue.filter('myReverse', function(value，arg1) {
  return value.split('').reverse().join('');
})
// 局部
var app = {
  filter: {
    myReverse(value，arg1) {
      return value.split('').reverse().join('');
    }
  }
}
```
3. 使用方式：{{数据属性 | 过滤器的名字}}, v-bind:属性="数据属性 | 过滤器的名字"

## 组件的生命周期
beforeCreate
created
beforeMount
mounted
beforeUpdate
updated
activated
deactivated
beforeDestroy
destroyed


