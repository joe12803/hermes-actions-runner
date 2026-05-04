# Hermes Agent GitHub Actions Runner

利用 GitHub Actions 运行 Hermes Agent，支持飞书网关、自定义模型和 Cloudflare Tunnel 临时 Web UI。

## 配置指南 (GitHub Secrets)

请在仓库的 `Settings > Secrets and variables > Actions` 中添加以下密钥：

1.  **`CUSTOM_API_KEY`**: 你的 API Key (例如：`sk-KhbSk9pyLHkw8AzPy`)。
2.  **`FEISHU_APP_ID`**: 飞书 App ID (`cli_a94be190f6b89cc4`)。
3.  **`FEISHU_APP_SECRET`**: 飞书 App Secret (`yNcA22fNJaYDeUXGbedb5c36SuUwkVvh`)。

## 功能说明

### 1. 飞书网关 (Feishu Gateway)
在运行工作流时勾选 `run_gateway`。Hermes 将作为飞书机器人在线运行。

### 2. 临时 Web UI (Cloudflare Tunnel)
勾选 `run_webui`。工作流将启动 `cloudcli` Web 界面，并通过 Cloudflare Tunnel 生成一个临时公网 URL。
> **注意**: 你需要在 Actions 的日志输出中查看 `cloudflared` 生成的 `trycloudflare.com` 地址。

### 3. 自定义模型
已预配置使用 `gemini-3-flash` 模型，API Base 为 `https://openclaw.994938.xyz/v1`。

## 使用方法

- 进入 **Actions** 选项卡。
- 选择 **Hermes Agent Runner**。
- 点击 **Run workflow**，根据需要配置参数。
