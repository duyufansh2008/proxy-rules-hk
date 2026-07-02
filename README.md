# proxy-rules-hk

Routing rule sets for Clash, Surge, Quantumult X, Loon and compatible clients.

## Behavior

```text
Selected rule sets -> Proxy
Everything else    -> DIRECT
```

## Raw base

```text
https://raw.githubusercontent.com/duyufansh2008/proxy-rules-hk/main/
```

## Files

| Client | AI | Social | Combined |
|---|---|---|---|
| Clash | `clash/ruleset/ai.yaml` | `clash/ruleset/social.yaml` | `clash/ruleset/proxy.yaml` |
| Surge | `surge/ruleset/ai.list` | `surge/ruleset/social.list` | `surge/ruleset/proxy.list` |
| Quantumult X | `quantumult-x/filter/ai.list` | `quantumult-x/filter/social.list` | `quantumult-x/filter/proxy.list` |
| Loon | `loon/ruleset/ai.list` | `loon/ruleset/social.list` | `loon/ruleset/proxy.list` |

## Clash

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

## Surge

```ini
[Rule]
RULE-SET,https://raw.githubusercontent.com/duyufansh2008/proxy-rules-hk/main/surge/ruleset/proxy.list,Proxy
FINAL,DIRECT
```

## Quantumult X

```ini
[filter_remote]
https://raw.githubusercontent.com/duyufansh2008/proxy-rules-hk/main/quantumult-x/filter/proxy.list, tag=HK Proxy Rules, enabled=true
```

## Loon

```ini
[Remote Rule]
https://raw.githubusercontent.com/duyufansh2008/proxy-rules-hk/main/loon/ruleset/proxy.list, policy=Proxy, tag=HK Proxy Rules, enabled=true
```

## Security

Do not commit real nodes, subscription links, credentials, keys, tokens, passwords or private account data.

See `docs/domains.md` and `docs/security.md`.
