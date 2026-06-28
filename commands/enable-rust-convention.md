---
description: 启用 rust-convention skill
---
Run this exact command to enable the rust-convention skill:

bash -c 'jq "if .permission then . else . + {permission: {}} end | .permission.skill += {\"rust-convention\": \"allow\"}" /Users/shiro/.config/opencode/opencode.jsonc > /tmp/opencode_tmp.json && mv /tmp/opencode_tmp.json /Users/shiro/.config/opencode/opencode.jsonc'
