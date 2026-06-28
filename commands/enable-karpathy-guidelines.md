---
description: 启用 karpathy-guidelines skill
---
Run this exact command to enable the karpathy-guidelines skill:

bash -c 'jq "if .permission then . else . + {permission: {}} end | .permission.skill += {\"karpathy-guidelines\": \"allow\"}" /Users/shiro/.config/opencode/opencode.jsonc > /tmp/opencode_tmp.json && mv /tmp/opencode_tmp.json /Users/shiro/.config/opencode/opencode.jsonc'
