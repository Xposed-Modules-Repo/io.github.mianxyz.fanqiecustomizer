# 更新日志

## 6.1 · versionCode 107

- 开屏去广告保留真实归因状态，在外层 SplashHelper.a(Boolean) 返回 Single.error，复用宿主 NO_AD 通道；前轮实机开屏停留约 0.25–0.36 秒。
- 底栏触摸 Hook 前移至初始化，去除重复绘制准备，margin 仅差量更新；资源 ID/名称按 Resources 缓存，并限制负缓存大小。
- 书卡封面一次 getPixels 批量读取；按 Bitmap 实例与 generationId 记忆占位拒绝，可变 Drawable 使用 180ms 冷却；前轮三次采样为 25/24/24 次。
- 日志使用容量 256 的单 daemon 线程异步派发，非 debug 模式静默逐卡诊断；移除临时 StartupPerf 及纯计时包装。
- 保持 90 键契约、6.0 视觉实现与六 APK 兼容登记；历史测量只说明对应热点改善，整体启动与长帧结果沿用前轮记录。最终封板未重测去广告秒进及全部主题／交互组合。

## 历史记录

适配番茄免费小说 7.3.9.32 (73932)，需要支持 libxposed API 102 的框架。
