## 下载安装输入法

应该适配于 Debian 和 Ubuntu

### 通过命令行安装

可能需要root权限，若安装失败请自行添加 `sudo` 使用特权模式

```shell
apt install --install-recommends fcitx5 fcitx5-chinese-addons -y
apt install fcitx5-rime -y
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

## 重新部署

```shell
rime_deployer --build ~/.local/share/fcitx5/rime
fcitx5 -r -d
```

## 配置同步

修改文件 **installation.yaml**，将其中的 **sync_dir** 修改为配置同步到的目录（如iCloud目录或者Dropbox的某个目录）

点击 Rime 输入法，选择 “同步用户数据”，重新部署后生成的输入法配置文件将会同步到配置的目录中，由同步功能（如iCloud或Dropbox）进行配置备份同步
