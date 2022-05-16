# 很简单，在 Ubuntu 18.04 上安装 Yarn 就是通过它的存储库。 我们将能够轻松地更新应用程序以及系统的其余部分。

## 按照以下步骤在 Ubuntu 16.04/18.04 系统上安装 Yarn


### 1. 步骤1.添加GPG密钥
> curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add - 

### 2. 步骤2.添加Yarn存储库
> echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list

### 3. 步骤3.更新包列表并安装Yarn
> sudo apt update

> sudo apt install yarn

#### tip. 如果您的系统上尚未安装 Node.js，则上面的命令将安装它。 那些使用 nvm 的人可以跳过 Node.js 安装：
> sudo apt install --no-install-recommends yarn

### 4. 步骤4.检查Yarn的版本
> yarn --version


```yarn operation manual
如何在 Ubuntu 上使用 Yarn
现在您已经在Ubuntu系统上安装了Yarn，下一步是探索一些最常见的Yarn命令。

步骤1.使用以下命令创建新项目
yarn init project_name
init脚本会问你几个问题。 您可以应答或按Enter键以使用默认值。

完成后，脚本将创建一个包含您提供的信息的基本package.json文件。 您可以稍后打开并编辑此文件。

步骤2.向项目添加依赖项
如果要在项目中使用其他包，则需要将其添加到项目依赖项中。 为此，请使用yarn add命令，后跟包名称：

yarn add [package_name]
但是，也可以将包或库的特定版本定义为项目的依赖项。

yarn add [package]@[version]
第3步。升级依赖项
要升级依赖项，请使用以下方法之一：

yarn upgrade [package_name]
我们还可以指定要更新的包的版本：

yarn upgrade [package_name]@[version_or_tag]
上面的命令将根据package.json文件中指定的版本范围将项目依赖项更新为其最新版本。

步骤4.删除依赖项
使用yarn remove命令后跟包名称来删除依赖项：

yarn remove [package_name]
此命令还将更新项目的package.json和yarn.lock文件。

步骤5.安装所有已定义的依赖项
要安装所有项目依赖项，请使用以下命令：

yarn install
或

yarn
```


