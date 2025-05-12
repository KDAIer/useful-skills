 # Windows（PowerShell / CMD） 和 Linux 下查看目录文件的对照总结：

---

## 📑 目录下文件查看命令总结

| 功能        | Windows PowerShell              | Windows CMD | Linux / macOS 终端                             |
| :-------- | :------------------------------ | :---------- | :------------------------------------------- |
| 查看当前目录内容  | `Get-ChildItem` 或 `ls`          | `dir`       | `ls`                                         |
| 查看详细信息    | `Get-ChildItem`（默认带属性）          | `dir`       | `ls -l`                                      |
| 查看包括隐藏文件  | `Get-ChildItem -Force`          | `dir /a`    | `ls -a`                                      |
| 查看文件名     | `Get-ChildItem \| Select Name`  | 无直接命令       | `ls`                                         |
| 递归查看子目录内容 | `Get-ChildItem -Recurse`        | `dir /s`    | `ls -R`                                      |
| 查看绝对路径    | `Get-ChildItem \| Resolve-Path` | 无直接命令       | `realpath filename` 或 `readlink -f filename` |

---

## 📌 小贴士：

* **PowerShell** 中 `ls` 是 `Get-ChildItem` 的别名，命令能互换。
* **Linux** 终端下 `ls` 比较灵活，可加上 `-l`、`-a`、`-R` 等参数组合使用。
* **CMD** 命令较少，常用 `dir` + 参数实现类似功能。
