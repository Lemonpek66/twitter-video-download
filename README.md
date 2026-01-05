# X Video Downloader | Twitter 视频下载工具

A simple web application to download videos from Twitter/X tweets.

一个简单的 Web 应用，用于下载 Twitter/X 推文中的视频。

<img src="cover.png" width="100%" alt="Project Cover">

## Features | 功能特性

- 🎬 Support Twitter/X video link parsing | 支持 Twitter/X 视频链接解析
- ⚡ Automatic video download | 自动下载视频
- 🔒 Proxy support via .env configuration | 通过 .env 配置代理支持
- 🧹 Automatic cleanup of temporary files | 自动清理临时文件

## Installation | 安装步骤

### 1. Install Python dependencies | 安装 Python 依赖

```bash
pip install -r requirements.txt
```

### 2. Configure proxy (if needed) | 配置代理（如需要）

Copy `.env.example` to `.env` and edit:

复制 `.env.example` 为 `.env` 并编辑：

```bash
cp .env.example .env
```

Edit `.env` file and set your proxy:

编辑 `.env` 文件并设置你的代理：

```bash
PROXY_URL=http://your-proxy-server:port
```

**Common proxy examples | 常见代理示例：**
- Corporate proxy | 公司代理: `http://proxy.company.com:8080`
- Clash: `http://127.0.0.1:7890`
- V2Ray: `http://127.0.0.1:10809`
- Shadowsocks: `socks5://127.0.0.1:1080`

**Note | 注意：** If you don't need a proxy, leave `PROXY_URL` empty or remove the line.

如果不需要代理，将 `PROXY_URL` 留空或删除该行。

## Run Application | 运行应用

```bash
python app.py
```

Visit | 访问: http://localhost:5000

## Usage | 使用方法

1. Open the application in your browser | 打开浏览器访问应用
2. Paste Twitter tweet link | 粘贴 Twitter 推文链接
   - Example | 例如：https://twitter.com/username/status/123456789
3. Click "Download Video" button | 点击"下载视频"按钮
4. Wait for processing, video will download automatically | 等待处理完成，视频会自动下载

## Tech Stack | 技术栈

- **Backend | 后端**: Flask
- **Video Parser | 视频解析**: yt-dlp
- **Frontend | 前端**: Native HTML/CSS/JavaScript

## Notes | 注意事项

- Conversion time depends on video length and quality | 转换时间取决于视频长度和质量
- Temporary files are stored in `temp_downloads/` | 临时文件存储在 `temp_downloads/` 目录
- Configure proxy in `.env` if needed | 如需代理请在 `.env` 中配置
- Proxy settings are not committed to Git (in `.gitignore`) | 代理设置不会提交到 Git（已在 `.gitignore` 中）

## Troubleshooting | 故障排除

**Error: Unable to parse link | 错误：无法解析链接**
- Check if the link is correct | 检查链接是否正确
- Ensure the tweet contains video content | 确保推文包含视频内容
- Private tweets may not be accessible | 私密推文可能无法访问

**Error: Network connection failed | 错误：网络连接失败**
- Configure proxy in `.env` file | 在 `.env` 文件中配置代理
- Check if proxy is running | 检查代理是否正在运行
- Verify proxy URL format is correct | 验证代理 URL 格式是否正确
