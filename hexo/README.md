## hexo镜像使用指导

如需使用容器部署代码（hexp deploy），还需要 **配置git** 以及 **安装hexo-deployer-git插件**

#### 配置git

```bash
git config --global user.email "you@example.com"
git config --global user.name "your name"
```

当然也可以根据需要配置ssh-key，这样不用每次提交都输入用户名密码

#### 安装hexo-deployer-git插件

为解决执行"hexo deploy" "ERROR Deployer not found: git" 问题，在站点目录中执行以下命令

```bash
cd ${your_hexo_project_dir}
npm install hexo-deployer-git --save
```

参考：[hexo d命令报错 ERROR Deployer not found: git](https://blog.csdn.net/qq_21808961/article/details/84476504)

#### 其它

hexo每次只会将 *${your_hexo_project_dir}/public* 目录下的内容提交到 *yourname.github.io*，建议在github上专门准备一个repository，用来管理hexo工程。

参考：[Git命令手动备份Hexo博客源文件](https://blog.enjoytoshare.club/article/manual_backup_blog_source_files.html)

​           [自动备份Hexo博客源文件](https://blog.enjoytoshare.club/article/auto_backup_blog_source_files.html) 


