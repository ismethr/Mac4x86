# Mac4x86

**给 Intel Mac 用的开源软件：官方只出 Apple 芯片版本的，这里补上 x86_64 版本。**

Apple 已经宣布 macOS 26 Tahoe 是最后一个支持 Intel 的系统，越来越多的开源软件只发布 arm64 版本。本仓库收集这些软件的**非官方** Intel（x86_64）构建，每个软件放在单独的 fork 仓库中，源码、改动和发布记录都可以查看。

> [!IMPORTANT]
> 这里的所有软件都是**非官方构建**，与原作者无关。遇到问题请到对应的 x86 仓库反馈，**不要去打扰上游作者**。
> 用的是 Apple 芯片的 Mac？请直接使用官方版本。

## 软件列表

| 软件 | 简介 | x86 版本 | 上游 | 许可证 | 最低系统 |
| --- | --- | --- | --- | --- | --- |
| Oil Find | macOS 上的 Everything：内存索引文件名，输入即出结果 | [oil-find-x86](https://github.com/ismethr/oil-find-x86/releases/latest) | [oil-oil/oil-find](https://github.com/oil-oil/oil-find) | MIT | macOS 14 |

想要某个软件的 x86 版本？请[提交申请](../../issues/new?template=app-request.yml)，提交前先看[收录规则](docs/POLICY.md#收录标准)。

## 安装须知

这些构建**没有经过 Apple 公证**，第一次打开时会被系统拦下：

1. 双击打开应用，看到提示后点「完成」。
2. 打开「系统设置 → 隐私与安全性」，在底部点「仍要打开」。

也可以在终端里去掉隔离属性（把路径换成实际的应用）：

```bash
xattr -dr com.apple.quarantine "/Applications/Oil Find.app"
```

**校验下载文件。** 每个 Release 都附有 SHA-256，可以这样核对：

```bash
shasum -a 256 ~/Downloads/Oil-Find-x86.zip
```

## 原则

- **只收开源软件**，并且许可证允许修改和再分发。详见[许可与收录规则](docs/POLICY.md)。
- **一个软件一个 fork 仓库**：源码、改动和构建脚本都公开，每个 Release 对应一个 git tag。
- **保留原作者的版权和许可证声明**，在 README 和 Release 说明中标明上游、原作者和许可证。
- **不冒充官方**：名称带「x86」，说明「非官方」，关闭指向上游的自动更新。
- **上游提出异议就下架**；上游开始官方提供 Intel 版本后，这里改为指向官方版本。

## 许可证

本仓库自身的文档和脚本使用 [MIT 许可证](LICENSE)。列表中的每个软件都遵循各自上游的许可证，以对应 x86 仓库中的 `LICENSE` 为准；本仓库的许可证不适用于这些软件。

---

## English

**Mac4x86** collects **unofficial** Intel (x86_64) builds of open-source macOS apps whose upstream only ships Apple Silicon binaries. Each app lives in its own public fork with full source, and keeps its upstream license and copyright notices. These builds are not affiliated with or endorsed by the original authors. Please report issues to the x86 repo, not upstream. Upstream authors who object can [open an issue](../../issues/new?template=takedown.yml) and the build will be removed.
