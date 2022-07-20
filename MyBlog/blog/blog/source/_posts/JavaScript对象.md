---
title: JavaScript对象
date: 2022-07-07 19:41:21
tags:
- JavaScript
categories:
- 前端组
cover: https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fp.cdn.sohu.com%2Fbc4e413e%2Fc8d120dfacc6cf91e861b5b9b0f14624.jpeg&refer=http%3A%2F%2Fp.cdn.sohu.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=auto?sec=1659877301&t=937bcfcda9286bda709a7e6cb9fa1392
coverWidth: 1200
coverHeight: 320
author: xiguayaaaaa
from: 
---
JavaScript对象
<!--more-->


+ 什么是对象
  + 对象是一种复合值，它汇聚多个值（原始值或者是其它对象），并且允许我们按照名称存储和获取这些值。
  + 对象是一个属性无序的集合，每个属性都有自己的名字和值，只有在对象中，其使用起来与顺序无关，只需要打点即可调用。
  + 在JavaScript中对象可以从其它对象继承属性。
  + JavaScript对象是动态的，即可以动态的添加和删除对象属性。
+ 认识对象
  + 创建自定义对象我们可以通过创建Object实例来实现，然后再给他添加属性和方法（函数）
  ```html
  	<script>
		let person = new Object();
		person.name = "zhangsan";
		person.age = 18;
		person.job = "Teacher"; 
		console.log(this.name+"，年龄"+this.age+"岁，他的工作是："+this.job);
		person.work = function(){}
		---
		let person = {
		name = "zhangsan",
		age = 18,
		job = "Teacher",
		work(){
		console.log(this.name+"，年龄"+this.age+"岁，他的工作是："+this.job);
		}
		}
		</script>
  ```

+ 属性的类型

  + JavaScript使用了一些内部特性来描述属性的特征，这些特性由JavaScript实现引擎的规范定义的，所以开发者不能直接在JavaScript中访问这些访问。

  + 属性特性分两种

    + 数据属性

      + 数据属性包含一个保存数据值得位置，数据的值会从这个位置中读取，当然也可以写入到这个位置，数据属性有4个特性描述他的行为

        + 【Configurable】：表示属性是否可以通过delete删除并重新定义，是否可以修改它的特性，以及是否可以把它改为访问器属性。其默认情况下为true
        + 【Enumerable】：表示属性是否可以通过for-in循环返回，默认情况也为true
        + 【Writable】：表示属性的值是否可以被修改，其默认值为true
        + 【Value】：包含属性的实际值，其默认值为undefined

      + 这些属性特性我们在定义对象时并不需要显式的添加前三个，而Value特性也会被我们定义，如：name:"zhangsan"

      + 如果想要修改这些默认特性，就必须使用Object.defineProperty()方法，这个方法在使用时接收三个参数：要给其添加属性的对象，属性的名称，以及一个描述特性的对象及其参数

    + 示例
    ```html
    <!DOCTYPE html>
        <html lang="en">
        <head>
         <meta charset="UTF-8">
         <title>Title</title>
         <script>
         let person = {};
         Object.defineProperty(person,"name",{
         writable:false,
         value:"王麻子"
         });
         console.log(person.name);
         person.name = "张金条";
         console.log(person.name);
         </script>
        </head>
        <body>
        </body>
        </html>
        <html lang="en">
        <head>
         <meta charset="UTF-8">
         <title>Title</title>
         <script>
         let person = {};
         Object.defineProperty(person,"name",{
         // configurable:true,
         configurable:false,
         value:"王麻子"
         });
         console.log(person.name);
         delete person.name;
         console.log(person.name);
         </script>
        </head>
        <body>
        </body>
        </html>
    ```
    + 访问器属性

      + 访问器属性不包含数据值，它包含一个获取（getter）函数以及一个设置 （setter）函数，不过这两个函数并非必须函数。

      + 在读取访问器属性时，程序会自个调用获取函数，也就是说获取函数的主 要任务就是返回一个有效的值

      + 访问器属性也有4个特性用了描述它们的行为
        + 【Configurable】，默认值为true，表示能否通过delete删除属性从而重新定义属性，能否修改属性的特性，能否把属性修改为访问器属性
        + 【Enumerable】，默认值为true，能否通过for-in循环返回属性
        + 【get】读取这个属性时调用的函数 getter函数
        + 【set】在为这个属性赋值时调用的函数 setter函数

     + 以上这些属性也是不能直接定义的，必须通过Object-defineProperty()
	```html
    			<html lang="en">
   	 			<head>
   	 			<meta charset="UTF-8">
   	 			<title>Title</title>
   	 			 <script>
   	 			 		let book = {
   	 			 		name:"七侠五义",
   	 			 		price:1
   	 			 		};
   	 			 		book.name = "斗破苍穹";
   	 			 		console.log(book.name);
   	 			 		Object.defineProperty(book,"name",{
   	 			 		get(){
							 return this.name;
						},
						set(newValue){
							this.name = newValue;
							}
						});
					</script>
					</head>
					<body>
					</body>
					</html>
  ```


+ 对象合并
  +  在开发JavaScript时我们会把多个对象合并使用
  +  具体来说就是把一个对象的所有属性复制到了目标对象上，这种方式也被称之为混入，通过对象的合并我们可以增强对象功能
  +  JavaScript专门为合并对象提供了一个Object.assign()方法，这个方法接收一个目标对象和一个或多个其它对象（源对象），然后将每个源对象中自有属性复制到目标对象
  ```html
		<html lang="en">
		<head>
		<meta charset="UTF-8">
		<title>Title</title>
		<script>
			//目标对象
			Obj1 = {name:"老八"};
			//源对象
			Obj2 = {name:"老八"};
			//把2复制到目标对象中
			result = Object.assign(Obj1,Obj2);
			console.log(Obj1 === result)
			console.log(Obj2 === result)
			console.log(result)
		</script>
		</head>
		<body>
		</body>
		</html>
	```
+ 增强的对象语法

  + ES6位对象定义了很多定义对象及其操作对象的语法特性，这些特性可以极大程度提高对象处理的方便程度

  + 属性值得简写

    + 在给对象添加值时我们可以引用变量
    ```html
			<script>
				let username= "sanlvzi";
				let person = {
				username:username
				};
				console.log(person)
			</script>
    ```
    + 还能简写（以下这种情况必须时变量名域对象的属性名相同才可以这么写）
    ```html
		<script>
		let username= "sanlvzi";
		username
		};
		let person = {
		console.log(person)
		</script>
    ```