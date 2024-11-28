# Rime 输入法配置

使用配置使用「[白霜拼音](https://github.com/gaboolic/rime-frost)」或「[雾凇拼音](https://github.com/iDvel/rime-ice)」为基础

添加了一些个性化的配置

- 9个候选词
- 2款皮肤
- 横向候选词

## 使用

### 下载并安装 Rime

#### 手动下载安装

下载并安装 [Rime](https://rime.im/download/) 输入法

#### 通过命令行安装

##### macOS

```shell
brew install --cask squirrel
```

##### Windows

```powershell
winget install weasel
```

##### Debian

应该适配于 Debian 和 Ubuntu

```shell
apt install --install-recommends fcitx5 fcitx5-chinese-addons -y
apt install fcitx5-rime -y
```

### 配置输入法

注意：下载好后，务必**重新部署**一次

#### macOS 配置

以下配置使用其一即可

##### 白霜拼音

```sh
# Backup original rime configuration
mv ~/Library/Rime ~/Library/Rime-Original

# Use rime-frost
git clone https://github.com/gaboolic/rime-frost --single-branch --depth=1 ~/Library/Rime

# Append custom configuration
curl -L https://raw.githubusercontent.com/luoweihua7/rime/main/squirrel/default.custom.yaml -o ~/Library/Rime/default.custom.yaml
curl -L https://raw.githubusercontent.com/luoweihua7/rime/main/squirrel/squirrel.custom.yaml -o ~/Library/Rime/squirrel.custom.yaml
```

##### 雾凇拼音

```sh
# Backup original rime configuration
mv ~/Library/Rime ~/Library/Rime-Original

# Use rime-ice
git clone https://github.com/iDvel/rime-ice --single-branch --depth=1 ~/Library/Rime

# Append custom configuration
curl -L https://raw.githubusercontent.com/luoweihua7/rime/main/squirrel/default.custom.yaml -o ~/Library/Rime/default.custom.yaml
curl -L https://raw.githubusercontent.com/luoweihua7/rime/main/squirrel/squirrel.custom.yaml -o ~/Library/Rime/squirrel.custom.yaml
```

下载好后，重新部署一次即可

#### Windows 配置

##### 使用 CMD

白霜拼音

```cmd
move %APPDATA%\Rime %APPDATA%\Rime-Original
git clone https://github.com/gaboolic/rime-frost --single-branch --depth=1 %APPDATA%\Rime
curl -L https://raw.githubusercontent.com/luoweihua7/rime/main/weasel/default.custom.yaml -o %APPDATA%\Rime/default.custom.yaml
curl -L https://raw.githubusercontent.com/luoweihua7/rime/main/weasel/weasel.custom.yaml -o %APPDATA%\Rime/weasel.custom.yaml
```

雾凇拼音

```cmd
move %APPDATA%\Rime %APPDATA%\Rime-Original
git clone https://github.com/iDvel/rime-ice --single-branch --depth=1 %APPDATA%\Rime
curl -L https://raw.githubusercontent.com/luoweihua7/rime/main/weasel/default.custom.yaml -o %APPDATA%\Rime/default.custom.yaml
curl -L https://raw.githubusercontent.com/luoweihua7/rime/main/weasel/weasel.custom.yaml -o %APPDATA%\Rime/weasel.custom.yaml
```

##### 使用 PowerShell

> 测试 **PowerShell 7.4.5** 通过，更早版本若不可用，可使用上面CMD的脚本

白霜拼音

```powershell
$APPDATA = $env:APPDATA
move $APPDATA\Rime $APPDATA\Rime-Original
git clone https://github.com/gaboolic/rime-frost --single-branch --depth=1 $APPDATA\Rime
curl -L https://raw.githubusercontent.com/luoweihua7/rime/main/weasel/default.custom.yaml -o $APPDATA\Rime/default.custom.yaml
curl -L https://raw.githubusercontent.com/luoweihua7/rime/main/weasel/weasel.custom.yaml -o $APPDATA\Rime/weasel.custom.yaml
```

雾凇拼音

```powershell
$APPDATA = $env:APPDATA
move $APPDATA\Rime $APPDATA\Rime-Original
git clone https://github.com/iDvel/rime-ice --single-branch --depth=1 $APPDATA\Rime
curl -L https://raw.githubusercontent.com/luoweihua7/rime/main/weasel/default.custom.yaml -o $APPDATA\Rime/default.custom.yaml
curl -L https://raw.githubusercontent.com/luoweihua7/rime/main/weasel/weasel.custom.yaml -o $APPDATA\Rime/weasel.custom.yaml
```

#### Debian 配置

**先切换到需要使用输入法的用户**（一般都不是 root 用户）

```shell
su <username>
```

下载输入法配置和设置

白霜拼音

```shell
# 输入法配置
mkdir -p ~/.local/share/fcitx5
git clone https://github.com/gaboolic/rime-frost --single-branch --depth=1 ~/.local/share/fcitx5/rime
curl -L https://raw.githubusercontent.com/luoweihua7/rime/main/fcitx5/default.custom.yaml -o ~/.local/share/fcitx5/rime/default.custom.yaml

# 输入法皮肤
git clone git@github.com:luoweihua7/rime.git -b fcitx5/themes --single-branch --depth=1 ~/.local/share/fcitx5/themes

# 输入法设置
mkdir -p ~/.config/fcitx5/conf
curl -L https://raw.githubusercontent.com/luoweihua7/rime/main/fcitx5/profile -o ~/.config/fcitx5/profile
curl -L https://raw.githubusercontent.com/luoweihua7/rime/main/fcitx5/config -o ~/.config/fcitx5/config
curl -L https://raw.githubusercontent.com/luoweihua7/rime/main/fcitx5/conf/classicui.conf -o ~/.config/fcitx5/conf/classicui.conf
curl -L https://raw.githubusercontent.com/luoweihua7/rime/main/fcitx5/conf/rime.conf -o ~/.config/fcitx5/conf/rime.conf
```

雾凇拼音

```shell
# 输入法配置
mkdir -p ~/.local/share/fcitx5
git clone https://github.com/iDvel/rime-ice --single-branch --depth=1 ~/.local/share/fcitx5/rime
curl -L https://raw.githubusercontent.com/luoweihua7/rime/main/fcitx5/default.custom.yaml -o ~/.local/share/fcitx5/rime/default.custom.yaml

# 输入法皮肤
git clone git@github.com:luoweihua7/rime.git -b fcitx5/themes --single-branch --depth=1 ~/.local/share/fcitx5/themes

# 输入法设置
mkdir -p ~/.config/fcitx5/conf
curl -L https://raw.githubusercontent.com/luoweihua7/rime/main/fcitx5/profile -o ~/.config/fcitx5/profile
curl -L https://raw.githubusercontent.com/luoweihua7/rime/main/fcitx5/config -o ~/.config/fcitx5/config
curl -L https://raw.githubusercontent.com/luoweihua7/rime/main/fcitx5/conf/classicui.conf -o ~/.config/fcitx5/conf/classicui.conf
curl -L https://raw.githubusercontent.com/luoweihua7/rime/main/fcitx5/conf/rime.conf -o ~/.config/fcitx5/conf/rime.conf
```

重新配置并重启输入法服务

```shell
rime_deployer --build ~/.local/share/fcitx5/rime
fcitx5 -r -d
```

## 个性化配置

下载仓库

```shell
git clone --recurse-submodules git@github.com:luoweihua7/rime.git
```

拉取线上新代码

```shell
git pull --recurse-submodules
```

## 说明

1. 备份 Rime 的输入法配置

    点击 Rime 托盘图标，选择 **程序文件夹**（Windows）或者 **用户设定**（macOS）打开配置目录。

    > Windows 目录一般为：`%APPDATA%\Rime` （若使用PowerShell时，目录为 `$env:APPDATA\Rime`） <br>
    > macOS 目录一般为：`~/Library/Rime`

    将配置文件夹备份一份即可，用于后续恢复。

2. 删除输入法配置

    将 Rime 输入法配置目录下的文件全部删除

3. 替换配置

    将下载的雾凇拼音下的所有文件（包括文件夹）全部复制到 Rime 输入法配置目录

4. 使用自定义配置

    将自定义配置（本仓库中的诸如 **default.custom.yaml** 等文件复制到 Rime 输入法配置目录

5. 重新部署

    切换到 Rime 输入法，然后点击输入法，选择 “重新部署”，等待重新部署完成即可使用

6. 输入法同步

    修改文件 **installation.yaml**，将其中的 **sync_dir** 修改为配置同步到的目录（如iCloud目录或者Dropbox的某个目录）<br>
    点击 Rime 输入法，选择 “同步用户数据”，重新部署后生成的输入法配置文件将会同步到配置的目录中，由同步功能（如iCloud或Dropbox）进行配置备份同步
