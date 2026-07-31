# Sub2API

<div align="center">

[![Go](https://img.shields.io/badge/Go-1.25.7-00ADD8.svg)](https://golang.org/)
[![Vue](https://img.shields.io/badge/Vue-3.4+-4FC08D.svg)](https://vuejs.org/)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-15+-336791.svg)](https://www.postgresql.org/)
[![Redis](https://img.shields.io/badge/Redis-7+-DC382D.svg)](https://redis.io/)
[![Docker](https://img.shields.io/badge/Docker-Ready-2496ED.svg)](https://www.docker.com/)

<a href="https://trendshift.io/repositories/21823" target="_blank"><img src="https://trendshift.io/api/badge/repositories/21823" alt="Wei-Shaw%2Fsub2api | Trendshift" width="250" height="55"/></a>

**基于订阅配额分发的 AI API 网关平台**

[English](README.md) | 中文 | [日本語](README_JA.md)

</div>

## ⚠️ 重要声明

在使用本项目之前，请仔细阅读以下内容：

- **🚨 服务条款风险**：使用本项目可能违反 Anthropic 及其他上游提供商的服务条款。请在使用前仔细阅读相关提供商的用户协议；由此产生的一切风险均由用户自行承担。
- **⚖️ 合规使用**：请在遵守所在国家或地区法律法规的前提下使用本项目。严禁任何非法用途。
- **📖 免责声明**：本项目仅供技术学习和研究使用。作者不对因使用本项目而导致的账号封禁、服务中断、数据丢失或任何其他直接或间接损失承担责任。

## 概述

Sub2API 是一款 AI API 网关平台，用于分发和管理 AI 产品订阅中的 API 配额。用户可以通过平台生成的 API Key 访问上游 AI 服务，而平台则负责身份验证、计费、负载均衡和请求转发。

## 功能特性

- **多账号管理** - 支持多种上游账号类型（OAuth、API Key）
- **API Key 分发** - 为用户生成和管理 API Key
- **精确计费** - Token 级别的用量追踪和成本计算
- **智能调度** - 智能账号选择，支持粘性会话
- **并发控制** - 按用户和按账号的并发限制
- **速率限制** - 可配置的请求和 Token 速率限制
- **内置支付系统** - 支持 EasyPay、支付宝、微信支付和 Stripe 用户自助充值，无需单独部署支付服务（[配置指南](docs/PAYMENT_CN.md)）
- **管理后台** - 用于监控和管理的 Web 界面
- **外部系统集成** - 通过 iframe 嵌入外部系统（例如工单系统），扩展管理后台功能

## ❤️ 赞助商

> [想出现在这里？](mailto:support@pincc.ai)

<table>

<tr>
<td width="180"><a href="https://www.openmodel.ai?ref=sub2api"><img src="assets/partners/logos/openmodel.jpg" alt="openmodel" width="150"></a></td>
<td>一个 API，覆盖所有顶级模型！<a href="https://www.openmodel.ai?ref=sub2api">OpenModel</a> 是一个生产级、高可用的 AI API 网关，让你的应用真正快速且稳定：自动故障转移、智能路由至性能最佳的渠道，以及生产级 SLA。其 SLA 远超任何单一提供商——让稳定性成为你的核心竞争优势。可直接与 Claude Code、Codex 和 Gemini CLI 配合使用。通过此链接注册即可开始使用。</td>
</tr>

<tr>
<td width="180"><a href="https://etok.ai"><img src="assets/partners/logos/etok.png" alt="ETok" width="150"></a></td>
<td>感谢 ETok.ai 对本项目的赞助！ETok.ai 致力于构建一站式 AI 编程工具服务平台。我们提供专业的 Claude Code 套餐和技术社区服务，并支持 Google Gemini 和 OpenAI Codex。通过精心设计的套餐和专业的技术社区，我们为开发者提供可靠的服务保障和持续的技术支持，让 AI 辅助编程成为真正的生产力工具。点击<a href="https://etok.ai">此处</a>注册！</td>
</tr>

<tr>
<td width="180"><a href="https://aigocode.com/invite/SUB2API"><img src="assets/partners/logos/aigocode.png" alt="AIGoCode" width="150"></a></td>
<td>感谢 AIGoCode 对本项目的赞助！AIGoCode 是一个集成 Claude Code、Codex 和最新 Gemini 模型的一体化平台，为你提供稳定、高效且极具性价比的 AI 编程服务。平台提供灵活的订阅方案，零封号风险，无需 VPN 直连，响应速度极快。AIGoCode 为 sub2api 用户准备了专属福利：通过<a href="https://aigocode.com/invite/SUB2API">此链接</a>注册，首次充值可额外获得 10% 的奖励金！</td>
</tr>

<tr>
<td width="180"><a href="https://code.silkapi.com/register?aff=SUB2API"><img src="assets/partners/logos/silkapi.png" alt="silkapi" width="150"></a></td>
<td>感谢 SilkAPI 对本项目的赞助！<a href="https://code.silkapi.com/register?aff=SUB2API">SilkAPI</a> 是一个基于 Sub2API 构建的中继服务，专注于提供高速稳定的 Codex API 中继服务。</td>
</tr>

<tr>
<td width="180"><a href="https://www.aicodemirror.com/register?invitecode=KMVZQM"><img src="assets/partners/logos/AICodeMirror.jpg" alt="AICodeMirror" width="150"></a></td>
<td>感谢 AICodeMirror 对本项目的赞助！AICodeMirror 为 Claude Code / Codex / Gemini CLI 提供官方高稳定性中继服务，具备企业级并发、快速开票和 7×24 小时专属技术支持。Claude Code / Codex / Gemini 官方渠道分别仅需原价的 38% / 2% / 9%，充值还有额外折扣！AICodeMirror 为 sub2api 用户提供专属福利：通过<a href="https://www.aicodemirror.com/register?invitecode=KMVZQM">此链接</a>注册，首次充值可享 8 折优惠，企业客户最高可享 75 折优惠！</td>
</tr>

<tr>
<td width="180"><a href="https://shop.bmoplus.com/?utm_source=github"><img src="assets/partners/logos/bmoplus.jpg" alt="bmoplus" width="150"></a></td>
<td>非常感谢 BmoPlus 对本项目的赞助！BmoPlus 是专为重度 AI 用户和开发者打造的高可靠性 AI 账号提供商。他们提供坚实可靠、即买即用的 ChatGPT Plus / ChatGPT Pro（全保修）/ Claude Pro / Super Grok / Gemini Pro 账号及官方充值服务。通过 <a href="https://shop.bmoplus.com/?utm_source=github">BmoPlus - 优质 AI 账号与充值</a> 注册下单，用户可享受低至官方 GPT 订阅价格 10% 的震撼优惠（即 90% OFF）。</td>
</tr>

<tr>
<td width="180"><a href="https://bestproxy.com/?keyword=a2e8iuol"><img src="assets/partners/logos/bestproxy.png" alt="bestproxy" width="150"></a></td>
<td>感谢 Bestproxy 对本项目的赞助！<a href="https://bestproxy.com/?keyword=a2e8iuol">Bestproxy</a> 提供高纯度住宅 IP，支持一人一 IP 的专属方案。通过结合真实家庭网络和指纹隔离，实现链路环境隔离，降低基于关联性的风控概率。</td>
</tr>

<tr>
<td width="180"><a href="https://pateway.ai/?ch=1tsfr51"><img src="assets/partners/logos/pateway.png" alt="pateway" width="150"></a></td>
<td>感谢 PatewayAI 对本项目的赞助！<a href="https://pateway.ai/?ch=1tsfr51">PatewayAI</a> 是一个面向重度 AI 开发者的优质 API 中继平台，提供 100% 来自官方渠道的完整 Claude 和 Codex 系列，支持透明的 Token 级计费。企业版包含高并发、专属管理、合同和开票服务。立即注册即可获得 3 美元试用额度，充值低至 4 折，推荐奖励最高可达 150 美元。</td>
</tr>

<tr>
<td width="180"><a href="https://api.pptoken.org/register?promo=SUB2API"><img src="assets/partners/logos/pptoken.png" alt="pptoken" width="150"></a></td>
<td>感谢 PPToken.org 对本项目的赞助！<a href="https://api.pptoken.org/register?promo=SUB2API">PPToken.org</a> 专注于 GPT 模型 API 中继服务，支持 Codex、Claude Code、OpenAI 兼容客户端和 Gemini CLI 集成。充值比例为 1:1（1 元人民币 = 1 美元额度）；GPT 模型起价低至 0.16 倍率，整体成本约为官方定价的 2.2%，首 Token 延迟约 1 秒——是追求低成本、高速访问 GPT 模型能力的开发者的理想选择。技术支持：7×24 小时真人响应（非机器人），在群内 @tech 可在 10 分钟内获得回复。赞助福利：前 200 名通过<a href="https://api.pptoken.org/register?promo=SUB2API">专属注册链接</a>注册并填写优惠码 `SUB2API` 的用户，可免费领取 Codex / Claude Code 试用额度——无最低消费，无需绑卡。
</td>
</tr>

<tr>
<td width="180"><a href="https://runapi.co/register?aff=fu2E"><img src="assets/partners/logos/runapi.png" alt="RunAPI" width="150"></a></td>
<td>感谢 RunAPI 对本项目的赞助！<a href="https://runapi.co/register?aff=fu2E">RunAPI</a> 是一个高效稳定的 API 平台和 OpenRouter 替代方案。通过一个 API Key，即可访问 150 多个热门模型，包括 OpenAI、Claude、Gemini、DeepSeek 和 Grok，价格低至原价的 10%。稳定性极高，可无缝兼容 Claude Code 和 OpenClaw 等工具。
</td>
</tr>

<tr>
<td width="180"><a href="https://unity2.ai/register?source=sub2api"><img src="assets/partners/logos/unity2.png" alt="unity2" width="150"></a></td>
<td>感谢 Unity2 对本项目的赞助！<a href="https://unity2.ai/register?source=sub2api">Unity2</a> 是一款面向个人、团队和企业的高性能 AI 模型 API 中继平台，日处理量超过 300 亿 Token，支持 5000 RPM 并发。一个 API Key 即可在 Claude Code、Codex、OpenAI 模型、IDE 插件和 Agent 工作流中通用，支持余额计费、套餐订阅、企业开票和一对一支持。<a href="https://unity2.ai/register?source=sub2api">注册</a>即可领取 2 美元余额，加入官方群还可再获得 10 美元——最高可获 12 美元免费额度。
</td>
</tr>

<tr>
<td width="180"><a href="https://veilx.io/#/hello/SJRBRVDV"><img src="assets/partners/logos/veilx.png" alt="veilx" width="150"></a></td>
<td>感谢 Veilx 对本项目的赞助！<a href="https://veilx.io/#/hello/SJRBRVDV">Veilx</a> CDN 专为大规模 AI API 流量而设计，深度优化 OpenAI、Claude、Gemini 等中继服务和调用链，覆盖聊天、图像生成、嵌入和流式传输等场景，在高并发下提供更低的延迟和更高的稳定性。同时提供中国三网优化回程线路，非常适合全球 AI 中继平台、海外 AI SaaS 和跨境高并发部署。
</td>
</tr>

<tr>
<td width="180"><a href="https://roxybrowser.com/invite/bgGKG7"><img src="assets/partners/logos/RoxyBrowser.png" alt="veilx" width="150"></a></td>
<td>感谢 RoxyBrowser 对本项目的赞助！<a href="https://roxybrowser.com/invite/bgGKG7">RoxyBrowser</a> 是 Sub2API 的完美合作伙伴：内置原生 Roxy AI Agent 和高质量原生住宅 IP，支持通过简单命令批量自动化，大幅提升多账号管理的安全性和效率！点击<a href="https://roxybrowser.com/invite/bgGKG7">此链接</a>注册，即可获得免费的住宅 IP 套餐和终身 9 折优惠。
</td>
</tr>

<tr>
<td width="180"><a href="https://apikl.com"><img src="assets/partners/logos/apikl.png" alt="apikl" width="150"></a></td>
<td>感谢 Apikl 对本项目的赞助！该平台基于 Sub2API 构建，为开发者提供 Codex / Claude 系列模型的中继服务，注重长期稳定、高速直连和卓越性价比。支持按量计费余额充值、企业级官方发票和一对一专属支持。<a href="https://apikl.com">立即注册</a>可享 1:1 充值返现——余额翻倍！
</td>
</tr>

<tr>
<td width="180"><a href="https://tokeneum.ai"><img src="assets/partners/logos/tokeneum.png" alt="tokeneum" width="150"></a></td>
<td>感谢 TokenEum 对本项目的赞助！<a href="https://tokeneum.ai">TokenEum</a> 是一家综合性 AI 模型聚合平台和智能体开发公司。它汇集了包括 Claude、Gemini、OpenAI 在内的国际顶级模型，以及 GLM、Qwen、Kimi 等领先开源模型，提供不同质量和价格层次的多种选择，满足各类需求。TokenEum 还提供 Seedance2.0 和 Happy Horse 等前沿视频生成模型。秉持透明和诚信经营，TokenEum 确保所有模型信息真实可靠。访问 <a href="https://tokeneum.ai">tokeneum.ai</a> 开始使用。
</td>
</tr>

<tr>
<td width="180"><a href="https://sub.666api.ai"><img src="assets/partners/logos/666api.jpg" alt="666api" width="150"></a></td>
<td>感谢 666api 对本项目的赞助！<a href="https://sub.666api.ai">sub.666api.ai</a> 是一个一体化平台，提供：<br>
⚡ API 中继 — 按量付费访问 100% 来自官方渠道的全球模型，最高可享官方价格 75% 折扣<br>
&nbsp;&nbsp;&nbsp;&nbsp;独家优惠：智谱 GLM 5 折 · DeepSeek V4-pro 5 折 · Seedance 2.0 92% 折扣（需白名单）· HappyHorse 海外版 7 折（需白名单）<br>
🔑 GPT 订阅账号（含同源 IP）· 全球住宅 IP <br>
💰 支持开具发票
</td>
</tr>

</table>

## 生态系统

扩展或与 Sub2API 集成的社区项目：

| 项目 | 说明 | 功能 |
|---------|-------------|----------|
| ~~[Sub2ApiPay](https://github.com/touwaeriol/sub2apipay)~~ | ~~自助支付系统~~ | **现已内置** — 支付功能已集成到 Sub2API 中，无需单独部署。详见 [支付配置指南](docs/PAYMENT_CN.md) |
| [sub2api-mobile](https://github.com/ckken/sub2api-mobile) | 移动端管理控制台 | 跨平台应用（iOS/Android/Web），支持用户管理、账号管理、监控仪表盘和多后端切换；基于 Expo + React Native 构建 |

## 技术栈

| 组件 | 技术 |
|-----------|------------|
| 后端 | Go 1.25.7, Gin, Ent |
| 前端 | Vue 3.4+, Vite 5+, TailwindCSS |
| 数据库 | PostgreSQL 15+ |
| 缓存/队列 | Redis 7+ |

---

## Nginx 反向代理说明

当使用 Nginx 作为 Sub2API（或 CRS）的反向代理，并与 Codex CLI 配合使用时，请在 Nginx 配置的 `http` 块中添加以下内容：

```nginx
underscores_in_headers on;
```

Nginx 默认会丢弃包含下划线的请求头（例如 `session_id`），这会破坏多账号环境下的粘性会话路由。

---

## 部署方式

### 方式一：脚本安装（推荐）

一键安装脚本，从 GitHub Releases 下载预编译二进制文件。

#### 前置要求

- Linux 服务器（amd64 或 arm64）
- PostgreSQL 15+（已安装并运行）
- Redis 7+（已安装并运行）
- Root 权限

#### 安装步骤

```bash
curl -sSL https://raw.githubusercontent.com/Wei-Shaw/sub2api/main/deploy/install.sh | sudo bash
```

脚本将执行以下操作：
1. 检测系统架构
2. 下载最新版本
3. 安装二进制文件到 `/opt/sub2api`
4. 创建 systemd 服务
5. 配置系统用户和权限

#### 安装后操作

```bash
# 1. 启动服务
sudo systemctl start sub2api

# 2. 设置开机自启
sudo systemctl enable sub2api

# 3. 在浏览器中打开设置向导
# http://YOUR_SERVER_IP:8080
```

设置向导将引导你完成：
- 数据库配置
- Redis 配置
- 管理员账号创建

#### 升级

你可以直接在**管理后台**中点击左上角的**检查更新**按钮进行升级。

Web 界面将：
- 自动检查新版本
- 一键下载并应用更新
- 支持在需要时回滚

#### 常用命令

```bash
# 查看状态
sudo systemctl status sub2api

# 查看日志
sudo journalctl -u sub2api -f

# 重启服务
sudo systemctl restart sub2api

# 卸载
curl -sSL https://raw.githubusercontent.com/Wei-Shaw/sub2api/main/deploy/install.sh | sudo bash -s -- uninstall -y
```

---

### 方式二：Docker Compose（推荐）

使用 Docker Compose 部署，包含 PostgreSQL 和 Redis 容器。

#### 前置要求

- Docker 20.10+
- Docker Compose v2+

#### 快速开始（一键部署）

使用自动化部署脚本，轻松完成部署：

```bash
# 创建部署目录
mkdir -p sub2api-deploy && cd sub2api-deploy

# 下载并运行部署准备脚本
curl -sSL https://raw.githubusercontent.com/Wei-Shaw/sub2api/main/deploy/docker-deploy.sh | bash

# 启动服务
docker compose up -d

# 查看日志
docker compose logs -f sub2api
```

**脚本功能：**
- 下载 `docker-compose.local.yml`（保存为 `docker-compose.yml`）和 `.env.example`
- 生成安全凭证（JWT_SECRET、TOTP_ENCRYPTION_KEY、POSTGRES_PASSWORD）
- 创建包含自动生成密钥的 `.env` 文件
- 创建数据目录（使用本地目录，便于备份和迁移）
- 显示生成的凭证供参考

#### 手动部署

如果你更喜欢手动设置：

```bash
# 1. 克隆仓库
git clone https://github.com/Wei-Shaw/sub2api.git
cd sub2api/deploy

# 2. 复制环境配置
cp .env.example .env

# 3. 编辑配置（生成安全密码）
nano .env
```

**`.env` 中的必填配置：**

```bash
# PostgreSQL 密码（必填）
POSTGRES_PASSWORD=your_secure_password_here

# JWT 密钥（建议填写 — 重启后保持用户登录状态）
JWT_SECRET=your_jwt_secret_here

# TOTP 加密密钥（建议填写 — 重启后保持双因素认证）
TOTP_ENCRYPTION_KEY=your_totp_key_here

# 可选：管理员账号
ADMIN_EMAIL=admin@example.com
ADMIN_PASSWORD=your_admin_password

# 可选：自定义端口
SERVER_PORT=8080
```

**生成安全密钥：**
```bash
# 生成 JWT_SECRET
openssl rand -hex 32

# 生成 TOTP_ENCRYPTION_KEY
openssl rand -hex 32

# 生成 POSTGRES_PASSWORD
openssl rand -hex 32
```

```bash
# 4. 创建数据目录（本地目录版本）
mkdir -p data postgres_data redis_data

# 5. 启动所有服务
# 选项 A：本地目录版本（推荐 — 易于迁移）
docker compose -f docker-compose.local.yml up -d

# 选项 B：命名卷版本（简单设置）
docker compose up -d

# 6. 检查状态
docker compose -f docker-compose.local.yml ps

# 7. 查看日志
docker compose -f docker-compose.local.yml logs -f sub2api
```

#### 部署版本说明

| 版本 | 数据存储 | 迁移 | 适用场景 |
|---------|-------------|-----------|----------|
| **docker-compose.local.yml** | 本地目录 | ✅ 简单（打包整个目录即可） | 生产环境、频繁备份 |
| **docker-compose.yml** | 命名卷 | ⚠️ 需要 docker 命令 | 简单试用 |

**建议：** 使用 `docker-compose.local.yml`（由脚本部署），便于数据管理。

#### 访问

在浏览器中打开 `http://YOUR_SERVER_IP:8080`。

如果管理员密码是自动生成的，可在日志中查找：
```bash
docker compose -f docker-compose.local.yml logs sub2api | grep "admin password"
```

#### 升级

```bash
# 拉取最新镜像并重新创建容器
docker compose -f docker-compose.local.yml pull
docker compose -f docker-compose.local.yml up -d
```

#### 轻松迁移（本地目录版本）

使用 `docker-compose.local.yml` 时，可轻松迁移到新服务器：

```bash
# 在源服务器上
docker compose -f docker-compose.local.yml down
cd ..
tar czf sub2api-complete.tar.gz sub2api-deploy/

# 传输到新服务器
scp sub2api-complete.tar.gz user@new-server:/path/

# 在新服务器上
tar xzf sub2api-complete.tar.gz
cd sub2api-deploy/
docker compose -f docker-compose.local.yml up -d
```

#### 常用命令

```bash
# 停止所有服务
docker compose -f docker-compose.local.yml down

# 重启
docker compose -f docker-compose.local.yml restart

# 查看所有日志
docker compose -f docker-compose.local.yml logs -f

# 删除所有数据（谨慎操作！）
docker compose -f docker-compose.local.yml down
rm -rf data/ postgres_data/ redis_data/
```

---

### 方式三：从源码构建

从源码构建并运行，适用于开发或自定义需求。

#### 前置要求

- Go 1.21+
- Node.js 18+
- PostgreSQL 15+
- Redis 7+

#### 构建步骤

```bash
# 1. 克隆仓库
git clone https://github.com/Wei-Shaw/sub2api.git
cd sub2api

# 2. 安装 pnpm（如果尚未安装）
npm install -g pnpm

# 3. 构建前端
cd frontend
pnpm install
pnpm run build
# 输出目录为 ../backend/internal/web/dist/

# 4. 构建嵌入前端的后端
cd ../backend
go build -tags embed -o sub2api ./cmd/server

# 5. 创建配置文件
cp ../deploy/config.example.yaml ./config.yaml

# 6. 编辑配置
nano config.yaml
```

> **注意：** `-tags embed` 标志用于将前端嵌入二进制文件中。如果不带此标志构建，二进制文件将无法提供前端 UI。

**`config.yaml` 中的关键配置：**

```yaml
server:
  host: "0.0.0.0"
  port: 8080
  mode: "release"

database:
  host: "localhost"
  port: 5432
  user: "postgres"
  password: "your_password"
  dbname: "sub2api"

redis:
  host: "localhost"
  port: 6379
  password: ""

jwt:
  secret: "change-this-to-a-secure-random-string"
  expire_hour: 24

default:
  user_concurrency: 5
  user_balance: 0
  api_key_prefix: "sk-"
  rate_multiplier: 1.0
```

### Sora 状态（暂时不可用）

> ⚠️ 由于上游集成和媒体传输存在技术问题，Sora 相关功能暂时不可用。
> 请不要在生产环境中依赖 Sora。
> 现有的 `gateway.sora_*` 配置项已保留，但在问题解决前可能不会生效。

`config.yaml` 中还有更多安全相关选项：

- `cors.allowed_origins` 用于配置 CORS 允许列表
- `security.url_allowlist` 用于配置上游/定价/CRS 主机允许列表
- `security.url_allowlist.enabled` 用于关闭 URL 校验（谨慎使用）
- `security.url_allowlist.allow_insecure_http` 用于在校验关闭时允许 HTTP URL
- `security.url_allowlist.allow_private_hosts` 用于允许私有/本地 IP 地址
- `security.response_headers.enabled` 用于启用可配置的响应头过滤（禁用时使用默认允许列表）
- `security.csp` 用于控制 Content-Security-Policy 响应头
- `billing.circuit_breaker` 用于在计费错误时开启熔断
- `server.trusted_proxies` 用于启用 X-Forwarded-For 解析
- `turnstile.required` 用于在 release 模式下要求 Turnstile 验证

**⚠️ 安全警告：HTTP URL 配置**

当 `security.url_allowlist.enabled=false` 时，系统默认执行最小化的 URL 校验，**拒绝 HTTP URL**，仅允许 HTTPS。如需允许 HTTP URL（例如用于开发或内部测试），必须显式设置：

```yaml
security:
  url_allowlist:
    enabled: false                # 关闭允许列表检查
    allow_insecure_http: true     # 允许 HTTP URL（⚠️ 不安全）
```

**或通过环境变量设置：**

```bash
SECURITY_URL_ALLOWLIST_ENABLED=false
SECURITY_URL_ALLOWLIST_ALLOW_INSECURE_HTTP=true
```

**允许 HTTP 的风险：**
- API 密钥和数据以**明文**传输（易被截获）
- 易受**中间人（MITM）攻击**
- **不适合生产**环境

**何时可以使用 HTTP：**
- ✅ 开发/测试本地服务器（http://localhost）
- ✅ 信任的内部网络端点
- ✅ 在获得 HTTPS 之前测试账号连通性
- ❌ 生产环境（请仅使用 HTTPS）

**未配置此设置时的示例错误：**
```
Invalid base URL: invalid url scheme: http
```

如果你关闭了 URL 校验或响应头过滤，请加固网络层：
- 对外发流量实施上游域名/IP 允许列表
- 阻止私有/回环/链路本地地址范围
- 强制仅允许 TLS 出站流量
- 在代理层剥离敏感的上游响应头

```bash
# 6. 运行应用
./sub2api
```

#### 开发模式

```bash
# 后端（热重载）
cd backend
go run ./cmd/server

# 前端（热重载）
cd frontend
pnpm run dev
```

#### 代码生成

编辑 `backend/ent/schema` 后，重新生成 Ent + Wire：

```bash
cd backend
go generate ./ent
go generate ./cmd/server
```

---

## 简单模式

简单模式适用于希望快速使用、无需完整 SaaS 功能的个人开发者或内部团队。

- 启用方式：设置环境变量 `RUN_MODE=simple`
- 区别：隐藏与 SaaS 相关的功能，跳过计费流程
- 安全提示：在生产环境中，你还必须设置 `SIMPLE_MODE_CONFIRM=true` 才能允许启动

---

## Antigravity 支持

Sub2API 支持 [Antigravity](https://antigravity.so/) 账号。授权后，可使用 Claude 和 Gemini 模型的专属端点。

### 专属端点

| 端点 | 模型 |
|----------|-------|
| `/antigravity/v1/messages` | Claude 模型 |
| `/antigravity/v1beta/` | Gemini 模型 |

### Claude Code 配置

```bash
export ANTHROPIC_BASE_URL="http://localhost:8080/antigravity"
export ANTHROPIC_AUTH_TOKEN="sk-xxx"
```

### 混合调度模式

Antigravity 账号支持可选的**混合调度**。启用后，通用端点 `/v1/messages` 和 `/v1beta/` 也会将请求路由到 Antigravity 账号。

> **⚠️ 警告**：Anthropic Claude 和 Antigravity Claude**不能在同一对话上下文中混合使用**。请使用分组将它们正确隔离。

### 已知问题

在 Claude Code 中，Plan Mode 无法自动退出。（通常在使用原生 Claude API 时，规划完成后 Claude Code 会弹出选项让用户批准或拒绝计划。）

**解决方法**：按 `Shift + Tab` 手动退出 Plan Mode，然后输入你的回复以批准或拒绝计划。

---

## 项目结构

```
sub2api/
├── backend/                  # Go 后端服务
│   ├── cmd/server/           # 应用入口
│   ├── internal/             # 内部模块
│   │   ├── config/           # 配置
│   │   ├── model/            # 数据模型
│   │   ├── service/          # 业务逻辑
│   │   ├── handler/          # HTTP 处理器
│   │   └── gateway/          # API 网关核心
│   └── resources/            # 静态资源
│
├── frontend/                 # Vue 3 前端
│   └── src/
│       ├── api/              # API 调用
│       ├── stores/           # 状态管理
│       ├── views/            # 页面组件
│       └── components/       # 可复用组件
│
└── deploy/                   # 部署文件
    ├── docker-compose.yml    # Docker Compose 配置
    ├── .env.example          # Docker Compose 环境变量
    ├── config.example.yaml   # 二进制部署的完整配置文件
    └── install.sh            # 一键安装脚本
```

## 免责声明

> **在使用本项目之前，请仔细阅读：**
>
> :rotating_light: **服务条款风险**：使用本项目可能违反 Anthropic 的服务条款。请在使用前仔细阅读 Anthropic 的用户协议。使用本项目所产生的一切风险均由用户自行承担。
>
> :book: **免责声明**：本项目仅供技术学习和研究使用。作者不对因使用本项目而导致的账号封禁、服务中断或任何其他损失承担责任。

---

## Star 历史

<a href="https://star-history.com/#Wei-Shaw/sub2api&Date">
 <picture>
   <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/svg?repos=Wei-Shaw/sub2api&type=Date&theme=dark" />
   <source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/svg?repos=Wei-Shaw/sub2api&type=Date" />
   <img alt="Star History Chart" src="https://api.star-history.com/svg?repos=Wei-Shaw/sub2api&type=Date" />
 </picture>
</a>

---

## 许可证

本项目采用 [GNU Lesser General Public License v3.0](LICENSE)（或更新版本）授权。

Copyright (c) 2026 Wesley Liddick

---

<div align="center">

**如果这个项目对你有帮助，请给它点个 Star！**

</div>
