# Rime 输入法配置

使用配置为 「[雾凇拼音](https://github.com/iDvel/rime-ice)」，在基础上添加了一些个性化的配置（如9个候选词）。使用了 [ssnhd](https://github.com/ssnhd/rime) 的皮肤配置进行修改

## 使用

### 下载并安装Rime

下载并安装 [Rime](https://rime.im/download/) 输入法

### 下载雾凇拼音

下载 「[雾凇拼音](https://github.com/iDvel/rime-ice)」到本地

```sh
git clone https://github.com/iDvel/rime-ice
```

### 使用配置

1. 备份 Rime 的输入法配置

    点击 Rime 托盘图标，选择 **程序文件夹**（Windows）或者 **用户设定**（macOS）打开配置目录。

    > Windows 目录一般为：`%APPDATA%\Rime` <br>
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
