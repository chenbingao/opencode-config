---
description: 启用 find-skills skill
---
Run this exact command to enable the find-skills skill:

bash -c 'jq "if .permission then . else . + {permission: {}} end | .permission.skill += {\"find-skills\": \"allow\"}" /Users/shiro/.config/opencode/opencode.jsonc > /tmp/opencode_tmp.json && mv /tmp/opencode_tmp.json /Users/shiro/.config/opencode/opencode.jsonc'
