# xiaohongshu-note-generator-skill

把长文或主题改写成适合小红书发布的笔记，并产出可选标题与纯文本正文。

## Installation

This skill is intended to run in the local Codex/Gemini skill workspace.

If you are working in this repository, use the skill directly from:

```bash
.gemini/skills/xiaohongshu-note-generator-skill
```

## Documentation

# Xiaohongshu Note Generator

## Codex Compatibility
- 不依赖 `write_file` 等专用写文件工具。
- 默认输出结果给上层流水线，由上层决定何时保存到 `content/xiaohongshu/[topic-name]/02-xhs-note.md`。
- 如果上层流程要求确认，必须先展示 3 个候选标题，再等待用户选择或自定义。

## Output Requirements
- 标题提供 3 个候选，且每个不超过 20 字。
- 最终正文使用纯文本风格，不保留 Markdown 标题和列表语法。
- 段落之间保留真实空行，适合手机竖屏阅读。
- 避免套路化口吻和强 CTA。
