---
description: 禁用 using-superpowers skill
---
Run this exact command to disable the using-superpowers skill:

bash -c 'jq "if .permission then . else . + {permission: {}} end | .permission.skill += {\"using-superpowers\": \"deny\"}" /Users/shiro/.config/opencode/opencode.jsonc > /tmp/opencode_tmp.json && mv /tmp/opencode_tmp.json /Users/shiro/.config/opencode/opencode.jsonc'
