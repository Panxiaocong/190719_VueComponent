# 自定义Vue开发环境
## 1. 搭建基本开发环境
    1). 下载依赖包
        npm add -D webpack                                          编译打包js
        npm add -D webpack-cli@3.3.12                               提供webpack命令
        npm add -D html-webpack-plugin                              自动引入打包生成的js/css
        npm add -D webpack-dev-server                               启动服务器,修改代码自动刷新
        npm add -D babel-loader @babel/core @babel/preset-env       es6转化es5
        npm add -D css-loader style-loader                          处理css
        npm add -D url-loader@2.3.0 file-loader@4.3.0               处理图片
    
    2). webpack的基本配置: webpack.config.js
        module.exports = {
          mode: 'production|development'
          entry: {

          },
          output: {

          },
          module: {
            rules: [

            ]
          },
          plugins: [

          ],
          devServer: {

          },
          devtool: ''
        }

    3). 区分使用生产环境与开发环境
        使用生产环境:
            npm run build   ==> webpack
            1). 在内存中进行编译打包, 生成内存中的打包文件
            2). 保存到本地(在本地生成打包文件)   ===> 此时还不能通过浏览器来访问, 需要启动服务器运行
        使用开发环境
            npm run dev   ==> webpack-dev-server
            1). 在内存中进行编译打包, 生成内存中的打包文件
            2). 启动服务器, 运行内存中的打包文件   ===> 可以通过浏览器虚拟路径访问



## vue组件化开发
