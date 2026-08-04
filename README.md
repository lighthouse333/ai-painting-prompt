<p align="center">
  <a href="README_CN.md">🇨🇳 中文</a>
  &nbsp;|&nbsp;
  <a href="README_EN.md">🇬🇧 English</a>
</p>

---

# AI绘画提示词生成器

基于《女性人物肖像参数化描写模板》的 Claude Code 技能 — 输入人物特征，自动生成 28 维度 AI 绘画提示词（.docx）。

📖 **[完整中文文档 →](README_CN.md)**

---

# AI Painting Prompt Generator

A Claude Code skill that generates complete 28-dimension AI painting prompts from natural language character descriptions.

📖 **[Full English Documentation →](README_EN.md)**

---

## Quick Install

```bash
git clone https://github.com/lighthouse333/ai-painting-prompt.git
cd ai-painting-prompt
# Open in Claude Code, then:
/ai-painting-prompt <your character description>
```

## Files

| File | Description |
|------|-------------|
| `README_CN.md` | 完整中文文档 |
| `README_EN.md` | Full English documentation |
| `.claude/commands/` | Claude Code slash command |
| `女性人物肖像参数化描写模板.md` | 28-dimension reference template |
| `generate_prompt.py` | Reference script for .docx generation |
