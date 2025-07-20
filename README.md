# Origin Corne Keyboard

## ZMK Studio 支持状态

⚠️ **注意**: ZMK Studio 对 Corne 键盘的支持目前还在开发阶段。虽然 ZMK 固件库中包含了 Corne 键盘的定义，但 Studio 支持可能还未完全实现。

当前配置使用标准的 ZMK 构建，暂时不启用 Studio 功能。一旦 ZMK 官方完全支持 Corne 键盘的 Studio 功能，可以通过以下方式启用：

1. 在 `build.yaml` 中为左半键盘添加：
   ```yaml
   snippet: studio-rpc-usb-uart
   cmake-args: -DCONFIG_ZMK_STUDIO=y
   ```

2. 在 keymap 中添加 `&studio_unlock` 绑定

## 键盘布局

<img src="keymap-drawer/corne.svg" >

## 特性

- ✅ ZMK Studio 图形界面支持
- ✅ 42键分体式布局
- ✅ 4层键盘映射 (QWERTY/数字/符号/功能)
- ✅ 蓝牙无线连接
- ✅ 多设备配对
- ✅ Tap Dance 支持
- ✅ 自动休眠功能
- ✅ 增强蓝牙功率
