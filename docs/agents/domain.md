# Domain Docs

engineering skill 探索代码库时，按本文件读项目的领域文档。本仓库为**单 context**（single-context）布局。

## 探索前读这些

- 根目录 **`CONTEXT.md`**（出海术语词典：出海 SaaS、目录站、躺赚、复利、SEO、外链、AITDK、SimilarWeb 等）。
- **`docs/adr/`**——读触及你即将改动区域的 ADR。

这些文件**不存在时，静默继续**。别指出缺失、别建议预先创建。`CONTEXT.md` 与 ADR 由 `domain-modeling` skill 在术语 / 决策真正谈拢时惰性创建。

## 格式与创建：归 domain-modeling

`CONTEXT.md` 的词汇表格式、ADR 的格式、何时够格开 ADR——**由 `domain-modeling` skill 规定**（见其 `references/CONTEXT-FORMAT.md` 与 `references/ADR-FORMAT.md`）。本文件只管**消费侧**：探索时怎么读、怎么用。不重复定义格式，避免两处漂移。

## 文件结构（单 context）

```
/
├── CONTEXT.md
├── docs/adr/
│   ├── 0001-...md
│   └── 0002-...md
└── ...（知识库：README.md + 1-选方向/ … 6-复盘增长/ + 原文/）
```

## 用 glossary 的词汇

当你的输出命名一个领域概念（issue 标题、重构提案、假设、测试名），用 `CONTEXT.md` 里定义的术语。**别漂移到 glossary 明确规避的同义词。**

你要的概念还不在 glossary 里，这是个 signal——要么你在发明项目不用的语言（重新考虑），要么真有缺口（记下给 `domain-modeling`）。

## 标出 ADR 冲突

如果你的输出和某条已有 ADR 矛盾，**显式摆出来**，别静默覆盖：

> _与 ADR-0007（...）冲突——但值得重开因为……_