---
description: 禁用 ts-convention skill
---
Run this exact command to disable the ts-convention skill:

bash -c 'jq "if .permission then . else . + {permission: {}} end | .permission.skill += {\"ts-convention\": \"deny\"}" /Users/shiro/.config/opencode/opencode.jsonc > /tmp/opencode_tmp.json && mv /tmp/opencode_tmp.json /Users/shiro/.config/opencode/opencode.jsonc'
