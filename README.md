# Home KTV - LazyCat App

一个局域网的私人 KTV 系统。支持 Intel 核显 VAAPI 硬件加速。

## 功能特点

- 🎤 局域网私人 KTV 系统
- 📺 电视端自动发现（UDP 18888）
- 🎵 支持自定义音乐库
- 🖥️ Intel 核显 VAAPI 硬件转码加速
- 🤖 可选 AI 辅助功能（基于 DeepSeek）

## 使用说明

1. 部署后打开应用网页端（8080 端口）
2. 电视端会自动扫描发现本服务（UDP 18888）
3. 将音乐文件放入 `/source-music` 目录
4. 应用会自动处理并生成 KTV 曲库

## 硬件加速

本应用通过 `/dev/dri` 设备直通支持 Intel 核显 VAAPI 硬件加速。
如果您的设备没有 Intel 核显，应用仍可正常运行（软件转码）。

## 开发

```bash
# 构建 LPK 包
lzc-cli project release -o home-ktv.lpk

# 查看包信息
lzc-cli lpk info home-ktv.lpk
```

## 发布

双商店发布：官方商店 + 喵喵商店（私有商店）。

## 上游

- 原项目: https://github.com/zhayinggang/ktv-home
- 镜像: ghcr.io/zhayinggang/ktv-home (GitHub Container Registry)