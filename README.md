## Maven安装和配置

### 1.本地环境

1.jdk版本：jdk1.8.0_192；

2.编辑器：IntelliJ IDEA；

3.操作系统：Windows 10

### 2.安装

maven下载地址：http://mirrors.tuna.tsinghua.edu.cn/apache/maven/maven-3/3.6.1/binaries/apache-maven-3.6.1-bin.zip

新建环境变量MAVEN_HOME，赋值为解压该压缩包的地址，我的是：C:\Program Files\Apache\maven-3.6.1。

Path环境变量追加一条%MAVEN_HOME%\bin\。

然后在命令行中测试：`mvn -v`，能得到结果即可。

### 3.配置Maven本地仓库

建立目录：D:\Program Files\Apache\maven-repository。

打开C:\Program Files\Apache\maven\conf\settings.xml文件，查找下面这行代码：

`<localRepository>/path/to/local/repo</localRepository>`

修改为

`<localRepository>D:\Program Files\Apache\maven-repository</localRepository>`

在命令行中运行：

`mvn help：system`

如果配置成功，D:\Program Files\Apache\maven-repository将会出现一些新文件。

### 4.在Intellij IDEA中配置Maven

打开Setting -> Build, Execution, Deployment -> Build Tools -> Maven，

选择Maven home directory：C:/Program Files/Apache/maven-3.6.1

选择User setting file（勾选重载）：C:\Program Files\Apache\maven-3.6.1\conf\settings.xml

选择Local repository（勾选重载）：D:\Program Files\Apache\maven-repository

至此，Maven的安装和配置步骤结束。



