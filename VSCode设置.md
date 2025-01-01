# VSCode设置
首先找到设置文件`settings.json`，在菜单栏打开`文件`>`首选项`>`设置`，点击右上角`打开设置(json)`即可进入文件。以下为推荐设置。

```jsonc
{
    //不启用工作区信任
    "security.workspace.trust.enabled": false,
    //在没有从上一次会话中恢复出信息的情况下启动时不打开任何编辑器(默认启动时显示欢迎页)
    "workbench.startupEditor": "none",
    //取消显示命令中心(搜索栏)
    "window.commandCenter": false,
    //打开文件时猜测字符集编码
    "files.autoGuessEncoding": true,
    //光标动画样式
    "editor.cursorBlinking": "smooth",
    //编辑器动画
    "editor.smoothScrolling": true,
    //启用平滑插入动画
    "editor.cursorSmoothCaretAnimation": "on"
}
```
