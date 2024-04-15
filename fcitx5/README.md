# fcitx5 输入法配置

目录说明

> `~/.local/share/fcitx5` 目录用于保存输入法的全局配置
>
> `~/.config/fcitx5` 用于保存用户配置，用户配置选项会覆盖全局配置选项

## 皮肤

皮肤目录放在 themes 文件夹下，将文件夹中的目录，放到 `~/.local/share/fcitx5/themes` 目录下即可

## 配置

配置 `conf/classicui.conf` 文件替换掉 `~/.config/fcitx5/conf/classicui.conf` 文件

```shell
mkdir -p ~/.config/fcitx5/conf
curl -L https://raw.githubusercontent.com/luoweihua7/rime/main/fcitx5/conf/classicui.conf -o ~/.config/fcitx5/conf/classicui.conf
curl -L https://raw.githubusercontent.com/luoweihua7/rime/main/fcitx5/conf/rime.conf -o ~/.config/fcitx5/conf/rime.conf
```