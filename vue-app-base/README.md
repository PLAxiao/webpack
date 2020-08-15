# vue-app-base
# Project setup
yarn

# Compiles and hot-reloads for development
yarn serve

# Compiles and minifies for production
yarn build

# Lints files
yarn lint

# Lints and fixes files

yarn lintfix
1. 这是一个使用 Vue CLI 创建出来的 Vue 项目基础结构
2. 有所不同的是这里我移除掉了 vue-cli-service（包含 webpack 等工具的黑盒工具）
3. 这里的要求就是直接使用 webpack 以及你所了解的周边工具、Loader、Plugin 还原这个项目的打包任务
4. 尽可能的使用上所有你了解到的功能和特性

一、简答题
1、Webpack 的构建流程主要有哪些环节？如果可以请尽可能详尽的描述 Webpack 打包的整个过程。
        从配置文件和命令行获取参数
        创建Complier对象
        执行Compiler的run方法创建Compliation
        寻找入口文件，调用所有配置的loader对所有模块进行编译。
        经loader编译完后得到每个模块最终内容及依赖关系。
        根据入口和模块依赖关系，组装包含多模块的chunk，把每个chunk转换成单独文件加入输出列表。这步是修改输出内容的最后机会。


2、Loader 和 Plugin 有哪些不同？请描述一下开发 Loader 和 Plugin 的思路。
  loader专注资源模块的转换和加载（转换代码，校验）
  plugin比较全面，解决一些自动换的HMR,清楚dist目录，拷贝文件等

  