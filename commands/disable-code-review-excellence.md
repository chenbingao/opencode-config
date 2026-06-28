---
description: 禁用 code-review-excellence skill
---
Run this exact command to disable the code-review-excellence skill:

bash -c 'jq "if .permission then . else . + {permission: {}} end | .permission.skill += {\"code-review-excellence\": \"deny\"}" /Users/shiro/.config/opencode/opencode.jsonc > /tmp/opencode_tmp.json && mv /tmp/opencode_tmp.json /Users/shiro/.config/opencode/opencode.jsonc'
