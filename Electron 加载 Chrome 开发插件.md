在 Electron 的开发过程中可以使用专门为 Chrome 开发的扩展插件，这样可以极大的提高页面 Debug 的效率。接下来看一下如何在 Electron 中使用这些扩展插件。

## 下载扩展插件

要想使用这些插件，首先要在自己的 Chrome 浏览器中安装这些插件，然后在 Chrome 的扩展程序页面 `chrome://extensions` 下找到刚下载的扩展，每一个扩展都以一个专属的 ID ，记住这个扩展的 ID。

## 查找扩展路径

接下来需要找到扩展的在本地磁盘的路径:

- 在 Windows 下 Chrome 扩展的路径一般为 `C:\Users\username\AppData\Local\Google\Chrome\User Data\Default\Extensions\` 或者 `%LOCALAPPDATA%\Google\Chrome\User Data\Default\Extensions`
- 在 Linux 下为 `~/.config/google-chrome/Default/Extensions/`
- 在 macOS 下为 `~/Library/Application Support/Google/Chrome/Default/Extensions`

具体的路径可能在不同的系统和软件版本之间有差异，可以自行搜索。然后在目录下找到刚才的 ID 值一样的文件夹，这个文件夹就是扩展的安装路径。

## 加载扩展

在 Electron 中使用 `BrowserWindow.addDevToolsExtension(devToolsUrl)` 来加载扩展，`devToolsUrl`为扩展的安装路径 。例如加载 Windows 中的 Chrome 扩展 :

``` javascript
const devToolsUrl = 'C:\\Users\\username\\AppData\\Local\\CentBrowser\\User Data\\Default\\Extensions\\nhdogjmejiglipccpnnnanhbledajbpd\\3.1.2_0'

function createWindow () {
  win = new BrowserWindow({
    width: 800,
    height: 600,
  })

  win.loadURL(url.format({
    pathname: path.join(__dirname, 'index.html'),
    protocol: 'file:',
    slashes: true
  }))

  win.webContents.openDevTools()
  // 加载扩展
  BrowserWindow.addDevToolsExtension(devToolsUrl)

  win.on('closed', () => {
    win = null
  })
}
```

这样就可以在 Electron 的开发工具中使用 Chrome 的扩展。

## 其他

现在 Electron 官方只支持部分 Chrome 扩展，具体信息可以查看此[链接](https://electron.atom.io/docs/tutorial/devtools-extension/#supported-devtools-extensions)。

