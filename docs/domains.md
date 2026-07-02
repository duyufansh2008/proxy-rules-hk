# Domain notes

Last checked: 2026-07-02

## Method

The rule files use three buckets:

1. AI service domains
2. Social media domains
3. Client-specific examples with a direct fallback

## Current files

- `clash/ruleset/ai.yaml`
- `clash/ruleset/social.yaml`
- `surge/ruleset/ai.list`
- `surge/ruleset/social.list`
- `quantumult-x/filter/ai.list`
- `quantumult-x/filter/social.list`
- `loon/ruleset/ai.list`
- `loon/ruleset/social.list`

## Notes

- Use small rule sets first.
- Avoid adding broad domains unless required.
- Re-check endpoints regularly.
- Keep credentials and private nodes outside this repository.
