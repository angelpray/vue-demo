# vue问题集

1. data: {}和data: function(){return {}}有什么区别？
答：在组件中，data必须是一个函数，在函数中返回一个对象。在Vue根实例中，data可以是一个函数，在函数中返回对象，也可以直接就是一个对象。

2. v-text和v-html的区别？

3. v-if和v-show的区别？

4. new Vue({})中的this指的是什么？
答：this指向每一个Vue实例本身。

5. 什么是单向数据流？
答： model =>>> view， model驱动view。注意，这是单向的，只能是data变化而导致view变化，但view变化，data不会变化。例子就是：v-bind。

6.什么是双向数据绑定？
答：model <<<=>>> view，相互影响，是双向的。例子就是：v-model。
![](https://image-static.segmentfault.com/411/343/4113434341-5cd4339a9a8b5_articlex)

7. 如何理解MVVM模式？

![MVVM](https://image-static.segmentfault.com/298/848/298848890-5cd1a04b24333_articlex)

8. 理解MVC模式？

9. MVC和MVVM的区别是什么？

10. 什么是动态props？

11. 如何监听复杂数据类型，比如object，array？
深入监视

12.watch和computed有什么区别？
最主要的区别，还是computed可以缓存，watch

13. 如何获取DOM元素？

14. ref属性名可以重复吗？

15. 生命周期中什么时候能获取DOM元素？

16. 编程式导航VS声明式导航？
直接以字符串的是声明式导航，以一些API动态操作导航的是编程式导航。

17. Restful规范？

18. axios的二次封装？

19. v-for中key的作用？
绑定组件一个独立的key，重新渲染
