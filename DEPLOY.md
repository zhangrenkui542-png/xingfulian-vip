# 幸赋链官网部署指南

## 免费部署方案（无需服务器）

### 方案一：Vercel（推荐，最简单）

1. **准备 GitHub 仓库**
   - 登录 GitHub，创建新仓库 `xingfulian-vip`
   - 上传所有 HTML 文件

2. **一键部署**
   - 登录 [vercel.com](https://vercel.com)
   - 点击 "Add New..." → "Project"
   - 选择刚才创建的仓库
   - 点击 "Deploy"

3. **绑定域名**
   - 进入 Settings → Domains
   - 添加 `xingfulian.vip`
   - 按照提示配置 DNS 记录

---

### 方案二：Netlify

1. **准备 GitHub 仓库**（同方案一）

2. **一键部署**
   - 登录 [netlify.com](https://netlify.com)
   - Drag & drop 上传 `xingfulian-vip` 文件夹
   - 等待部署完成

3. **绑定域名**
   - Domain Management → Add custom domain

---

### 方案三：Cloudflare Pages（国内访问快）

1. **准备 GitHub 仓库**（同方案一）

2. **一键部署**
   - 登录 [cloudflare.com](https://cloudflare.com)
   - Workers 和 Pages → Create application → Pages
   - Connect to Git → 选择仓库
   - 构建命令留空，直接部署

3. **绑定域名**
   - Custom domains → Add domain

---

## 文件结构

```
xingfulian-vip/
├── index.html       # 首页（已添加测评入口）
├── about.html       # 关于我们
├── products.html    # 产品矩阵
├── allies.html      # 盟友权益
├── office.html      # 天枢办公室
└── assessment.html  # 创业测评系统
```

---

## 部署后检查清单

- [ ] 首页可以访问
- [ ] 导航链接全部正常
- [ ] 测评页面可以答题
- [ ] 域名解析生效
- [ ] HTTPS 证书自动生成

---

## 天枢状态同步

龙虾办公室运行在本地，需要公网暴露才能在官网展示：
- 方案：使用 Cloudflare Tunnel（需要一台始终开机的电脑运行 agent）
- 或者：仅展示静态图片/链接

---

有问题随时联系天枢。
