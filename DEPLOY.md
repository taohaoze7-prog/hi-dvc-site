# 🚀 H&I Lab Website · Deploy Checklist

> 目标 URL: **https://hi-dvc.github.io/**
> 方案: 建 GitHub Organization → 建 repo → push → Pages 自动上线

---

## ✅ 前置检查

- [x] 网站源码已完成 (`index.html`)
- [x] Favicon 已生成 (`favicon.svg`)
- [x] OG 分享图已生成 (`og-image.svg`)
- [x] 所有链接已填充 (Instagram / Discord / Email)
- [x] 8 位 Officers 人物卡完整
- [ ] **← 你的任务从这里开始**

---

## 📋 部署步骤 (约 8 分钟)

### Step 1 · 创建 GitHub Organization (2 分钟)

1. 用你自己的 GitHub 账号登录
2. 打开 → https://github.com/organizations/plan
3. 选 **Free** 方案
4. **Organization account name** 填: `hi-dvc`
5. **Contact email** 填: `hilabdvc@gmail.com`
6. 归属选 **My personal account**
7. 下一步 → 跳过邀请成员 → Create organization

> ⚠️ 如果 `hi-dvc` 被占了,备选: `hi-dvc-lab` / `hidvc` / `handi-dvc`
> 告诉我用了哪个,我改最终链接。

---

### Step 2 · 创建仓库 (1 分钟)

1. 进入新建的组织: https://github.com/hi-dvc
2. 点 **Create a new repository**
3. **Repository name** 必须填: `hi-dvc.github.io`
   > 这个名字让 GitHub Pages 自动部署到根路径
4. Description: `Heritage & Intelligence Laboratory · Diablo Valley College`
5. 选 **Public**
6. **不要**勾选 Add README / .gitignore / license (我们已经准备好所有文件)
7. 点 **Create repository**

---

### Step 3 · 推代码 (2 分钟)

在终端复制粘贴执行:

```bash
cd /Users/henryt/MyAI_Secretary/projects/hi-dvc-site

# 初始化 git
git init
git add .
git commit -m "Initial launch · H&I Lab founding site"

# 添加远程仓库
git branch -M main
git remote add origin https://github.com/hi-dvc/hi-dvc.github.io.git

# 推送
git push -u origin main
```

> 首次 push 会让你登录 GitHub (浏览器授权或 Personal Access Token)。
> 如果卡在这一步,告诉我看到了什么报错。

---

### Step 4 · 开启 GitHub Pages (30 秒)

1. 进入 https://github.com/hi-dvc/hi-dvc.github.io/settings/pages
2. **Source**: 选 `Deploy from a branch`
3. **Branch**: 选 `main` · 文件夹选 `/ (root)`
4. 点 **Save**

---

### Step 5 · 等待上线 (1-3 分钟)

1. 回到仓库首页
2. 点右侧 **Actions** 标签,看到绿色 ✓ 表示部署成功
3. 访问 → **https://hi-dvc.github.io/**

🎉 上线完成!

---

## 🔄 以后更新内容

以后修改网站内容,只需:

```bash
cd /Users/henryt/MyAI_Secretary/projects/hi-dvc-site
# 改文件...
git add .
git commit -m "描述这次改动"
git push
```

GitHub 会自动重新部署,约 1 分钟后生效。

---

## 📂 文件清单

```
hi-dvc-site/
├── index.html          # 网站主文件
├── favicon.svg         # 标签页图标 (朱砂印章 文韻智行)
├── og-image.svg        # 社交分享预览图 (1200×630)
├── DEPLOY.md           # 本文件
└── previews/
    ├── style-A-obsidian-gold.html
    ├── style-B-cyber-inkwash.html
    └── style-C-scholar-paper.html
```

---

## ⚠️ 常见问题

### `git push` 要密码?
GitHub 2021 起不再支持密码 push,需要用 **Personal Access Token** 或 **SSH key**:
- 创建 PAT: https://github.com/settings/tokens/new (勾选 `repo` 权限)
- 或者安装 GitHub CLI: `brew install gh && gh auth login`

### 上线后 404?
- 检查 Pages 是否 Enable (Settings → Pages)
- 仓库名必须是 `hi-dvc.github.io` 才能走根路径
- 等 3-5 分钟让 DNS 生效

### 想用自定义域名?
以后想买 `hi-dvc.org` 等真实域名,在 Pages 设置里填 Custom domain,再加一条 CNAME 记录即可。

---

## 🎨 上线后建议的下一步

1. **微调 Officers bios** — 现在的 bio 是我猜的,你在 `index.html` 里搜 `founder-bio` 批量改
2. **加 Google Analytics** — 想追踪访问量的话告诉我,2 分钟加
3. **买 `hi-dvc.org` 域名** — 长期品牌建议
4. **加 RSVP 表单** — Google Form 嵌入或跳转
5. **加图片画廊** — 第一次 meeting 拍的照片
