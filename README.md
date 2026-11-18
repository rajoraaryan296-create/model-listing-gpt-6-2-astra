# 模型上架：gpt-6.2-astra、gpt-6.2-sol！

OpenAI 在 **2026 年 11 月 17 日** 发布了 GPT-6.2 Astra 和 GPT-6.2 Sol。第二天，第三方接口聚合站 momoAPIPro（[tryallapi.com](https://tryallapi.com/)）的系统公告写明这两个模型已经上架，模型 ID 分别是 `gpt-6.2-astra` 和 `gpt-6.2-sol`。

要在自己的项目或脚本里按量调用，可以从这个注册入口进入：[https://tryallapi.com/register?aff=5A6A](https://tryallapi.com/register?aff=5A6A)。

本文按 **2026 年 11 月 18 日（Asia/Shanghai，UTC+8）** 对公开页面、系统公告和当日定价数据的复核来写。需要先说清楚：tryallapi.com / momoAPIPro 是**第三方 API 聚合站**，不是 OpenAI 官网，也不是官方 API。模型是否在线、分组是否开放、以及按量价格都会变，请以当天控制台和模型广场为准。

## 这两个模型是什么

根据 [OpenAI 官方介绍](https://openai.com/index/introducing-gpt-6-2-astra-sol) 和 [API 文档](https://developers.openai.com/api/docs/guides/latest-model)：

- **GPT-6.2 Astra**（`gpt-6.2-astra`）：官方定位为面向最难项目的旗舰模型，适合复杂专业工作、编码、科研，以及文档和演示制作。
- **GPT-6.2 Sol**（`gpt-6.2-sol`）：官方定位为更高效的日常工作模型，适合写作、改代码、审 PR、把会议记录整理成简报这类多步骤任务。官方写明，它的 API 代币价格与 GPT-6.1 Sol 保持一致。

官方还写到：这两个模型都支持文本和图像输入、文本输出；已在 ChatGPT Work、Codex 和 API 中上线。API 侧建议使用 Responses API；工具调用需要走 Responses，而不是只靠 Chat Completions。

OpenAI 公布的 **Standard 短上下文** 标价（USD / 1M tokens，2026-11-18 核对 [官方定价页](https://developers.openai.com/api/docs/pricing)）是：

| 模型 | 输入 | 缓存命中 | 输出 |
| --- | --- | --- | --- |
| gpt-6.2-astra | $8.00 | $0.40 | $40.00 |
| gpt-6.2-sol | $2.00 | $0.10 | $10.00 |

官方说明：Astra 的输入和输出价格比 GPT-6 Astra 低 20%，缓存输入有 60% 折扣。长上下文，以及 Batch、Fast、Ultrafast 等档位另有标价，这里不展开，以官方定价页为准。

## 渠道：tryallapi.com（momoAPIPro）按量 API

- **站点：** [https://tryallapi.com/](https://tryallapi.com/)
- **注册入口：** [https://tryallapi.com/register?aff=5A6A](https://tryallapi.com/register?aff=5A6A)

这一条面向要在自己的项目、脚本或客户端里调用模型的人，不是 ChatGPT 官方网页。站点品牌是 **momoAPIPro**，定位是按量计费的 API 聚合。

2026 年 11 月 18 日 16:33（Asia/Shanghai）左右，站点系统公告发出：「模型上架：gpt-6.2-astra、gpt-6.2-sol」。

![momoAPIPro 系统公告：gpt-6.2-astra、gpt-6.2-sol 已上架](https://upload.maynor1024.live/file/1794991517126_01-tryallapi-announcement.png)

> 图注：2026-11-18 系统公告截图。同日公告里也能看到部分其他模型或分组因资源紧张暂时下架，可见上架并不等于所有分组都一直可用。

同日公开定价数据里，这两个模型的厂商标注为 OpenAI，计费类型为按量，状态为可用。站点上的模型说明分别是：

- `gpt-6.2-astra`：可以构建和修改软件、操作计算机以及处理文档。支持文本和图像输入，并以文本形式响应。在 Responses API 中，可使用多智能体测试版将任务委派给子智能体执行。
- `gpt-6.2-sol`：支持文本和图像输入，并输出文本。可通过 Responses API 将其与网页搜索、计算机操作等工具配合使用。

支持的 API 接点类型为：

- `openai`（OpenAI 兼容 Chat Completions）
- `openai-response`（Responses API）

同日现网首页的接入示例里，OpenAI 兼容 Base URL 写的是 `https://tryallapi.com/v1`。文档站点有时也会出现 `https://api.maynorai.asia/v1`。具体以控制台、文档和当日表单展示为准。调用时把 `model` 设成 `gpt-6.2-astra` 或 `gpt-6.2-sol`。如果要用官方文档里强调的工具调用，优先走 Responses 接点。

### 分组价格（2026-11-18 公开定价数据）

单位是 **USD / 1M Tokens**，按量计费。下表按 2026 年 11 月 18 日的公开定价数据计算，使用前请回到模型广场或定价页核对。同一模型在不同分组里价差很大：**不要默认所有分组都比官方便宜**。

**gpt-6.2-astra**

| 分组 | 输入 | 补全 | 缓存命中 |
| --- | --- | --- | --- |
| Codex-Gpt-1 | $0.6472 | $3.2358 | $0.0324 |
| Codex-Gpt-2 | $1.0354 | $5.1770 | $0.0518 |
| Codex-Gpt-3 | $1.2941 | $6.4706 | $0.0647 |
| Openai-Gpt-1 | $10.3530 | $51.7651 | $0.5177 |
| Openai-Gpt-2 | $12.9413 | $64.7064 | $0.6471 |

**gpt-6.2-sol**

| 分组 | 输入 | 补全 | 缓存命中 |
| --- | --- | --- | --- |
| Codex-Gpt-1 | $0.1618 | $0.8089 | $0.0081 |
| Codex-Gpt-2 | $0.2589 | $1.2943 | $0.0129 |
| Codex-Gpt-3 | $0.3235 | $1.6177 | $0.0162 |
| Openai-Gpt-1 | $2.5883 | $12.9413 | $0.1294 |
| Openai-Gpt-2 | $3.2353 | $16.1766 | $0.1618 |

对照官方 Standard 短上下文标价：最便宜的 **Codex-Gpt-1** 输入大约是官方标价的 8.1%（约省 92%）。**Openai-Gpt-1 / Openai-Gpt-2** 则高于官方标价，例如 Astra 在 Openai-Gpt-1 的输入是 $10.3530，已经超过官方的 $8.00。如果控制台提供「价格优先」一类智能路由，更适合偶尔按量用的人；手动选分组时，先看价格和该分组是否仍在开放。

这两条模型的定价数据里没有单独给出 5 分钟或 1 小时缓存创建价格，所以这里只列出输入、补全和缓存命中，不补写未见的数字。长上下文或其他服务档位，请以当天页面为准。

另外，廉价分组也可能因资源紧张被临时下架。就在这则上架公告之前，站点还提示过 AWS-Gpt-1 等分组资源紧缺、暂时下架——这提醒我们：公告上架只说明模型已出现在目录里，不保证某个低价分组随时都能打通，也不保证无等待。

## 怎么接入

1. 打开 [https://tryallapi.com/register?aff=5A6A](https://tryallapi.com/register?aff=5A6A) 注册并登录。
2. 在控制台创建令牌（API Key）。不要把密钥发到聊天、截图或文章里。
3. 把客户端的 Base URL 设为站点当时展示的地址（首页示例是 `https://tryallapi.com/v1`），`model` 填写 `gpt-6.2-sol` 或 `gpt-6.2-astra`。
4. 日常任务可以先用 Sol，遇到更重的项目再换成 Astra。实际扣费以控制台账单和当时命中的分组为准。
