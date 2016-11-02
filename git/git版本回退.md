在命令行使用git：
在工作区目录下输入
```
git reflog
```
可以查询出每个历史版本的commit，每个commit都有对应的ID，确认好要退回的ID后输入：
```
git reset --hard 确认的ID
```
便可退回相应的历史版本