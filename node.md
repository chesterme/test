# 设置ssh key
GitHub上连接已有仓库时，是通过ssh的公开密钥来进行认证的。
1. 在本地上生成ssh key
```
    ssh-keygen -t rsa -C "your_email@example.com"
```
2. 在GitHub账号上添加本地生成的公钥
3. 测试连接
```
    ssh -T git@github.com
```


# clone已有仓库
```
    git clone git@github.com:usename/repositories-name.git
```

# 提交
```
    git add filename // 添加文件到版本管理系统
    git commit -m "description" // 添加描述信息
    git log // 查看日志
    git push // 将改变的内容提交到GitHub仓库中
```

# 基本操作
```
    git init // 初始化仓库
    git status // 查看仓库的状态
    git add // 向暂存区中添加文件
    git commit // 保存仓库的历史记录
    git log // 查看日志
    git diff // 查看更改前后的差别，q退出，+表示新添加的行，-表示被删除的行
```

# 分支操作
在多个并行作业时，会使用到分支。在不同分支中，可以同时进行完全不同的作业。等该分支的作业完成后再与master分支合并。
```
    git branch // 显示分支
    git checkout -b feature-name // 创建、切换分支
    git branch featrue-name // 创建分支
    git checkout feature-name // 切换分支,*表示当前分支
    git merge // 合并分支
```

## 特性分支
集中实现单一特性（主题），除此之外不进行任何作业的分支。在日常开发中，往往会创建多个特性分支，同时在此外在保留一个随时可以发布软件的稳定分支。