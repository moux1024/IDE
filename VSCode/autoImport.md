# 关于自动完成同时自动引入模块的功能
> 有位大佬在vscode的issue里暴跳,说默认启用的autoImport浪费了他4个小时,答复推测他启用了ts插件的autoImport功能并建议他关闭,和我遇到的情况略有区别,不过实质上是一样的.

## 症状
在自动完成 `log` -> `console.log()`时,会`import log from "xxx"`,`setTimeout`同理

## 解决办法
在settings.json中加入`"vetur.completion.autoImport": false,`即可,最新版vscode即时生效,如未生效,请在 [ 设置 ] 里搜索autoImport,并禁用对应插件的import功能

