---
description: 启用 webapp-testing skill
---
Run this exact command to enable the webapp-testing skill:

bash -c 'jq "if .permission then . else . + {permission: {}} end | .permission.skill += {\"webapp-testing\": \"allow\"}" /Users/shiro/.config/opencode/opencode.jsonc > /tmp/opencode_tmp.json && mv /tmp/opencode_tmp.json /Users/shiro/.config/opencode/opencode.jsonc'
