## 下载安装输入法

### 手动下载安装

下载并安装 [Rime](https://rime.im/download/) 输入法

### 通过命令行安装

```shell
brew install --cask squirrel
```

## 配置输入法

以下配置使用其一即可

> macOS 下输入法的配置文件目录一般为：`~/Library/Rime`

### 白霜拼音

```sh
# Backup original rime configuration
mv ~/Library/Rime ~/Library/Rime-Original

# Use rime-frost
git clone https://github.com/gaboolic/rime-frost --single-branch --depth=1 ~/Library/Rime

# Append custom configuration
curl -L https://raw.githubusercontent.com/luoweihua7/rime/main/squirrel/default.custom.yaml -o ~/Library/Rime/default.custom.yaml
curl -L https://raw.githubusercontent.com/luoweihua7/rime/main/squirrel/squirrel.custom.yaml -o ~/Library/Rime/squirrel.custom.yaml
```

### 雾凇拼音

```sh
# Backup original rime configuration
mv ~/Library/Rime ~/Library/Rime-Original

# Use rime-ice
git clone https://github.com/iDvel/rime-ice --single-branch --depth=1 ~/Library/Rime

# Append custom configuration
curl -L https://raw.githubusercontent.com/luoweihua7/rime/main/squirrel/default.custom.yaml -o ~/Library/Rime/default.custom.yaml
curl -L https://raw.githubusercontent.com/luoweihua7/rime/main/squirrel/squirrel.custom.yaml -o ~/Library/Rime/squirrel.custom.yaml
```

## 重新部署

切换到鼠须管输入法后，通过快捷键 `Ctrl + Option + ~` 重新部署一次即可

## 配置同步

修改文件 **installation.yaml**，将其中的 **sync_dir** 修改为配置同步到的目录（如iCloud目录或者Dropbox的某个目录）

点击 Rime 输入法，选择 “同步用户数据”，重新部署后生成的输入法配置文件将会同步到配置的目录中，由同步功能（如iCloud或Dropbox）进行配置备份同步
