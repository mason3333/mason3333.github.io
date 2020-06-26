# 起步

## 安装配置环境

+ 下载安装 nodeJs
+ 下载链接: <https://nodejs.org/en/>
+ 安装：   
    + 傻瓜式一键安装      
    + 安装过后再次安装会升级
+ 确定NodeJs是否安装成功  
    + 查看nodeJs的版本号：  `node --version `  
    + 或者 `node -v`
+ 安装cnpm淘宝镜像加快速度：
    
        npm install -g cnpm registry=http://registry.npm.taobao.org
+ 确定是否cnpm下载成功
    
        npm -v
+ 下载hexo框架
    
        cnpm install -g hexo-cli
+ 确定是否下载成功
    
        hexo -v

+ **补充**：一切配置都要在`root`下进行操作

## 创建一个blog文件目录

+ 默认操作都在blog目录下进行
+ 初始化hexo:
    
        hexo init

## 启动博客

+ terminal下输入：
    
        hexo s
+ 启动网页: &ensp;<http://localhost:4000>

## 书写博客

+ **默认语法为**:  `markdown`
    + 请参考：<http://baidu.com>

#### terminal下书写的方法：
+ 新建一个blog:
    
        hexo n "name"
+ 切换到blog文件目录下： 
    
        vim name.md

#### vscode下的书写方法：

##### 安装markdown插件

+ 安装 (可同步实现书写效果！！！)
```    
    MarkDown Preview Enhanced
```  
``` 
    md-filter
```
##### 正式书写.md文件

+ 在 `blog\source\_posts`目录下新建 `.md`格式文件
+ 在 vscode 下打开
打开`MarkDown Preview Enhanced`进行同步书写

##### 更新 blog 相关文件
+ 在 blog 路径下进行
```
    hexo clean
```  
```
    hexo g
```
+ 重新启动
```
    hexo s
```
## 将hexo部署到github

+ 创建一个 github 账户
+ 新建一个仓库名称为你的昵称
    + 例如：`mason3333.github.io`
+ 安装git插件
    
        cnpm install --save hexo-deployer-git

#### 配置 **_config.yml** 文件

+ 在deploment下加入
    
        type: git         
        repo: http://github.com/mason3333/mason3333.  github.io.git (你的仓库地址)
        branch: master

###### 补充：+ type、repo、branch前面要空格！！！

#### 配置git的文件

+ 在 git bash 下输入
    
        git config user.name"username"

        git config user.email "email"

+ 最后在终端下输入
    
        hexo d

### 登录你的个人博客

+ 仓库地址的后缀名：
    https://mason3333.github.io/



### 博客换肤

+ 通过 github 下找到相关项目地址
    + 例如：<https://github.com/litten/hexo-theme-yilia>
+ 在blog目录下输入：
    
        git clone https://github.com/litten/hexo-theme-yilia themes/yilia(自定义主题名)
+ 在 **_config.yml**目录下修改`themes`为你下载的主题名字

##### 更新 blog 相关文件

+ 在 blog 路径下进行
    
        hexo clean
        hexo g
        hexo d (推到远端github)

