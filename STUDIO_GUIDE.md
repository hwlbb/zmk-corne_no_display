# ZMK Studio 使用指南

## 当前状态

⚠️ **重要说明**: 根据 ZMK 官方文档和构建测试，Corne 键盘的 ZMK Studio 支持目前可能还未完全实现。

虽然 ZMK 固件库中包含了 Corne 键盘的定义，但 Studio 功能需要额外的物理布局配置，这些配置可能还在开发中。

## 现状分析

1. **ZMK 内置支持**: ZMK 确实包含 `corne_left` 和 `corne_right` 的 shield 定义
2. **Studio 要求**: Studio 需要键盘定义包含物理布局（physical layout）和 `keys` 属性
3. **开发状态**: 根据 ZMK 官方博客，并非所有键盘都已更新为支持 Studio

## 如何检查 Studio 支持

你可以查看 [ZMK Studio 支持的键盘列表](https://zmk.dev/blog/2024/11/11/zmk-studio-mvp-ga) 来确认 Corne 是否已正式支持。

## 替代方案

在 Studio 支持完全实现之前，你可以：

1. **使用传统配置**: 继续编辑 `.keymap` 文件来自定义布局
2. **使用 Keymap Editor**: 使用第三方工具如 [keymap-editor.zmk.dev](https://keymap-editor.zmk.dev/)
3. **关注更新**: 持续关注 ZMK 官方更新，等待 Corne 的 Studio 支持

## 未来启用 Studio

一旦 ZMK 官方完全支持 Corne 键盘的 Studio 功能，可以通过以下步骤启用：

ZMK Studio 是一个基于 Web 的图形界面工具，允许你实时修改 ZMK 键盘的配置，无需重新编译和刷写固件。

## 如何使用

### 1. 准备工作

确保你的键盘固件已经启用 Studio 支持（本配置已启用）。

### 2. 连接键盘

- **USB 连接**: 使用 USB-C 线缆连接键盘到电脑
- **蓝牙连接**: 确保键盘已与电脑配对并连接

### 3. 打开 ZMK Studio

访问官方 Studio 网站：https://zmk.dev/studio

### 4. 连接键盘

1. 点击页面上的 "Connect" 按钮
2. 选择你的 Corne 键盘设备
3. Studio 会自动检测并加载键盘布局

### 5. 编辑布局

- **选择层**: 在界面顶部选择要编辑的层（Default、Number、Symbol、Fn）
- **修改按键**: 点击任意按键，从弹出的菜单中选择新的功能
- **实时生效**: 修改会立即生效，无需重启或刷写固件

### 6. 保存配置

1. 完成编辑后，点击 "Export" 按钮
2. 下载生成的 keymap 文件
3. 将文件内容复制到本项目的 `config/corne.keymap` 文件中
4. 提交更改到 Git 仓库

## 支持的功能

- ✅ 实时按键重映射
- ✅ 多层布局编辑
- ✅ Tap/Hold 行为配置
- ✅ 组合键设置
- ✅ 蓝牙配置
- ✅ 系统控制键

## 注意事项

1. **固件兼容性**: 确保使用最新的 ZMK 主分支固件
2. **浏览器兼容性**: 推荐使用 Chrome 或基于 Chromium 的浏览器
3. **连接稳定性**: USB 连接通常比蓝牙更稳定
4. **备份配置**: 在大幅修改前，建议备份当前的 keymap 文件

## 故障排除

### 无法连接键盘

1. 确认键盘固件包含 Studio 支持
2. 尝试重新连接 USB 或重新配对蓝牙
3. 刷新浏览器页面重试

### 修改不生效

1. 确认已正确选择对应的层
2. 检查是否有冲突的按键映射
3. 尝试断开重连键盘

### 导出配置问题

1. 确保完整下载了 keymap 文件
2. 检查文件格式是否正确
3. 对比原文件结构，确保语法正确
