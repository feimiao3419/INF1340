# 指南：把 Colab 里改好的 notebook 保存回 GitHub 仓库

*Guide: how to save a notebook you edited in Colab back to this GitHub repo.*

---

## 前提 Prerequisites

1. **有仓库的写权限**：仓库主人在 Settings → Collaborators 里加了你；没有的话走 [方法三：fork + Pull Request](#方法三没有写权限时fork--pull-request)
2. **Colab 已关联 GitHub 账号**：Colab 菜单 工具 → 设置 → GitHub；第一次保存时也会自动弹出授权窗口，登录即可

---

## 方法一：Colab 直接保存（推荐）

*Save directly from Colab — the easiest way.*

1. 在 Colab 里打开并修改 notebook
2. 菜单：**文件 → 在 GitHub 中保存副本**（File → Save a copy in GitHub）
3. 弹出的窗口里确认：
   - **仓库**：`feimiao3419/INF1340`
   - **分支**：`main`
   - **文件路径**：例如 `notebooks/github_data_demo.ipynb`
     （如果你就是从 GitHub 打开的这个 notebook，路径会自动填好原位置，保存 = 更新原文件）
   - **提交信息**：写一句你改了什么，比如 `update data demo`
4. 可选：勾选「包含 Colab 链接」，会在 notebook 顶部加一个 “Open in Colab” 徽章，方便别人一键打开
5. 点确定 → Colab 会直接 commit 到仓库，刷新 GitHub 页面就能看到

> ⚠️ 这一步不需要挂载 Google Drive，和 Drive 完全无关。

---

## 方法二：下载 .ipynb 再到 GitHub 网页上传

*Download the .ipynb and upload it on github.com — good if you don't want to authorize Colab on GitHub.*

1. Colab 菜单：**文件 → 下载 → 下载 .ipynb**
2. 打开 GitHub 仓库网页，进入 `notebooks/` 文件夹
3. **Add file → Upload files**，把下载的 `.ipynb` 拖进去
4. 写提交信息 → **Commit changes**

适合：不想给 Colab 授权 GitHub 账号，或者只是偶尔提交一次。

---

## 方法三：没有写权限时：fork + Pull Request

*No write access? Fork and open a pull request.*

1. 打开仓库页面，点右上角 **Fork**，复制一份到你自己的账号
2. 在 Colab 里用方法一保存时，仓库选**你自己的 fork**
3. 到你的 fork 页面，点 **Contribute → Open pull request**
4. 仓库主人合并后，你的修改就进主仓库了

---

## 多人协作注意事项 Working with classmates

- **同时改同一个 notebook 会互相覆盖**：GitHub 不会合并两个人的改动，后保存的覆盖先保存的
- 建议做法：
  - 每人保存时用自己的文件名，如 `notebooks/demo_alice.ipynb`
  - 或者各自在自己的分支上改（保存窗口里分支名填自己的，如 `alice-dev`）
- 保存前，最好先在 GitHub 网页上看一眼这个文件最近有没有被别人更新过

## 改错了怎么办 Undoing a mistake

GitHub 会保留每一次提交的历史：

1. 打开文件页面 → 点 **History**
2. 找到改错之前的那个版本，点进去可以查看
3. 需要恢复的话，把旧版本内容复制回来重新提交即可

---

## 常见问题 FAQ

**Q：保存时找不到 INF1340 仓库？**
A：确认你是 collaborator，并且在 Colab 的 工具 → 设置 → GitHub 里关联了正确的 GitHub 账号。

**Q：私有仓库保存不了？**
A：本仓库是 public，不受影响。如果以后转私有，需要在 Colab 的 GitHub 设置里勾选「访问私有代码库和组织代码库」。

**Q：保存后 GitHub 上看不到更新？**
A：确认保存窗口里的分支是 `main`，路径没写错；然后刷新页面。
