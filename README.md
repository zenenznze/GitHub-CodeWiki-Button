# GitHub CodeWiki Button  
# GitHub CodeWiki 按钮  

Add a `CodeWiki` button to GitHub repository pages. Instantly jump to the corresponding CodeWiki page.  
在 GitHub 仓库页面添加一个 `CodeWiki` 按钮. 一键跳转到对应的 CodeWiki 页面。  

**Example URL Mapping · 示例跳转格式**

```text
https://github.com/google-gemini/gemini-cli
→ https://codewiki.google/github.com/google-gemini/gemini-cli
````

---

## One click install · 一键安装脚本

> Replace `your-username` with your real GitHub username.
> 请把下面链接中的 `your-username` 改成你自己的 GitHub 用户名。

[👉 Click here to install via Tampermonkey · 点此一键安装脚本](https://raw.githubusercontent.com/zenenznze/GitHub-CodeWiki-Button/refs/heads/main/codewiki-github-button.user.js)

If Tampermonkey is installed, opening the link above will trigger the install prompt automatically.
如果已经安装了 Tampermonkey, 打开上述链接会自动弹出安装窗口。

---

## Features · 功能简介

* Detect whether the current page is a GitHub repository page
  自动识别当前页面是否为 GitHub 仓库页面
* Parse `user` and `repo` from the URL path
  从地址栏中解析出 `user` 和 `repo` 信息
* Inject a `CodeWiki` button into the repository header area
  在仓库头部操作区域插入一个 `CodeWiki` 按钮
* Clicking the button opens

  ```text
  https://codewiki.google/github.com/{user}/{repo}
  ```

  按钮点击后跳转到上面的 CodeWiki 地址格式
* Compatible with GitHub PJAX and SPA navigation. the script watches DOM and URL changes and re injects the button when needed
  适配 GitHub 的单页应用和 PJAX 行为. 通过监听 DOM 和地址变化, 确保按钮始终存在

---

## Installation · 安装方法

### Method 1 . Use the one click link above

### 方法一 . 用上面的“一键安装”链接

1. Make sure Tampermonkey or another userscript manager is installed
   确保浏览器已安装 Tampermonkey 或其他油猴脚本管理器
2. Click the install link above
   点击上面的脚本安装链接
3. Tampermonkey will open an install page. click `Install`
   Tampermonkey 会打开安装页面, 点击 `安装`

### Method 2 . Manual install

### 方法二 . 手动安装

1. Open Tampermonkey icon. choose `Create a new script`
   点击浏览器中的 Tampermonkey 图标, 选择 `添加新脚本`
2. Delete the default template code
   删除默认模板代码
3. Copy all content of `codewiki-github-button.user.js` into the editor
   将 `codewiki-github-button.user.js` 文件的全部内容复制进去
4. Save. then refresh any GitHub repository page
   保存后刷新任意 GitHub 仓库页面

---

## Usage · 使用说明

1. Open any GitHub repository page
   打开任意 GitHub 仓库页面
   例如 `https://github.com/google-gemini/gemini-cli`
2. You will see a new `CodeWiki` button in the repository header area
   在仓库顶部操作区域会多出一个 `CodeWiki` 按钮
3. Click it to open the corresponding CodeWiki page in a new tab
   点击按钮, 会在新标签页打开对应的 CodeWiki 页面

实际跳转地址为:

```text
https://codewiki.google/github.com/{user}/{repo}
```

---

## Project structure · 项目结构

```text
github-codewiki-button/
├─ README.md                         # Repository description 仓库说明文档
├─ LICENSE                           # License 许可证, 推荐 MIT
└─ codewiki-github-button.user.js    # Core userscript file 核心用户脚本文件
```

---

## License · 许可证

This project is licensed under the MIT License.
本项目使用 MIT License 开源. 详情见 `LICENSE` 文件。

