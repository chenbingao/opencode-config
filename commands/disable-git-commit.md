---
description: 禁用 git-commit skill
---
Run this exact command to disable the git-commit skill:

bash -c 'jq "if .permission then . else . + {permission: {}} end | .permission.skill += {\"git-commit\": \"deny\"}" /Users/shiro/.config/opencode/opencode.jsonc > /tmp/opencode_tmp.json && mv /tmp/opencode_tmp.json /Users/shiro/.config/opencode/opencode.jsonc'
