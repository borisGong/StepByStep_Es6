## StepByStep_Es6

该工程的主要目的是快速搭建一个Es6环境 , 具体步骤如下

1. 首先创建工程目录

* src文件夹 : 存放js源文件
* dist文件夹 : 存放编译后js文件

2. 创建文件

* index.js : 在src文件下面创建index.js

``` 
let t = 1;
console.log(t);
``` 

* index.html ：在root目录创建index.html文件 ，使用<script src="./dist/index.js"></script>引用js
``` 
  <!DOCTYPE html>
  <html lang="en">
      <head>
          <title></title>
          <meta charset="UTF-8">
          <meta name="viewport" content="width=device-width, initial-scale=1">
          <script src="./dist/index.js"></script>
      </head>
      <body>
          Hello ECMA Script 6
      </body>
  </html>
``` 

2. 安装环境

* npm初始化工程: npm init (root目录下面生成package.json)
* 安装babel-cli ：npm install -g babel-cli
* 安装babel-preset-es201,babel -cli : npm install --save-dev babel-preset-es2015 babel-cli 
* 创建.babelrc
``` 
{
    "presets":[
        "es2015"
    ],
    "plugins":[]
}
``` 
* 终端输入babel src/index.js -o dist/index.js ，既可完成
* 如果想让命令简单可以在package中的配置：

```
{
  "name": "stepbystep_es6",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "build": "babel src/index.js -o dist/index.js"
  },
  "repository": {
    "type": "git",
    "url": "git+https://github.com/borisGong/StepByStep_Es6.git"
  },
  "author": "",
  "license": "ISC",
  "bugs": {
    "url": "https://github.com/borisGong/StepByStep_Es6/issues"
  },
  "homepage": "https://github.com/borisGong/StepByStep_Es6#readme",
  "devDependencies": {
    "babel-cli": "^6.26.0",
    "babel-preset-es2015": "^6.24.1"
  }
}

```

