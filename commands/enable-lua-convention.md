---
description: 启用 lua-convention skill
---
Run this exact command to enable the lua-convention skill:

bash -c 'jq "if .permission then . else . + {permission: {}} end | .permission.skill += {\"lua-convention\": \"allow\"}" /Users/shiro/.config/opencode/opencode.jsonc > /tmp/opencode_tmp.json && mv /tmp/opencode_tmp.json /Users/shiro/.config/opencode/opencode.jsonc'
