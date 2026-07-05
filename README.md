# proxy-rules-hk

**Language / 语言切换:** [中文](#中文) | [English](#english)

<a id="中文"></a>
## 中文

适用于 Clash、Surge、Quantumult X、Loon 及兼容客户端的香港代理分流规则集。本项目将常见 AI 服务与社交媒体域名放入代理规则，其他流量默认直连。

### 分流行为

```text
命中的规则集 -> Proxy
其他所有流量 -> DIRECT
```


### 订阅链接

原始文件基址：

```text
https://raw.githubusercontent.com/duyufansh2008/proxy-rules-hk/main/
```

| 客户端 | AI 规则 | 社交规则 | 合并规则 |
|---|---|---|---|
| Clash | `https://raw.githubusercontent.com/duyufansh2008/proxy-rules-hk/main/clash/ruleset/ai.yaml` | `https://raw.githubusercontent.com/duyufansh2008/proxy-rules-hk/main/clash/ruleset/social.yaml` | `https://raw.githubusercontent.com/duyufansh2008/proxy-rules-hk/main/clash/ruleset/proxy.yaml` |
| Surge | `https://raw.githubusercontent.com/duyufansh2008/proxy-rules-hk/main/surge/ruleset/ai.list` | `https://raw.githubusercontent.com/duyufansh2008/proxy-rules-hk/main/surge/ruleset/social.list` | `https://raw.githubusercontent.com/duyufansh2008/proxy-rules-hk/main/surge/ruleset/proxy.list` |
| Quantumult X | `https://raw.githubusercontent.com/duyufansh2008/proxy-rules-hk/main/quantumult-x/filter/ai.list` | `https://raw.githubusercontent.com/duyufansh2008/proxy-rules-hk/main/quantumult-x/filter/social.list` | `https://raw.githubusercontent.com/duyufansh2008/proxy-rules-hk/main/quantumult-x/filter/proxy.list` |
| Loon | `https://raw.githubusercontent.com/duyufansh2008/proxy-rules-hk/main/loon/ruleset/ai.list` | `https://raw.githubusercontent.com/duyufansh2008/proxy-rules-hk/main/loon/ruleset/social.list` | `https://raw.githubusercontent.com/duyufansh2008/proxy-rules-hk/main/loon/ruleset/proxy.list` |

### Clash 示例

```yaml
rule-providers:
  hk_proxy:
    type: http
    behavior: classical
    path: ./ruleset/hk-proxy.yaml
    url: https://raw.githubusercontent.com/duyufansh2008/proxy-rules-hk/main/clash/ruleset/proxy.yaml
    interval: 86400

rules:
  - RULE-SET,hk_proxy,Proxy
  - MATCH,DIRECT
```

### Surge 示例

```ini
[Rule]
RULE-SET,https://raw.githubusercontent.com/duyufansh2008/proxy-rules-hk/main/surge/ruleset/proxy.list,Proxy
FINAL,DIRECT
```

### Quantumult X 示例

```ini
[filter_remote]
https://raw.githubusercontent.com/duyufansh2008/proxy-rules-hk/main/quantumult-x/filter/proxy.list, tag=HK Proxy Rules, enabled=true
```

### Loon 示例

```ini
[Remote Rule]
https://raw.githubusercontent.com/duyufansh2008/proxy-rules-hk/main/loon/ruleset/proxy.list, policy=Proxy, tag=HK Proxy Rules, enabled=true
```

### 本次域名审查与更新

- 补齐各客户端之间不一致的 AI 域名：`oaistatic.com`、`oaiusercontent.com`、`openaiapi-site.azureedge.net`、`perplexity.ai`、`poe.com`、`cursor.sh`、`cursor.com`。
- 补齐 Google Gemini / AI Studio 相关域名：`gemini.google.com`、`aistudio.google.com`、`ai.google.dev`、`generativelanguage.googleapis.com`。
- 补齐 TikTok 相关社交域名：`tiktokv.com`、`tiktokcdn-us.com`、`tiktokd.net`、`tiktokd.org`、`musical.ly`、`muscdn.com` 与 `tiktok` 关键字规则。

### 后续可优化项

- 增加自动化脚本，从统一的域名清单生成 Clash、Surge、Quantumult X、Loon 文件，避免多端规则不同步。
- 增加 CI 校验，检查重复规则、格式错误、合并规则是否完整包含 AI 与社交规则。
- 将代理策略名 `Proxy` 做成文档变量说明，方便用户替换为自己的策略组名称。
- 视需求增加更细分规则集，例如 `google-ai`、`openai`、`tiktok`，让用户按服务单独订阅。

### 安全说明

请不要提交真实节点、机场订阅、账号凭据、密钥、令牌、密码或私人账号数据。更多说明见 `docs/domains.md` 与 `docs/security.md`。

<a id="english"></a>
## English

Routing rule sets for Clash, Surge, Quantumult X, Loon and compatible clients. The selected AI and social-media domains go through `Proxy`; all other traffic falls back to `DIRECT`.

### Behavior

```text
Matched rule sets -> Proxy
Everything else   -> DIRECT
```


### Subscription URLs

Raw base URL:

```text
https://raw.githubusercontent.com/duyufansh2008/proxy-rules-hk/main/
```

| Client | AI | Social | Combined |
|---|---|---|---|
| Clash | `https://raw.githubusercontent.com/duyufansh2008/proxy-rules-hk/main/clash/ruleset/ai.yaml` | `https://raw.githubusercontent.com/duyufansh2008/proxy-rules-hk/main/clash/ruleset/social.yaml` | `https://raw.githubusercontent.com/duyufansh2008/proxy-rules-hk/main/clash/ruleset/proxy.yaml` |
| Surge | `https://raw.githubusercontent.com/duyufansh2008/proxy-rules-hk/main/surge/ruleset/ai.list` | `https://raw.githubusercontent.com/duyufansh2008/proxy-rules-hk/main/surge/ruleset/social.list` | `https://raw.githubusercontent.com/duyufansh2008/proxy-rules-hk/main/surge/ruleset/proxy.list` |
| Quantumult X | `https://raw.githubusercontent.com/duyufansh2008/proxy-rules-hk/main/quantumult-x/filter/ai.list` | `https://raw.githubusercontent.com/duyufansh2008/proxy-rules-hk/main/quantumult-x/filter/social.list` | `https://raw.githubusercontent.com/duyufansh2008/proxy-rules-hk/main/quantumult-x/filter/proxy.list` |
| Loon | `https://raw.githubusercontent.com/duyufansh2008/proxy-rules-hk/main/loon/ruleset/ai.list` | `https://raw.githubusercontent.com/duyufansh2008/proxy-rules-hk/main/loon/ruleset/social.list` | `https://raw.githubusercontent.com/duyufansh2008/proxy-rules-hk/main/loon/ruleset/proxy.list` |

### Clash

```yaml
rule-providers:
  hk_proxy:
    type: http
    behavior: classical
    path: ./ruleset/hk-proxy.yaml
    url: https://raw.githubusercontent.com/duyufansh2008/proxy-rules-hk/main/clash/ruleset/proxy.yaml
    interval: 86400

rules:
  - RULE-SET,hk_proxy,Proxy
  - MATCH,DIRECT
```

### Surge

```ini
[Rule]
RULE-SET,https://raw.githubusercontent.com/duyufansh2008/proxy-rules-hk/main/surge/ruleset/proxy.list,Proxy
FINAL,DIRECT
```

### Quantumult X

```ini
[filter_remote]
https://raw.githubusercontent.com/duyufansh2008/proxy-rules-hk/main/quantumult-x/filter/proxy.list, tag=HK Proxy Rules, enabled=true
```

### Loon

```ini
[Remote Rule]
https://raw.githubusercontent.com/duyufansh2008/proxy-rules-hk/main/loon/ruleset/proxy.list, policy=Proxy, tag=HK Proxy Rules, enabled=true
```

### Domain audit and updates

- Added missing AI domains across clients: `oaistatic.com`, `oaiusercontent.com`, `openaiapi-site.azureedge.net`, `perplexity.ai`, `poe.com`, `cursor.sh`, and `cursor.com`.
- Added Google Gemini / AI Studio domains: `gemini.google.com`, `aistudio.google.com`, `ai.google.dev`, and `generativelanguage.googleapis.com`.
- Added TikTok-related social domains: `tiktokv.com`, `tiktokcdn-us.com`, `tiktokd.net`, `tiktokd.org`, `musical.ly`, `muscdn.com`, plus the `tiktok` keyword rule.

### Recommended improvements

- Add a generator script that builds Clash, Surge, Quantumult X, and Loon outputs from one canonical domain list.
- Add CI checks for duplicate rules, invalid formats, and combined-rule completeness.
- Document `Proxy` as a replaceable policy-group name so users can map it to their own clients.
- Add optional service-specific subscriptions such as `google-ai`, `openai`, and `tiktok`.

### Security

Do not commit real nodes, subscription links, credentials, keys, tokens, passwords or private account data. See `docs/domains.md` and `docs/security.md`.
