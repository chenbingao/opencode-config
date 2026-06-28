---
description: 禁用 commit-convention skill
---
Run this exact command to disable the commit-convention skill:

bash -c 'jq "if .permission then . else . + {permission: {}} end | .permission.skill += {\"commit-convention\": \"deny\"}" /Users/shiro/.config/opencode/opencode.jsonc > /tmp/opencode_tmp.json && mv /tmp/opencode_tmp.json /Users/shiro/.config/opencode/opencode.jsonc'
