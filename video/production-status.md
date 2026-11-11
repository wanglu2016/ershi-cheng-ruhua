# 二十城入画：完成记录

- 完整视频：city-in-ancient-ink-1080p.mp4；89,843,137 bytes。
- 视频画面：137.375 秒，1920×1080，24fps，H.264/yuv420p；AAC 48kHz 单声道，完整封装时长137.487秒。
- 内容：20座当代城市、20幅不重复古画参考、片头片尾、逐段角标、中文配音及23条同步字幕。
- SHA-256：35d3d861bff5badeae9fe4fbddda0de154e0ff473f8cde9ae4850634cafb4560。
- 核验：整片解码及字幕时序通过；抽查20个城市段画面及角标；音量峰值约-1.4dB，无削波；未作逐段人工听审。
- 远端核验：GitHub Release已发布（draft=false），远端文件bytes及SHA-256与本地一致。浏览器下载回读未完成，没有记作通过。
- 发布范围：私有仓库。
- 文档提交：814ca8b86879b7b554ec6a9e8faeda1c1a8b0334。
- 海报及版本标签提交：3a1ac371c2126a3d4cddec6800cc1253ad8e42c5。
- 完整视频入口：https://github.com/wanglu2016/ershi-cheng-ruhua/releases/tag/v1.0.0
- 项目与说明：https://github.com/wanglu2016/ershi-cheng-ruhua

## 恢复制作

制作源包保留20幅城市画面、分段配音及字词时间戳、时间线、字幕、说明和渲染脚本。依赖为 edge-tts==7.3.1、pillow、numpy、opencv-python-headless、FFmpeg与Noto CJK字体。

恢复命令：python scripts/render_film.py --workers 2

原始配音无需重合成，镜头文件可按缓存跳过。改变画面后重渲染该镜头及相邻转场，再合并并执行技术检查。当前请求的成片与GitHub交付已完成。
