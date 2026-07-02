# Security Checklist

This repository is public. Treat every committed file as permanently visible.

## Never commit

- Proxy subscription URLs
- Real proxy nodes
- Server IPs you do not want public
- UUIDs
- Passwords
- Tokens
- API keys
- Private keys
- WireGuard private keys
- Surge license or device credentials
- Paid service account data

## Before committing

Search the changed files for these keywords:

```text
token
password
passwd
secret
uuid
private_key
subscription
subscribe
机场
airport
server
sni
reality
wireguard
```

## Recommended workflow

1. Keep public rule files here.
2. Keep private node files only on your own device.
3. Use placeholders in examples.
4. If a secret is accidentally committed, rotate or revoke it immediately. Deleting the file from the latest commit is not enough, because Git history may still contain it.
