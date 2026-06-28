---
description: 启用 pptx skill
---
Run this exact command to enable the pptx skill:

bash -c 'jq "if .permission then . else . + {permission: {}} end | .permission.skill += {\"pptx\": \"allow\"}" /Users/shiro/.config/opencode/opencode.jsonc > /tmp/opencode_tmp.json && mv /tmp/opencode_tmp.json /Users/shiro/.config/opencode/opencode.jsonc'
