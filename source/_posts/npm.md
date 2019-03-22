---
title: npm
date: 2019-03-22 11:31:07
tags:
---

###  查看npm版本

```shell
npm -v
```

### 安装最新的官方测试版本

```shell
npm install npm@latest -g
```

### 安装将来发布的版本

```shell
npm install npm@next -g
```

### 防止权限错误

原因，官网下载的node.js会默认把npm安装在有全局访问权限的目录中

1.使用nvm重新安装npm

2.手动更改npm的安装目录

```shell
mkdir ~/.npm-global
npm config set prefix '~/.npm-global'
export PATH=~/.npm-global/bin:$PATH
source ~/.profile
```

### 管理本地安装的npm包

创建一个package.json文件

```shell
npm init
```



必须具备 "name"和"version"

```json
{
    "name": "my-package",
    "version": "1.0.0"
}
```

#### 指定依赖关系

dependencies : 您的应用程序在生产中需要这些包

devDependencies : 这些包仅用于开发和测试

```json
{
    "name": "my-package",
    "version": "1.0.0",
    "dependencies": {
        "my-dep": "1.0.0"
    },
    "devDependencies": {
        "my-test-framework": "3.0.0"
    }
}
```

更简单的方法添加依赖

添加到package.json文件的dependencies

```shell
npm install <package-name> --save
```

添加到package.json文件的devDependencies

```shell
npm install <package-name> --save-dev
```

### 更新本地安装的包

1. 在package.json文件所在的目录中执行

   ```shell
   npm update
   ```

   

2. 执行一下命令不会有任何输出

   ```shell
   npm outdated
   ```

### 卸载本地安装的包

删除node_modules目录下面的包

```shell
npm uninstall <package-name>
```

从package.json文件中删除依赖

```shell
npm uninstall <package-name> --save
npm uninstall <package-name> --save-dev
```

### 安装全局的包

```shell
npm install <package-name> -g
```

### 更新全局的包

更新指定的全局包

```shell
npm update -g <package-name>
```

找出需要更新的所有全局包

```shell
npm outdated -g --depth=0
```

更新所有全局包

```shell
npm update -g
```

### 卸载全局包

```shell
npm uninstall -g <package-name>
```



