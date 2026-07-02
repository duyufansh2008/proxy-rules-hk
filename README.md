# proxy-rules-hk

Personal rules and configuration templates for **Clash**, **Surge**, **Quantumult X**, **Loon** and other proxy clients.

> ⚠️ This repository is public. Do **not** commit subscription URLs, proxy nodes, UUIDs, passwords, tokens, private keys, WireGuard private keys, API keys, or any paid service credentials.

## Structure

```text
proxy-rules-hk/
├── clash/
│   ├── ruleset/          # Clash rule-provider files
│   ├── providers/        # Provider templates; no real nodes
│   └── examples/         # Clash example configs
├── surge/
│   ├── ruleset/          # Surge RULE-SET files
│   ├── modules/          # Surge modules
│   └── examples/         # Surge example configs
├── quantumult-x/
│   ├── filter/           # Quantumult X filter rules
│   └── rewrite/          # Quantumult X rewrite rules
├── loon/
│   └── plugins/          # Loon plugin templates
└── docs/
    └── security.md       # Safety checklist
```

## Raw file base URL

```text
https://raw.githubusercontent.com/duyufansh2008/proxy-rules-hk/main/
```

## Clash example

```yaml
rule-providers:
  ai:
    type: http
    behavior: classical
    path: ./ruleset/ai.yaml
    url: https://raw.githubusercontent.com/duyufansh2008/proxy-rules-hk/main/clash/ruleset/ai.yaml
    interval: 86400

rules:
  - RULE-SET,ai,Proxy
  - GEOIP,CN,DIRECT
  - MATCH,Proxy
```

## Surge example

```ini
[Rule]
RULE-SET,https://raw.githubusercontent.com/duyufansh2008/proxy-rules-hk/main/surge/ruleset/ai.list,Proxy
GEOIP,CN,DIRECT
FINAL,Proxy
```

## Current rule sets

| Tool | File | Purpose |
|---|---|---|
| Clash | `clash/ruleset/ai.yaml` | Common AI service domains |
| Surge | `surge/ruleset/ai.list` | Common AI service domains |

## Maintenance rules

- Keep real proxy nodes outside this repository.
- Put only rules, templates and documentation here.
- Before every commit, check for sensitive strings such as `token`, `password`, `uuid`, `private_key`, `subscription`, `airport`, `server`, `passwd`.
- Prefer small, clearly named rule files rather than one huge mixed file.
