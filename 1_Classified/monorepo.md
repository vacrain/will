# monorepo 实践总结

> 2022-05-31 看了一些天monorepo，不再观望，做一些demo，然后把steppp整合一下

[toc]



## Env

> 环境准备

1. Node: 16.14.2 ，安装好后，全局安装：
   1. pnpm@7.1.7
   2. vite@2.9.5
   3. commitizen@4.2.4
2. VSCode: 最新版，安装好后，安装插件：
   1. gitlens
   2. tabninie
   3. prettier
   4. ESLint



Npm 命令参考：

```sh
全局安装指定版本：
npm install -g 依赖或软件名@版本号
如：
npm install -g pnpm@7.1.7
```

Pnpm 命令参考

```sh
pnpm查看帮助方式:
pnpm help xxx
如：
pnpm help add

npm命令选项须知：
-r  是每个子包都安装
-D  是安装到dev依赖里
-w  是安装到root，也就是workspace
--filter=包名	指定子项目进行操作
如：
pnpm add vue @vuepress/client@next --filter=site -D

可能用到的命令：
pnpm init -y
pnpm create vue
pnpm add vite vitest typescript -r -D
pnpm add eslint @mistjs/eslint-config-vue -Dw
pnpm add @vue/tsconfig -r -D
pnpm add vue -r
pnpm add vue @vuepress/client@next --filter=site -D
pnpm add vuepress@next --filter=site
```



## common

> 所有项目，新建目录后，都要做的事

1. 初始化项目

```
pnpm init
git init
```

2. 配置项目

- ./package.json

```

```

- ./pnpm-workspace.yaml

```

```

- ./.gitignore

```

```

- 创建目录 ./packages/package1 ， ./packages/package2 ，...



## Demos

> [common](# common) 都做完后，再开始下面的内容

### demo-01

> Fastify + Vue3&Vite2

```

  "husky": {
    "hooks": {
      "pre-commit": "lint-staged",
      "commit-msg": "commitlint -E HUSKY_GIT_PARAMS"
    }
  },
  
  git commit -m"add gitignore"  
```















