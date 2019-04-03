---
title: gradle
date: 2019-04-03 16:21:44
tags:
---

### gradle 依赖方式

旧的 `compile` `provided` `apk` `testCompile` `debugCompile` `releaseCompile`

现在 `implementation` `api` `compileOnly` `runtimeOnly` `unitTestImplementation` `testImplementation`  `debugImplementation` `releaseImplementation`

### 区别

##### implementation和api

`implementation`和`api`取代之前的`compile`,`api`和`compile`是一样的,`implementation`有所不同，通过`implementation`依赖的库只能自己库本身访问

##### compile only

`compileOnly`和`provided`效果一样，不参与打包

##### runtime only

`runtimeOnly`和`apk`一样，只在打包的时候有效，编译不参与

##### test implement

`testImplementation`和`testCompile`一样，在单元测试的时候和打包测试apk的时候有效

##### debugImplementation

`debugImplementation`和`debugCompile`效果一样,在`debug`模式下有效

##### release implementation

`releaseImplementation`和`releaseCompile`效果相同,只在`release`模式和打包`release`包情况下有效

