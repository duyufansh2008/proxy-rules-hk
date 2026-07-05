# Domain notes

Last checked: 2026-07-05

## Method

The rule files use three buckets:

1. AI service domains
2. Social media domains
3. Client-specific examples with a direct fallback

## Current files

- `clash/ruleset/ai.yaml`
- `clash/ruleset/social.yaml`
- `clash/ruleset/proxy.yaml`
- `surge/ruleset/ai.list`
- `surge/ruleset/social.list`
- `surge/ruleset/proxy.list`
- `surge/ruleset/google-ai.list`
- `quantumult-x/filter/ai.list`
- `quantumult-x/filter/social.list`
- `quantumult-x/filter/proxy.list`
- `loon/ruleset/ai.list`
- `loon/ruleset/social.list`
- `loon/ruleset/proxy.list`

## 2026-07-05 audit

- Synchronized AI rules across Clash, Surge, Quantumult X and Loon.
- Added Google Gemini / AI Studio domains to the main AI and combined proxy rules.
- Synchronized TikTok social rules across Clash, Surge, Quantumult X and Loon.
- Kept `surge/ruleset/proxy-lite.list` intentionally small for users who want a minimal starter set.

## Notes

- Use small rule sets first.
- Avoid adding broad domains unless required.
- Re-check endpoints regularly.
- Keep credentials and private nodes outside this repository.
