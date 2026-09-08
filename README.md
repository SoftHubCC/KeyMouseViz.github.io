# KeyMouseViz

键鼠可视化助手 - 让每一次点击和按键都清晰可见

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Platform](https://img.shields.io/badge/platform-Windows%2010%2F11-blue)](https://www.microsoft.com/windows)
[![Python](https://img.shields.io/badge/Python-3.13+-blue.svg)](https://www.python.org/)
[![PyQt5](https://img.shields.io/badge/PyQt5-5.15+-green.svg)](https://riverbankcomputing.com/software/pyqt/)

## 📥 下载

前往 [Releases](https://github.com/SoftHubCC/KeyMouseViz/releases) 页面下载最新版本：

| 文件 | 大小 | 说明 |
|------|------|------|
| `KeyMouseViz_installer_v1.0.0.exe` | 22 MB | 安装程序（一键安装，推荐） |
| `KeyMouseViz_portable_v1.0.0.zip` | 28 MB | 便携版（解压即用） |

## ✨ 功能特性

### 鼠标功能
- **轨迹高亮显示** - 实时可视化鼠标移动轨迹
- **点击效果动画** - 点击时显示醒目的视觉效果
- **坐标实时显示** - 随时查看鼠标精确坐标位置
- **聚光灯效果** - 突出显示鼠标周围区域

### 键盘功能
- **按键可视化** - 按下键盘时显示按键动画

### 工具辅助
- **放大镜效果** - 放大鼠标周围区域，便于精确定位
- **浮动工具栏** - 一键快速切换各项功能
- **窗口置顶选择器** - 轻松设置窗口置顶状态

### 快捷键
| 快捷键 | 功能 |
|--------|------|
| `Ctrl+Shift+1` | 切换鼠标高亮显示 |
| `Ctrl+Shift+2` | 切换点击效果 |
| `Ctrl+Shift+3` | 切换键盘显示 |
| `Ctrl+Shift+4` | 切换鼠标坐标显示 |
| `Ctrl+Shift+5` | 切换聚光灯效果 |
| `Ctrl+Shift+6` | 切换放大镜效果 |
| `` Ctrl+Shift+` `` | 切换浮动工具栏 |
| `Ctrl+Shift+T` | 切换窗口置顶 |
| `Ctrl+Shift+-` | 降低透明度 |
| `Ctrl+Shift+=` | 增加透明度 |
| `Ctrl+Shift+F1` | 打开设置 |
| `Ctrl+Shift+F2` | 退出程序 |

### 自定义
- **浮动工具栏颜色自定义** - 每个功能可独立设置启用状态颜色
- **配置文件** - 通过 `config/config.json` 调整各项参数

## 🚀 快速开始

### 方式一：便携版（推荐）
1. 下载 `KeyMouseViz_portable_v1.0.0.zip`
2. 解压到任意目录
3. 双击运行 `KeyMouseViz\KeyMouseViz.exe`

### 方式二：安装程序
1. 下载 `KeyMouseViz_installer_v1.0.0.exe`
2. 运行安装程序，按提示完成安装
3. 从开始菜单或桌面快捷方式启动

## 📂 项目结构

```
KeyMouseViz/
├── KeyMouseViz.py          # 主程序源码
├── KeyMouseViz.spec        # PyInstaller 打包配置
├── app_build.bat           # 打包脚本
├── app_run.bat             # 程序启动脚本
├── _build_msg.py           # 打包提示信息管理
├── _postbuild_fix.py       # 打包后处理脚本
├── config/
│   ├── app.ico             # 程序图标
│   ├── app.png             # 程序图标
│   ├── config.json         # 配置文件
│   └── floatbar/           # 浮动工具栏图标
│       ├── target.svg      # 鼠标高亮
│       ├── click.svg       # 点击效果
│       ├── keyboard.svg    # 键盘显示
│       ├── crosshair.svg   # 鼠标坐标
│       ├── sun-electricity.svg  # 聚光灯
│       └── list-search.svg     # 放大镜
└── dist/
    └── KeyMouseViz/        # 打包输出目录
        ├── KeyMouseViz.exe
        ├── config/
        └── _internal/
```

## 🛠️ 本地构建

### 环境要求
- Python 3.13+
- Windows 10/11

### 构建步骤
```bash
# 1. 创建虚拟环境
python -m venv venv
venv\Scripts\activate

# 2. 安装依赖
pip install -r requirements.txt
pip install pyinstaller

# 3. 运行打包脚本
.\app_build.bat
```

打包完成后，输出目录为 `dist/KeyMouseViz/`

## 📝 技术栈

- **GUI 框架**: PyQt5
- **键鼠控制**: pyautogui, pynput
- **系统交互**: pywin32
- **打包工具**: PyInstaller
- **UI 设计**: 自定义无边框窗口 + SVG 图标

## 📄 许可证

MIT License - 详见 [LICENSE](LICENSE) 文件

## 👥 作者

**雨意澜风**
- GitHub: [SoftHubCC](https://github.com/SoftHubCC)
- 网站: [softhub.cc](https://softhub.cc)

## 🙏 致谢

- [PyQt5](https://www.riverbankcomputing.com/software/pyqt/) - 跨平台 GUI 框架
- [pyautogui](https://pyautogui.readthedocs.io/) - 键鼠自动化库
- [pynput](https://github.com/moses-palmer/pynput) - 键鼠监听库
- [pywin32](https://pypi.org/project/pywin32/) - Windows API 封装

## 📊 更新日志

### v1.0.0 (2026-09-08)
- 初始版本发布
- 支持鼠标轨迹高亮、点击效果、按键显示
- 支持聚光灯、放大镜效果
- 支持浮动工具栏快速切换
- 支持窗口置顶选择器
- 支持快捷键操作
- 支持浮动工具栏颜色自定义
