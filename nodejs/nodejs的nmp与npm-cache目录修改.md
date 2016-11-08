### nmp与npm-cache目录修改

下载安装：https://nodejs.org/en/

默认安装完node.js后会自己安装npm，通过npm下载全局模块默认安装到 `C:\Users\wangyc\AppData\Roaming` 目录下，主要有两个文件夹：`npm`、`npm-cache`   
npm：下载的具体模块
npm-cache：npm的缓存文件

如果需要修改此两个文件的目录，甚至将将这两个文件拷贝到无法连网的机器上呢？
使用命令：

```c
npm config set prefix "D:\nodejs\npm" npm config set cache "D:\nodejs\npm-cache"
```

由于node全局模块大多数都是提供命令行访问的，所以还要把 `D:\nodejs\npm` 加到系统PATH里面，注意同时需要将以前的默认路径从PATH中删除。

###  修改npm库

淘宝针对国内下载npm库缓慢的问题，使用建立自己的cnpm库，可以很方便使用在公司内部使用。  
地址：http://npm.taobao.org/

使用淘宝的NPM库镜像

```c
$ npm install -g cnpm --registry=http://registry.npm.taobao.org
```
