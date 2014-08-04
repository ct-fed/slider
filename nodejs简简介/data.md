title: Node.js简简介
author:
  name: Fanzj
  url: http://fancyboy.net/
output: slider.html

--

# Node.js简简介
## 只告诉你路在哪，坑还是要自己填...

--

### Node.js是什么？

Pass...

--

### Node.js能做什么？

Pass...

--
### Node.js对我而言

* Only javascript
* Not only running in browser
* Anything is possible

--

### 这次分享涉及到的

* Hello World(创建一个文件)
* module(模块)
* npm(包管理机制)
* uglify(压缩你的javascript)
* grunt(构建工具)
* express + mongoose + mongodb(建站)

--

### Hello World

```js

var fs = require('fs');
fs.writeFile('HelloWorld.txt', 'Hello World', function (err) {
    if (err){
        throw err;
    }
    console.log('创建成功');
});

```
--
### module

```js

module.exports = {
    say : function(content){
        console.log(content);
    }
};

```

```js

var say = require('./modules/say');
say.say('Hello World!');

```
--

### npm

* .../node_modules/node_modules/node_modules/... 

```cmd

npm install -g uglify

```
--