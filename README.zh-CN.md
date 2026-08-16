# rutabaga_gfx（Android 固定版本）

[English](README.md) | 简体中文

rutabaga_gfx 是 crosvm 与 gfxstream/virgl 等图形后端之间的 Rust 抽象层。BSCP 使用 manifest
固定版本以保持 Guest 协议、外部内存句柄和主机图形依赖一致。

修改 capability、资源导入、fence 或跨平台句柄转换时，应分别验证无头与加速路径，并保证
资源释放和错误传播不会因主机平台不同而静默降级。
