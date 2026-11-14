# 个人主页 · Personal Site

一个纯静态、无需后端的个人主页，带可视化编辑器。内容全部保存在 `index.html` 内嵌的 JSON 数据块中，改完 push 即可更新。

## ✨ 功能

- 单页个人主页：个人介绍 / 技能 / 项目作品 / 联系方式，响应式布局
- `admin.html` 可视化编辑器：左侧编辑、右侧实时预览，无需懂代码
- 内容一键导出为新的 `index.html`，替换仓库文件即可上线
- 支持 GitHub Pages 免费托管

## 🚀 快速开始

### 1. 本地使用

直接双击打开 `index.html` 查看主页；
双击打开 `admin.html` 进入编辑器（无需启动服务器）。

### 2. 编辑内容

1. 打开 `admin.html`
2. 左侧修改「基本信息 / 技能 / 项目 / 联系方式」，右侧实时预览
3. 点击右上角 **「⬇ 导出 index.html」**，下载新的 `index.html`
4. 用下载的文件**替换本仓库的 `index.html`**
5. 提交并推送：

```bash
git add index.html
git commit -m "update site content"
git push
```

> 💡 编辑进度会自动保存在浏览器 localStorage 中，刷新不丢失。
> 也可以用「复制 JSON / 导入 JSON」在不同设备间迁移内容。

### 3. 发布到 GitHub Pages

1. 在 GitHub 新建仓库（如 `my-site`），推送本项目：

```bash
git remote add origin https://github.com/<你的用户名>/<仓库名>.git
git branch -M main
git push -u origin main
```

2. 打开仓库 **Settings → Pages**：
   - Source 选择 `Deploy from a branch`
   - Branch 选择 `main` / `(root)`
   - 保存
3. 一分钟后访问 `https://<你的用户名>.github.io/<仓库名>/`

> 想要 `https://<用户名>.github.io/` 根域名？把仓库名命名为 `<用户名>.github.io` 即可。

### 4. 自定义域名（可选）

在仓库根目录添加 `CNAME` 文件，内容为你的域名，并在 DNS 添加 CNAME 记录指向 `<用户名>.github.io`。

## 📁 文件说明

| 文件 | 说明 |
| --- | --- |
| `index.html` | 主页（部署上线的就是它，内容在内嵌 JSON 中） |
| `admin.html` | 可视化编辑器（本地使用即可，也可部署） |

## 🔧 进阶：绑定头像图片

编辑器「基本信息 → 头像图片地址」填入图片链接，或把图片放进仓库后填 `avatar.jpg` 这样的相对路径。
