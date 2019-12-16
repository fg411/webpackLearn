# webpack 练习

>练习webpack文档实例，标记一些常用知识点和之前没注意到的知识点

## 起步

## 管理资源

>webpack 根据正则表达式，来确定应该查找哪些文件，并将其提供给指定的 loader。示例中，所有以 .css 结尾的文件，都将被提供给 style-loader 和 css-loader

依赖包：

 - style-loader 和 css-loader
 - file-loader
 - csv-loader 和 xml-loader

## 管理输出

依赖包

 - html-webpack-plugin
 - clean-webpack-plugin

## 开发环境

 - 使用 source map
 - webpack watch mode
 - webpack-dev-server
 - webpack-dev-middleware）

`webpack watch mode`: 自动地重新编译修改后的模块,需要刷新浏览器

`webpack-dev-server` 在编译之后不会写入到任何输出文件。而是将 `bundle` 文件保留在内存中，然后将它们 `serve` 到 `server` 中，就好像它们是挂载在 `server` 根路径上的真实文件一样。如果你的页面希望在其他不同路径中找到 `bundle` 文件，则可以通过 `dev server` 配置中的 `publicPath` 选项进行修改

`webpack-dev-middleware` 是一个封装器`(wrapper)`，它可以把 `webpack` 处理过的文件发送到一个 `server`。 `webpack-dev-server` 在内部使用了它，也可以作为一个单独的 `package` 来使用，以便根据需求进行更多自定义设置