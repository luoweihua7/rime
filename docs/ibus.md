## 下载安装输入法

应该适配于 Debian 和 Ubuntu

### 通过命令行安装

可能需要root权限，若安装失败请自行添加 `sudo` 使用特权模式

```shell
apt install ibus-rime -y
```

## 配置输入法

**先切换到需要使用输入法的用户**（一般都**不是** root 用户）

```shell
su <username>
```

下载输入法配置和设置

白霜拼音

```shell
# 输入法配置
mv ~/.config/ibus/rime ~/.config/ibus/rime-bak
git clone https://github.com/gaboolic/rime-frost --single-branch --depth=1 ~/.config/ibus/rime
curl -L https://raw.githubusercontent.com/luoweihua7/rime/main/ibus/default.custom.yaml -o ~/.config/ibus/rime/default.custom.yaml
curl -L https://raw.githubusercontent.com/luoweihua7/rime/main/ibus/ibus_rime.custom.yaml -o ~/.config/ibus/rime/ibus_rime.custom.yaml
```

雾凇拼音

```shell
# 输入法配置
mv ~/.config/ibus/rime ~/.config/ibus/rime-bak
git clone https://github.com/iDvel/rime-ice --single-branch --depth=1 ~/.config/ibus/rime
curl -L https://raw.githubusercontent.com/luoweihua7/rime/main/ibus/default.custom.yaml -o ~/.config/ibus/rime/default.custom.yaml
curl -L https://raw.githubusercontent.com/luoweihua7/rime/main/ibus/ibus_rime.custom.yaml -o ~/.config/ibus/rime/ibus_rime.custom.yaml
```

## 重新部署

点击任务栏的输入法，选择 **部署** 或者 **Deploy**

## 配置同步

修改文件 **installation.yaml**，将其中的 **sync_dir** 修改为配置同步到的目录（如iCloud目录或者Dropbox的某个目录）

点击 Rime 输入法，选择 “同步用户数据”，重新部署后生成的输入法配置文件将会同步到配置的目录中，由同步功能（如iCloud或Dropbox）进行配置备份同步
