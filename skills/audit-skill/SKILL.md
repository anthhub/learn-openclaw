# audit-skill

> Skill 安全审计助手，用于 s09 教学

## 功能

对指定的 ClawHub Skill 执行基础安全扫描，输出审计报告。

## 触发方式

- 关键词：`审计 skill`、`扫描插件`、`audit skill`

## 参数

| 参数 | 类型 | 必填 | 说明 |
|------|------|------|------|
| skill_id | string | 是 | ClawHub 上的 Skill ID |
| deep_scan | boolean | 否 | 是否启用深度扫描（默认 false） |

## 示例

（待完善）

## 安全说明

此 Skill 仅读取 Skill 的公开元数据和代码，不会修改任何配置。
