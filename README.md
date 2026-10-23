# Paper Reading Skill

A source-grounded skill for understanding one research paper at a time. By default, it combines a quick overview, standard analysis, and sequential accompaniment. It works with a paper PDF, link, DOI, arXiv ID, title, or pasted text.

## What it does

- Default workflow: quick takeaway and field classification, standard analysis, then sequential accompaniment
- Deep-read checks for task inputs and outputs, dataset provenance and splits, baselines, ablations, and evaluation metrics
- Sequential accompaniment: paragraph-by-paragraph concise translation with cited figures, tables, and equations explained inline in source order; named objects are reached through their section in reading order
- After the complete sequential accompaniment: three paper-grounded ideas or methods to borrow, three candidate application fields, and three concrete research proposals for A-tier venues
- Plain-language explanations of the research question, method, equations, and evidence
- Figure and table interpretation that is explicit about what was actually inspected
- Clear separation between author claims, reported evidence, and interpretation
- Coverage of empirical, theoretical, and systems papers without forcing every paper into one template

It is not a paper search engine or an automatic daily-paper recommendation system. A complete paper accompaniment can take multiple turns; at each stopping point, it reports where it will resume. You can ask for a narrower mode, such as a quick screen only. It does not default to multi-paper review or a long audit report.

## Install for Codex

Copy this folder into your personal Codex skills directory:

```bash
mkdir -p "${CODEX_HOME:-$HOME/.codex}/skills/paper-reading"
cp SKILL.md "${CODEX_HOME:-$HOME/.codex}/skills/paper-reading/SKILL.md"
```

Restart or refresh Codex if the skill does not appear immediately. The skill can also be installed by a compatible agent skill installer that supports the `SKILL.md` format.

## Use

Share a paper or its identifier and say what you want to understand. For example:

- "快速讲一下这篇论文，重点告诉我值不值得细读。"
- "一句话讲清这篇论文，并告诉我它属于什么领域。"
- "解释一下这篇论文。" (default: quick overview, standard analysis, then sequential accompaniment)
- "Walk me through the method and explain the key equation."
- "按顺序伴读 Figure 3 所在章节，读到图时解释它是否支持作者的主张。"
- "Give me a deeper critical read of this paper."
- "逐段精炼翻译这篇论文的 Introduction，段落顺序和引用保留。"
- "按文章顺序伴读：每段先精炼翻译，遇到公式、图或表就紧接着解释，再继续下一段。"
- "完整顺序伴读后，接着给出三个可借鉴的想法、三个迁移领域，以及三个面向 A 类会议的具体研究 idea。"
- "深入拆解实验：数据集从哪来、怎么划分、baseline 和 ablation 分别是什么、指标怎么解释？"

## Project layout

```text
paper-reading/
|-- SKILL.md
|-- README.md
`-- LICENSE
```

## License

MIT. See [LICENSE](LICENSE).
