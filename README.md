# ZenNeko-CI

公开的构建外壳仓库：**只有一个 workflow YAML**，用来在 public 仓库的免费额度下
构建私有仓库 `wisyh/ZenNeko` 的 Android APK。

- 本仓库**不含**任何源码、密钥或构建产物。
- 源码由 workflow 在 runner 的临时工作区 checkout，用完即销毁，不会提交回本仓库。
- 产物推回**私有**仓库的 Release，本仓库**不**上传 artifact
  （public 仓库的 artifact 任何人都能下载）。
- Actions 缓存刻意排除 `caches/build-cache-1`，避免私有源码的编译产物进入可读缓存。

手动触发：**Actions → Build ZenNeko → Run workflow**。
