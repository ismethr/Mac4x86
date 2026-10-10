# Release 说明模板

在 x86 仓库发布新版本时，复制下面的内容，替换尖括号里的部分。

```markdown
<软件名> 的非官方 **Intel（x86_64）版本**，基于上游 [<owner>/<repo> <上游版本>](https://github.com/<owner>/<repo>/releases/tag/<上游 tag>)。<软件名> 由 <原作者>开发，以 <许可证> 许可证开源；本版本与原作者无关，有问题请在本仓库反馈。

> Apple 芯片的 Mac 请使用[官方版本](https://github.com/<owner>/<repo>/releases/latest)。

## 本版本更新内容

- …

## 与上游的区别

- 编译为 x86_64，可以在 Intel Mac（macOS <最低版本> 及以上）上运行。
- …

## 安装 / 升级

1. 下载 `<文件名>.zip`，解压后把应用拖进「应用程序」。
2. 本版本没有经过 Apple 公证，第一次打开会被拦下：到「系统设置 → 隐私与安全性」，点「仍要打开」。

SHA-256: `<shasum -a 256 的结果>`

许可证：<许可证>。发布包内附有 LICENSE；对应源码见本 Release 的 tag。

---

Unofficial **Intel (x86_64)** build of <App> by <Author>, <License> licensed; not affiliated with or endorsed by the original author.
```
