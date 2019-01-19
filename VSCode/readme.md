# VSCode的setting
> vscode的setting有多处,包括
- user-settings(~/Library/Application Support/Code/User/settings.json)   
- workspace-settings([YOUR PROJECT]/.vscode/settings.json)   
> 打开settings页面,点击界面右上角{}标志,打开settings.json文件,修改后<b>重启VSCode或重载对应的插件</b>即可生效   
以下以我使用的vue项目为例
```js
{
  //tab size
	"editor.tabSize": 2,
  //eslint的配置项
	"eslint.options": {
    // 设置configFile
		"configFile": "./.eslintrc.js"
	},
  //配置保存时自动fix
	"eslint.autoFixOnSave": true,
  //配置生效区域
	"eslint.workingDirectories": [
		"./parcel"
	],
  //和自动fix配合,指定对应的代码类型,如vue的代码
	"eslint.validate": [
		"javascript",
		"javascriptreact",
		"html",
		{
				"language": "vue",
				"autoFix": true
		}
	],
}

```
以上就是通过eslint进行autofix的配置,下面说一下比较简单的通过prettier进行autoformat的配置
```js
{
// Set the default
 "editor.formatOnSave": false,
// Enable per-language
"[vue]": {
		"editor.formatOnSave": true
 },
```
以上是适用于prettier的对vue代码autoformat的配置内容
