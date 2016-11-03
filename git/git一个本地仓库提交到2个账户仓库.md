本地仓库config配置

----------

```c
[core]
    repositoryformatversion = 0
    filemode = false
    bare = false
    logallrefupdates = true
    symlinks = false
    ignorecase = true
    hideDotFiles = dotGitOnly
[remote "github"]
    url = https://github.com/paddingme/paddingme.github.io.git
    fetch = +refs/heads/*:refs/remotes/github/*
[branch "master"]
    remote = origin
    merge = refs/heads/master
[remote "gitcafe"]
    url = https://gitcafe.com/paddingme/paddingme.github.io.git
    fetch = +refs/heads/*:refs/remotes/gitcafe/*
[alias]
    publish=!sh -c \"git push github master && git push gitcafe master:gitcafe-pages\"
```