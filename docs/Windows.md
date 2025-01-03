## 下载安装输入法

### 手动下载安装

下载并安装 [Rime](https://rime.im/download/) 输入法

### 通过命令行安装

```powershell
winget install weasel
```

## 配置输入法

以下配置使用其一即可

### 使用 PowerShell

> 测试 **PowerShell 7.4.5** 通过，更早版本若不可用，可尝试使用 CMD 命令行的脚本

> Windows 下输入法的配置文件目录一般为 `$env:APPDATA\Rime` （若为命令行CMD下时，目录为：`%APPDATA%\Rime`）

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

### 使用 CMD

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

## 重新部署

右击任务栏中的小狼毫输入法图表，点击 **重新部署** 一次即可

## 配置同步

修改文件 **installation.yaml**，将其中的 **sync_dir** 修改为配置同步到的目录（如iCloud目录或者Dropbox的某个目录）

点击 Rime 输入法，选择 “同步用户数据”，重新部署后生成的输入法配置文件将会同步到配置的目录中，由同步功能（如iCloud或Dropbox）进行配置备份同步
