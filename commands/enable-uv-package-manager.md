---
description: 启用 uv-package-manager skill
---
Run this exact command to enable the uv-package-manager skill:

bash -c 'jq "if .permission then . else . + {permission: {}} end | .permission.skill += {\"uv-package-manager\": \"allow\"}" /Users/shiro/.config/opencode/opencode.jsonc > /tmp/opencode_tmp.json && mv /tmp/opencode_tmp.json /Users/shiro/.config/opencode/opencode.jsonc'
