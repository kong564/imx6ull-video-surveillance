# imx6ull-video-surveillance

基于IMX6ULL的嵌入式网络视频监控系统
项目简介
基于NXP i.MX6ULL平台开发的嵌入式视频监控系统，实现本地采集显示与远程监控功能。下位机完成V4L2摄像头采集、JPEG压缩及Qt界面显示；上位机通过TCP接收JPEG流，实现实时预览、MP4录制及播放器功能。

技术栈
C++ / Qt / V4L2 / TCP Socket / FFmpeg / IMX6ULL

核心工作
采集与显示：基于V4L2实现USB摄像头采集，通过V4L2→JPEG→QImage链路在IMX6ULL触摸屏实时显示

远程传输：TCP+JPEG方案替代UDP避免IP分片丢包，同网段延迟＜100ms

录制与播放：基于FFmpeg实现MP4录制，开发播放器支持seek拖拽、暂停/继续

关键问题解决：定位并修复FFmpeg录制颜色发灰问题（Full Range vs Limited Range）

项目成果
实现嵌入式本地采集显示 + 远程监控双端系统，支持实时预览、拍照、相册同步、视频录制与回放全功能。
