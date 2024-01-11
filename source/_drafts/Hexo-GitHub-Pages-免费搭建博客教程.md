---
title: Hexo + GitHub Pages 免费搭建博客教程
tags:
  - 教程
date: 2024-01-11 15:05:07
---

这两天我用 GitHub Pages 和 Hexo 博客引擎搭建了一个个人博客，期间走了不少弯路。现在把经验分享给大家，希望能帮助大家少走弯路，搭建起属于自己的免费博客。

## 1.搭建 Hexo 博客

### 1.1.安装 Hexo

#### 1.1.1.安装 Git 和 Node.js

{% note info %}
如果您已安装了这两个软件，您可以跳过本章节，阅读1.1.2。
{% endnote %}

Git 是一款源代码管理工具，Hexo 需要它运行。在[这里](https://git-scm.com/downloads)下载你对应系统和版本的 Git。

下载完成后运行安装程序，根据指示完成安装。安装完成后在命令行执行

```batch
git --version
```

输出形如 `git version 2.36.0.windows.1` 的结果，说明安装成功。

---

Hexo 需要 Node.js 运行，因此我们还要下载 [Node.js](https://nodejs.org/en)，按指示完成安装。安装完成后在命令行执行

```batch
node -v
```

输出形如 `v20.10.0` 的结果，说明安装成功。同时要记录下此时输出的版本中第一位小数点前的数字，下文备用。

#### 1.1.2. 安装 Hexo

安装好所有必须程序后，我们现在开始安装 Hexo。

在命令行中执行

```batch
npm install -g hexo-cli
```

安装 Hexo 博客引擎和命令行工具。

{% fold info @如果你坚持使用旧的 Node.js…… %}
你可以考虑安装 Hexo 的过去版本。但请注意，目前官方已停止提供对过去版本 Hexo 的错误修复。

我强烈建议永远安装[最新版本](https://www.npmjs.com/package/hexo?activeTab=versions)的 Hexo，以及[推荐的 Node.js 版本](https://hexo.io/zh-cn/docs/#%E5%AE%89%E8%A3%85%E5%89%8D%E6%8F%90)。

Hexo 版本范围与 Node.js 的版本范围如下表所示

| Hexo 版本范围   | Node.js 版本范围     |
| ----------- | ---------------- |
| 7.0+        | 14.0.0+          |
| 6.2+        | 12.13.0+         |
| 6.0+        | 12.13.0 - 18.5.0 |
| 5.0+        | 10.13.0 - 12.0.0 |
| 4.1 - 4.2   | 8.10 - 10.0.0    |
| 4.0         | 8.6 - 8.10.0     |
| 3.3 - 3.9   | 6.9 - 8.0.0      |
| 3.2 - 3.3   | 0.12 - 未知        |
| 3.0 - 3.1   | 0.10 或 iojs      |
| 0.0.1 - 2.8 | 0.10             |

（本段资料改写自 [Hexo 文档](https://hexo.io/zh-cn/docs/#Node-js-%E7%89%88%E6%9C%AC%E9%99%90%E5%88%B6)）

{% endfold %}
