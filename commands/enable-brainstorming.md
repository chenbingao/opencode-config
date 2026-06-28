---
description: 启用 brainstorming skill
---
Run this exact command to enable the brainstorming skill:

bash -c 'jq "if .permission then . else . + {permission: {}} end | .permission.skill += {\"brainstorming\": \"allow\"}" /Users/shiro/.config/opencode/opencode.jsonc > /tmp/opencode_tmp.json && mv /tmp/opencode_tmp.json /Users/shiro/.config/opencode/opencode.jsonc'
