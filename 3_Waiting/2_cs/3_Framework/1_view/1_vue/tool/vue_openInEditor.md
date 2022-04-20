

参考：https://www.jianshu.com/p/ad0f42c0541c

终端执行：

```
npm install launch-editor-middleware -d
```

编辑`webpack.dev.conf.js`：

```
const openInEditor = require('launch-editor-middleware');

devServer: {
  ....
  before (app) {
    /**
    * 我使用的是Visual Studio Code 所以这边传的编辑器类型是code
    * 编辑器类型在文章下面了，自己找吧。
    */
    app.use('/__open-in-editor', openInEditor('code'))
  }
}

```

编辑器类型：下面第一个code对应上面的`openInEditor('code')`
code	Visual Studio Code
sublime	Sublime Text
webstorm	WebStorm



2021/6/25 16:11:44 试了一下 不太行