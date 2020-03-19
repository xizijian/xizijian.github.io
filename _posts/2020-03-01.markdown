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
 * 回文是指类似于“上海自来水来自海上”或者“madam”，从前往后和从后往前读，字符串的内容是一样的，称为回文。判断一个字符串是否是回文有很多种思路：
 1.利用Array.reverse()反转数组特性
 ```python
       isPalindRome = (str)=>{
             console.log(str.split('').reverse().join('') === str);
             return str.split('').reverse().join('') === str;
       }
   ```  
 2.循环遍历对比
 ```python
        function isPalindRome(str) {
            let newStr = '';
            for(let i = str.length - 1; i >= 0; i --){
                newStr = newStr + str[i];
        
            }
            return newStr === str;
        
        }
        
        console.log(isPalindRome('madam'));//ture
        console.log(isPalindRome('mada'));//false
  ```  
 
