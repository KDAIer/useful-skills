# github 常用UI和emoji

## 📦 GitHub常用操作图标（UI）

| 图标              | 含义                      |
| :---------------- | :------------------------ |
| 📦 箱子/包裹      | 表示 release 或者 package |
| 📝 铅笔           | 编辑                      |
| ➕ 加号           | 新增                      |
| ❌ 叉号           | 删除、关闭                |
| 🔍 放大镜         | 搜索                      |
| 🔀 分支箭头       | Merge、Pull Request       |
| ⬆️⬇️ 上下箭头 | 上下切换、排序            |
| ⏰ 时钟           | 最近活动、历史            |
| ⭐️ 星星         | 收藏 Star                 |
| 👁️ 眼睛         | Watch 仓库                |

## 📝 开发者常用 emoji 表情标记（Git 提交/PR 标题）

| Emoji                            | 用途                    |
| :------------------------------- | :---------------------- |
| 🎉`:tada:`                     | 初次提交 / 项目初始化   |
| ✨`:sparkles:`                 | 新功能                  |
| 🐛`:bug:`                      | 修复 bug                |
| ♻️`:recycle:`                | 重构代码                |
| 🔥`:fire:`                     | 删除代码或文件          |
| 🚑️`:ambulance:`              | 热修复                  |
| 📝`:memo:`                     | 更新文档                |
| ✅`:white_check_mark:`         | 添加测试                |
| 🔒`:lock:`                     | 修复安全问题            |
| ⬆️`:arrow_up:`               | 升级依赖                |
| ⬇️`:arrow_down:`             | 降级依赖                |
| 📦`:package:`                  | 打包发布                |
| 👷`:construction_worker:`      | CI/CD 配置              |
| 🔧`:wrench:`                   | 配置相关变更            |
| 🚀`:rocket:`                   | 部署功能                |
| 💄`:lipstick:`                 | UI 样式调整             |
| 📈`:chart_with_upwards_trend:` | 性能优化                |
| 🎨`:art:`                      | 改进代码结构 / 格式美化 |

---

# github 回退commits技巧

## 📌 情况 1：**回退到这个 commit，并保留后续改动在工作区**

```bash
git reset --mixed ...
```

👉 回到那个 commit，**后面的改动会放到工作区，未 add 状态**

## 📌 情况 2：**回退到这个 commit，保留后续改动在暂存区**

```bash
git reset --soft ...
```

👉 回到那个 commit，**后面的改动仍然保留在暂存区**

## 📌 情况 3：**回退到这个 commit，删除之后所有改动（危险⚠️）**

```bash
git reset --hard ...
```

👉 回到那个 commit，**之后的改动和 commit 都消失了**

## 📌 如果回退完，还要推送到远程仓库（如果已经 push 过）

```bash
git push -f
```

⚠️ **强推**会覆盖远程仓库的历史，协作项目一定要确认好！

## 📌 查看确认一下

如果你想确认一下历史提交：

```bash
git log --oneline
```

就能看到 ... 这条在哪。
