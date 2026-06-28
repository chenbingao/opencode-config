---
description: 禁用 lua-convention skill
---
Run this exact command to disable the lua-convention skill:

bash -c 'jq "if .permission then . else . + {permission: {}} end | .permission.skill += {\"lua-convention\": \"deny\"}" /Users/shiro/.config/opencode/opencode.jsonc > /tmp/opencode_tmp.json && mv /tmp/opencode_tmp.json /Users/shiro/.config/opencode/opencode.jsonc'
