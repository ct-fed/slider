title: Node.js简简介
author:
  name: Fancy
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

* Only javascript(只用写js)
* Not only running in browser(不再局限在浏览器里)
* Anything is possible(发挥想象)

--

### 这次分享涉及到的

* Hello World(创建一个文件)
* module(模块)
* npm(包管理机制)
* uglify-js(压缩你的javascript)
* grunt(构建工具)

--

### Hello World

```

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

```

module.exports = {
    say : function(content){
        console.log(content);
    }
};

```

```

var say = require('./modules/say');
say.say('Hello World!');

```
--

### npm

* .../node_modules/node_modules/node_modules/... 
* 安装uglify

```

npm install -g uglify-js

```
--

### uglify-js

```

uglifyjs [ options... ] [ filename ]

```
--

### grunt

* 语法检查(syntax)
* 单元测试(test)
* 合并(concat)
* 压缩(compress)
* 清除缓存(cache)
* 再来一遍...

--

# 重复的工作交给程序来完成！

--

### grunt三步曲

1. initConfig(定义任务)
2. loadNpmTasks(加载依赖插件)
3. registerTask(注册任务指令)

```

module.exports = function(grunt) {

    grunt.initConfig({
        pkg: grunt.file.readJSON('package.json'),
        jshint : {},
        concat : {},
        uglify: {}
    });

    grunt.loadNpmTasks('grunt-contrib-jshint');
    grunt.loadNpmTasks('grunt-contrib-concat');
    grunt.loadNpmTasks('grunt-contrib-uglify');

    grunt.registerTask('default', ['jshint']);
    grunt.registerTask('build', ['jshint', 'concat', ''uglify']);
};

```

--

### 可以做的还很多

* less/sass/stylus
* requireJs
* express + mongoose + mongodb
* ...

--

# 一起来吧！
