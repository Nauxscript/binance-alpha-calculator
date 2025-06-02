# Alpha 月度利润计算器

## 简介

图形化 Alpha 月度利润计算器，支持 macOS 和 Windows 平台。界面美观，参数灵活，适合积分、余额、过期积分等多种场景的月度利润测算。

## 功能
- 支持输入日交易量档位、余额积分、每次领取预期收益、交易损耗率等参数
- 支持 15 天内积分滚动过期和领取扣除逻辑
- 自动计算真实交易量、余额档位、余额金额
- 结果一键显示，界面自适应，支持深色/浅色 mac 风格
- 支持 X（推特）和 GitHub 主页跳转

## 运行方法

1. 安装 Python 3（推荐 3.8 及以上，需自带 Tkinter）
2. 进入项目目录，运行：

```bash
python alpha_profit_calculator_tkinter.py
```

无需额外依赖。

## 打包为可执行文件

### macOS

```bash
pip install pyinstaller
pyinstaller --onefile --windowed alpha_profit_calculator_tkinter.py
```

生成的可执行文件在 `dist/` 目录下。

### Windows

请在 Windows 环境下运行：

```bash
pip install pyinstaller
pyinstaller --onefile --windowed alpha_profit_calculator_tkinter.py
```

### 跨平台自动打包（GitHub Actions）

本项目支持 GitHub Actions 自动打包 Windows 版本。参考 `.github/workflows/build-windows.yml`，推送到 main 分支或手动触发即可自动生成 Windows EXE 并下载。

## 主要参数说明
- **Ntl（日交易量档位）**：入账交易量 2^N USD 得 N 分
- **Pb（余额积分）**：余额积分，10^N USD 余额得 N-1 分
- **Ipdw（每次领取预期收益）**：每次领取的预期收益，默认 1000
- **Rdur（交易损耗率）**：默认 0.0002
- **15天前过期积分**：自动等于 Ntl，可手动修改

## 联系作者
- X: [@tan_maty](https://x.com/tan_maty)
- GitHub: [matyle](https://github.com/matyle)

---

如有建议或需求，欢迎 issue 或 PR！ 