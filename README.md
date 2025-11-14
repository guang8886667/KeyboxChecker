# Keybox Checker
[![actions](https://github.com/KimmyXYC/KeyboxChecker/actions/workflows/ruff.yml/badge.svg)](https://github.com/KimmyXYC/KeyboxChecker/actions/workflows/ruff.yaml)
[![actions](https://github.com/KimmyXYC/KeyboxChecker/actions/workflows/docker-ci.yml/badge.svg)](https://github.com/KimmyXYC/KeyboxChecker/actions/workflows/docker-ci.yaml)
## 部署

- 下载源码。
```shell
git clone https://github.com/KimmyXYC/KeyboxChecker.git
cd KeyboxChecker
```

- 复制配置文件。
```shell
cp .env.exp .env
```

- 填写配置文件。
```
TELEGRAM_BOT_TOKEN=xxx
# TELEGRAM_BOT_PROXY_ADDRESS=socks5://127.0.0.1:7890
```

### 本地部署
- 安装依赖并运行。
```shell
pip3 install pdm
pdm install
pdm run python main.py
```
- 使用 PM2 守护进程。
```shell
pm2 start pm2.json
pm2 monit
pm2 restart pm2.json
pm2 stop pm2.json
```

### Docker 部署
- 使用预构建镜像。
```shell
docker run -d --name keyboxchecker --env-file .env ghcr.io/kimmyxyc/keyboxchecker:main
```

## 使用
在私聊中发送 keybox.xml 文件，或在 keybox.xml 文件消息下回复 /check

## 联系方式
- 个人联系方式（Telegram）：@guang8886667
- 交流群组：https://t.me/guang8886667_file

![Usage](./screenshot.png)
