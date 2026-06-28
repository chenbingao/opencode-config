---
description: 查看所有skill的启用禁用状态并管理
---

## 任务

管理 opencode 的 skill 状态。

### 第一步：列出所有 skill 及其状态

1. 读取 `~/.agents/skills/` 下所有子目录名（排除 README.md）
2. 读取 `~/.config/opencode/opencode.jsonc`，查看 `permission.skill` 中每个 skill 的覆盖状态
3. skill 状态规则：
   - 如果 `permission.skill` 中没有该 skill 的条目 → 状态为「已启用」（默认 allow）
   - 如果设为 `"allow"` → 状态为「已启用」
   - 如果设为 `"deny"` → 状态为「已禁用」
   - 如果设为 `"ask"` → 状态为「每次询问」

### 第二步：展示给用户

用以下格式展示：

```
# Skill 状态一览

| Skill | 状态 |
|-------|------|
| brainstorming | ✅ 已启用 |
| commit-convention | ❌ 已禁用 |
| ... | ... |
```

### 第三步：询问用户

使用 question 工具询问用户要执行的操作：
- 选项应包含「退出不修改」+ 所有需要切换的 skill
- 每个 skill 显示为：「启用 xxx」（当当前为禁用时）或「禁用 xxx」（当当前为启用时）
- 支持多选

### 第四步：执行修改

直接编辑 `~/.config/opencode/opencode.jsonc`，在 `permission.skill` 中添加或修改对应 skill 的状态。

注意：
- 如果 `permission` 字段不存在，需要先创建
- 不要删除其他已有的配置
- 如果 status 改回默认（allow），可以直接移除该条目以保持配置简洁

### 第五步：完成

显示修改后的 skill 状态一览。
