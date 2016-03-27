汽车连锁信息管理系统
===
___
>~~~信老魏，得永生~~~[^1]

[^1]:你信或不信，老魏都在那里，不悲不喜。
技术栈
---
___
####前端
* [bootstrap](http://getbootstrap.com/)
* ![react logo](https://facebook.github.io/react/img/logo.svg =50x) [react](https://facebook.github.io/react/)
* [reactcss](https://github.com/casesandberg/reactcss#readme)
* [react-bootstrap](http://react-bootstrap.github.io/)

####后端
* ![nodejs logo](https://nodejs.org/static/images/logos/nodejs-new-white-pantone.png =100x) [nodejs](https://nodejs.org/en/)
* [express](http://expressjs.com/)
* ![mongodb logo](https://www.mongodb.org/assets/global/mongodb-logo-web-tagline-99280fe76cc002a93d023901c1a05df8b621f1c893084a580dee83de9be96630.png =100x) [mongodb](https://www.mongodb.org/)
* [mongoose](http://mongoosejs.com/)

####工具
* ![npm logo](https://www.npmjs.com/static/images/npm-logo.svg =150x) [npm](https://www.npmjs.com/)
* ![Webpack logo](https://webpack.github.com/assets/logo.png =150x) [webpack](https://github.com/webpack/webpack)
* ![Nginx logo](http://nginx.org/nginx.png =150x) [nginx](http://nginx.org/)
  
##遇到的问题及解决办法
___
1. `react`中创建的类首字母必须**大写**  
   在定义或者引入`react`的类时，首字母必须大写，因为babel在处理过程中，会把类名转换为小写，如果首字母小写，就会找不到定义的类。
2. `webpack`版本6使用`babel-loader`,必须引入`babel-preset-es2015`和`babel-preset-react`。
3. `npm`安装全局包出现权限问题  
   通过在命令行运行`sudo chown -R $(whoami) $(npm config get prefix)/{lib/node_modules,bin,share}`，可以解决此问题。
4. `npm`

##用到的ES6语法
___
1. 箭头函数  
   `=>(x, y) { return x+y; }`等同于`function (x, y) { return x+y;}.bind(this)`。 
2. 解构赋值  
   `import React from 'react';`  
   `let { Button, List } = React;` 等同于  
   `let Button = React.Button, List = React.List`，  
   `let [x,y] = [y,x]` 等同于  
   `let tmp = x; x = y; y = tmp`。
3. 变量定义  
   使用`let`定义局部变量，使用`const`定义常量。
4. 


##数据格式
___
+ ####分类数据格式  

m            | Second Header | Third Header
------------ | ------------- | ------------
Content Cell | Content Cell  | Content Cell
Content Cell | Content Cell  | Content Cell    

```
var Catagory = {
	displayName: 'Level1 cata',
	key: '00',
	subCatagory: []
};
```   
+ ####仓库数据格式   
必须要有空行吗？
 
```
var Storage = {
	name: String,
	id: ID,
	catagory: String
};
```	