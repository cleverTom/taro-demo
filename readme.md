1. (iconfont不打包)在app.tsx中引用了styles中的iconfont文件, 静态资源并没有打包到最外层的static文件夹中;

2. (iconfont引用线上会被taro处理为scss文件) 如果你把icon.scss改为线上的地址,你会发现被taro编译成了url(xxx.scss)文件, 打开静态资源处理会处理掉我的线上引用, 可以看dist/app.wxss中的iconfont的引用;

taro info
Node: 11.1.0 - ~/.nvm/versions/node/v11.1.0/bin/node
Yarn: 1.15.2 - ~/.nvm/versions/node/v11.1.0/bin/yarn
npm: 6.10.3 - ~/.nvm/versions/node/v11.1.0/bin/npm