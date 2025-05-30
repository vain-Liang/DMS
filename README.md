# 用法

## 环境安装
需要安装 **IDEA** 、 **Git** 、 **Java** 、 **Tomcat** 以及 **MySQL** 环境。
1. 使用 [**IntelliJ IDEA**](https://www.jetbrains.com/idea/download/)![](https://camo.githubusercontent.com/5b6ba2a51ac1abd8d47caa3acd8c3049558c480ed87a61619330861d0cb1ef78/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f496e74656c6c694a253230494445412d3030303030302e7376673f7374796c653d666f722d7468652d6261646765266c6f676f3d696e74656c6c696a69646561266c6f676f436f6c6f723d666666666666)  
2. 在系统上安装[**Git**](https://git-scm.com/downloads/)![](https://img.shields.io/badge/GIT-E44C30?style=for-the-badge&logo=git&logoColor=white)

> [!CAUTION]
> `JDK` 版本必须为 **1.8**，不要使用 **21** 及以上版本的JDK！！！

## 将源代码复制到本地
项目名称为 **DMS** （`Digital Management System`）。<br/>

<a name="No-3"></a>
3. 在你方便找到的任意位置创建名为 `DMS` 的 **空文件夹**
4. 在 `IDEA` 启动页面选择 [`第3步`](#No-3) 创建的 `DMS` 空文件目录
5. 选择 `clone` （`克隆`）`remote repository`（`远程仓库`），`URL`为 `https://gitea.immortalx.site:46578/No.20/FormalRepo.git`
6. 输入你的这个`gitea`平台的 **用户名**和**密码**

> [!IMPORTANT]
> - `IDEA` 的版本最好新一些， 不要低于**2022**
> - `Git` 的安装跟随官方指导，下载对应操作系统的版本。据我所知， `MacOS` 系统上应该自带有Git
> - `Java` 、 `Tomcat` 和 `MySQL` 的安装不再赘述，应该之前已经安装过，如果没有请自己搜索教程安装

> [!CAUTION]
> 创建 `DMS` 空文件夹这一步很重要，在克隆源代码之前，DMS目录下不应该再存在其他目录


## 编译
7. 代码克隆成功后，会自动进入你熟悉的 IDEA 项目界面，右下角会有弹窗提示，**注意同意**或点击**是**
8. 等待一段时间，IDEA会使用自带的 `Maven` 下载 `pom.xml` 中的项目依赖，如果太慢，请根据[阿里云镜像教程](https://blog.csdn.net/yufeiluo/article/details/129358411)配置镜像，提高下载速度

> [!NOTE]
> 我的在 Maven 下载依赖这一步进行了大概**29分钟**，注意分配时间

9. 在代码目录 `src\main\resources` 中的 **config.properties** 文件中更改连接数据库的用户名和密码
10. 执行代码目录 `src\main\resources` 中的  **db.sql** 和 **sys_user.sql** 创建数据表


## 部署到 `Tomcat`
11. 在 IDEA 中添加 `Tomcat Server Local` 运行配置，并在 `部署`(`Deployment`) 中选择 `DMS: war exploded`工件 **（这一步和Java Web运行配置是一样的）**
12. 启动 Tomcat 服务器 并查看是否部署成功，如果部署失败请检查运行配置，部署成功后如果无法登录请启动`MySQL`数据库


