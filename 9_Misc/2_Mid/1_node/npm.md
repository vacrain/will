win的.npmrc 在哪

https://zhidao.baidu.com/question/1499004587754875659.html



或者直接改

https://www.cnblogs.com/yiweiyihang/p/8064604.html

安装完node.js并配置环境变量。在cmd窗口检查npm安装是否成功。

安装淘宝npm：

### 1.临时使用

```
npm --registry https://registry.npm.taobao.org install express
```

### 2.持久使用

```
npm config set registry https://registry.npm.taobao.org
```

- 配置后可通过下面方式来验证是否成功 
  `npm config get registry`
- 或 
  `npm info express`

### 3.通过cnpm使用

```
npm install -g cnpm --registry=https://registry.npm.taobao.org
```

- - 使用 
    `cnpm install express`

# win很重要一点！

配置npm全局安装的目录到环境变量中， 查看npm全局安装目录：

```
npm config get prefix
```

用上面的命令，可以查到下面的目录：

```
C:\Users\ys1222\AppData\Roaming\npm
```

在全局变量中添加上面的目录即可，之后就可随处使用npm安装的软件了 ！！！











```
npm WARN bootstrap-switch@3.3.4 requires a peer of bootstrap@^3.1.1 but none is installed. You must install peer dependencies yourself.
npm WARN ejs-html-loader@3.1.0 requires a peer of webpack@2.x - 3.x but none is installed. You must install peer dependencies yourself.
npm WARN metronic@6.1.7 No repository field.
npm WARN optional SKIPPING OPTIONAL DEPENDENCY: fsevents@1.2.11 (node_modules\fsevents):
npm WARN notsup SKIPPING OPTIONAL DEPENDENCY: Unsupported platform for fsevents@1.2.11: wanted {"os":"darwin","arch":"any"} (current: {"os":"win32","arch":"x64"})

up to date in 15.256s

45 packages are looking for funding
  run `npm fund` for details

PS F:\jimzen_workspace_web\tools> npm install

> node-sass@4.13.1 install F:\jimzen_workspace_web\tools\node_modules\node-sass
> node scripts/install.js

Cached binary found at C:\Users\ys1222\AppData\Roaming\npm-cache\node-sass\4.13.1\win32-x64-72_binding.node

> core-js@2.6.11 postinstall F:\jimzen_workspace_web\tools\node_modules\core-js
> node -e "try{require('./postinstall')}catch(e){}"

Thank you for using core-js ( https://github.com/zloirock/core-js ) for polyfilling JavaScript standard library!

The project needs your help! Please consider supporting of core-js on Open Collective or Patreon: 
> https://opencollective.com/core-js 
> https://www.patreon.com/zloirock 

Also, the author of core-js ( https://github.com/zloirock ) is looking for a good job -)


> preact@8.2.9 postinstall F:\jimzen_workspace_web\tools\node_modules\preact
> node -e "console.log('\u001b[35m\u001b[1mLove Preact? You can now donate to our open collective:\u001b[22m\u001b[39m\n > \u001b[34mhttps://opencollective.com/preact/donate\u001b[0m')"

Love Preact? You can now donate to our open collective:
 > https://opencollective.com/preact/donate

> nodemon@1.19.4 postinstall F:\jimzen_workspace_web\tools\node_modules\nodemon
> node bin/postinstall || exit 0


> node-sass@4.13.1 postinstall F:\jimzen_workspace_web\tools\node_modules\node-sass
> node scripts/build.js

Binary found at F:\jimzen_workspace_web\tools\node_modules\node-sass\vendor\win32-x64-72\binding.node
Testing binary
Binary is fine

> ejs@2.7.4 postinstall F:\jimzen_workspace_web\tools\node_modules\ejs
> node ./postinstall.js

Thank you for installing EJS: built with the Jake JavaScript build tool (https://jakejs.com/)

npm WARN metronic@6.1.7 No repository field.
npm WARN optional SKIPPING OPTIONAL DEPENDENCY: fsevents@1.2.11 (node_modules\fsevents):
npm WARN notsup SKIPPING OPTIONAL DEPENDENCY: Unsupported platform for fsevents@1.2.11: wanted {"os":"darwin","arch":"any"} (current: {"os":"win32","arch":"x64"})

added 1801 packages from 918 contributors in 177.282s

45 packages are looking for funding
  run `npm fund` for details

```

