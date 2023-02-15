设置中搜索 Paste Image，配置下必要参数，后面就可以截完图，按Ctrl + ALT + V 直接粘贴图片到md中了

![](assets/vscode%20md%20复制图片/20230131160636.png)

扩展修改：

![](assets/vscode%20md%20复制图片/20230131160717.png)

修改内容如下：
`"pasteImage.path": "${currentFileDir}/assets/${currentFileNameWithoutExt}",
"pasteImage.defaultName": "YMMDDHHmmss"`

截图完毕后，按Ctrl + Alt + V粘贴，插件会自动帮你保存到 配置的pasteImage.path中.