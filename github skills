# github 回退commits技巧
---

## 📌 情况 1：**回退到这个 commit，并保留后续改动在工作区**

```bash
git reset --mixed ...
```

👉 回到那个 commit，**后面的改动会放到工作区，未 add 状态**

---

## 📌 情况 2：**回退到这个 commit，保留后续改动在暂存区**

```bash
git reset --soft ...
```

👉 回到那个 commit，**后面的改动仍然保留在暂存区**

---

## 📌 情况 3：**回退到这个 commit，删除之后所有改动（危险⚠️）**

```bash
git reset --hard ...
```

👉 回到那个 commit，**之后的改动和 commit 都消失了**

---

## 📌 如果回退完，还要推送到远程仓库（如果已经 push 过）

```bash
git push -f
```

⚠️ **强推**会覆盖远程仓库的历史，协作项目一定要确认好！

---

## 📌 查看确认一下

如果你想确认一下历史提交：

```bash
git log --oneline
```

就能看到 ... 这条在哪。

