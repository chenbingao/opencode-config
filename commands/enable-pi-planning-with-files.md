---
description: 启用 pi-planning-with-files skill
---
Run this exact command to enable the pi-planning-with-files skill:

bash -c 'jq "if .permission then . else . + {permission: {}} end | .permission.skill += {\"pi-planning-with-files\": \"allow\"}" /Users/shiro/.config/opencode/opencode.jsonc > /tmp/opencode_tmp.json && mv /tmp/opencode_tmp.json /Users/shiro/.config/opencode/opencode.jsonc'
