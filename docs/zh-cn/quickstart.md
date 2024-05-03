# 快速开始

## 安装
### MacOS或Linux下的安装

复制以下命令，并在终端中执行。

```bash
curl --proto '=https' --tlsv1.2 -sSf https://gvc.1710717.xyz/proxy/https://raw.githubusercontent.com/gvcgo/version-manager/main/scripts/install.sh | sh
```

### Windows下的安装

复制以下命令，并在Powershell中执行。
```bash
powershell -nop -c "iex(New-Object Net.WebClient).DownloadString('https://gvc.1710717.xyz/proxy/https://raw.githubusercontent.com/gvcgo/version-manager/main/scripts/install.ps1')"
```

!> 如果你的系统是Win11，你需要打开**开发者模式**，因为vmr需要创建符号链接。如果你的系统是Win10，并且遇到创建符号链接失败的情况，你可以尝试在管理员权限下完成操作(**一般情况下无需管理员权限**)。

!> 使用go源码编译得到的Windows可执行文件，经常被检测为病毒，这是**误报**，目前没有较好的办法。关于解释，详见[这里](https://juejin.cn/post/7027066330331217957)。 这种情况下，你需要手动将一些目录添加到信任列表中。需要添加到信任的目录有 **$HOME**, **$HOME/.vm**, 以及你指定的**SDK安装目录**。

!> **VMR**定制了**source**命令，可以用于在当前Powershell中刷新Path环境变量。

### VMR安装在哪里？

```bash
$HOME/.vm
```

### 可以指定SDK的安装目录吗？

可以。在首次安装的时候，会提示你**Enter the SDK installation directory for vmr**，这时候在输入框中输入你想要定制的SDK安装路径即可。
如果你不小心输入错误了，你也可以在$HOME/.vm/config.json配置文件中手动修改。

![installation](https://cdn.jsdelivr.net/gh/moqsien/img_repo@main/vmr_install.png)

## 更新
### 方法一

使用VMR自带的更新脚本。
```bash
vmr-update
```

### 方法二 

复制上面的安装命令到终端中执行。

## 卸载

暂时没有提供卸载脚本，你可以手动删除以下的目录。
```bash
$HOME/.vm
SDK_Installation_Dir
```