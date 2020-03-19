---
layout:     post
title:      "随笔---基础知识记录"
subtitle:   "Basic knowledge of records"
date:       2020-03-01
author:     "Mr.Xi"
header-img: "img/post-bg-universe.jpg"
catalog:    true
tags:
    - ES6、ES7、ES8
    - React 
    - Web 
    - 前端 
---

## 前言

>记录工作中遇到的小知识点。

##### 1.JS中Map和ForEach的区别
 * forEach(): 针对每一个元素执行提供的函数(executes a provided function once for each array element)。
   map(): 创建一个新的数组，其中每一个元素由调用数组中的每一个元素执行提供的函数得来(creates a new array with the results of calling a provided function on every element in the calling array)。
   到底有什么区别呢？forEach()方法不会返回执行结果，而是undefined。也就是说，forEach()会修改原来的数组。而map()方法会得到一个新的数组并返回。
 1.forEach实例
 ```python
      forEachAry(){
              let arr = [1,2,3,4,5]
              arr.forEach((item,index)=>{
                  return arr[index] = item*2;
              })
              console.log('forEachAry:',arr)
          }
   ```  
   打印结果：
   ```python
         forEachAry: (5) [2, 4, 6, 8, 10]
      ``` 
   
 2.map实例
 ```python
          let arr = [1,2,3,4,5];
                let newArr = arr.map((item)=>{
                    return item*2;
                })
                console.log('mapAry:',newArr)
  ```  
  打印结果：
  ```python
           mapAry: (5) [2, 4, 6, 8, 10]
  ```  
  执行速度对比：上forEach()的执行速度比map()慢了70%。每个人的浏览器的执行结果会不一样。
  函数式角度的理解
  
  如果你习惯使用函数是编程，那么肯定喜欢使用map()。因为forEach()会改变原始的数组的值，而map()会返回一个全新的数组，原本的数组不受到影响。
  
  哪个更好呢？
  
  取决于你想要做什么。
  
  forEach适合于你并不打算改变数据的时候，而只是想用数据做一些事情 – 比如存入数据库或则打印出来。
  
  map()适用于你要改变数据值的时候。不仅仅在于它更快，而且返回一个新的数组。这样的优点在于你可以使用复合(composition)(map(), filter(), reduce()等组合使用)来玩出更多的花样。
    
  核心要点
  
  能用forEach()做到的，map()同样可以。反过来也是如此。
  map()会分配内存空间存储新数组并返回，forEach()不会返回数据。
  forEach()允许callback更改原始数组的元素。map()返回新的数组。
