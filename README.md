2020-06-22

#### MVC和MVVM
mvc指的是view，model和controller;v通知c，c再控制m;m再反映到v;他们的通信都是单向的；mvvm是指model view 和viewmodel view的变化会反映在viewmodel上viewmodel和model间是双向通信；
#### ajax contentType
在请求携带较为复杂的数据时候（比如对象中嵌套的有数组时）需要把数据用JSON.stringify()方法序列化后再发送；
#### felx
外部盒子displey：flex;内部盒子元素可以设置，设为 Flex 布局以后，子元素的float、clear和vertical-align属性将失效。容器的flex-direction属性决定主轴的方向（即项目的排列方向）。
#### 箭头函数this指向
它会捕获其所在（即定义的位置）上下文的this值， 作为自己的this值，

```javascript
  let nkyName="王麻子";
  const person1 = {
    nkyName: "张三",
    sayHi: ()=>{
      console.log(`Hi,${this.nkyName}`);//这里输出undefined 箭头函数的this继承的是父执行上下文里面的this；父执行是person1；父执行上下文是window;let不会挂载在window上
    }
  };
```

#### 解构赋值
```javascript
  const obj ={a:1，b:2};
  const {a,b} = obj;
  const {a:c,b:d}=obj://将a的值赋值给变量c，b的值赋值给变量d；
  //在函数里面也一样；
  function fun ({a,b}){
    conosole.log(a,b)// 1,2
  }
  fun(obj)
```

#### Object的一些应用

```javascript
const obj = {
    start:'开始',
    end:'结束',
    stop:'停止',
}
if(value ==='start'){
    console.log(`发送的是；开始`)
}else if(value ==='end'){
    console.log(`发送的是；结束`)
}else{
    console.log(`发送的是；停止`)
}
//上面的判断可以直接用优化为
//可以看出某些情况下适用数组来代替也是同理的优化代码
console.log(`发送的是${obj[value]}`)
```

