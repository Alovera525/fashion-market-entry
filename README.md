# fashion-market-entry

面向时尚、服饰、箱包品牌的新市场进入调研 Skill。它把“某品牌能不能进入某个国家或地区”拆成可核验的市场判断、风险闸门和落地策略，避免把估算、代理指标或未确认的库存分配写成事实。

> 当前版本：`0.1.0` · 兼容：Claude Code / Codex · 许可证：MIT

## 适合处理什么

| 场景 | 产出 |
|---|---|
| 判断品牌能否进入某市场 | 一页结论、否决条件和章节大纲 |
| 制定新国家市场策略 | 有来源、可追溯的 Markdown 调研文档 |
| 选择平台、价格带和目标人群 | 带假设、限制条件和验证动作的建议 |
| 审查已有市场报告 | 结构、证据、逻辑、重复和执行性检查 |

不适用于单品文案、已确定市场的日常运营排期或纯财务测算。

## 核心方法

1. 先确认委托方身份、货盘前提、市场与时间窗、平台和预算。
2. 把数字区分为可直接引用、需标注的推算值、尚未确定且不能给数三类。
3. 先检查授权、准入和品牌现有渠道等否决性风险，再继续画像与策略。
4. 将证据、判断、限制条件和执行动作连成闭环。
5. 先在对话里交付“一页结论 + 章节大纲”，方向确认后再生成完整 `.md`。

## 安装

### Claude Code

```bash
claude plugin marketplace add Alovera525/fashion-market-entry
claude plugin install fashion-market-entry@fashion-market-entry
```

安装后可直接提出需求，例如：

```text
请判断一个授权经销商是否适合用现有箱包库存进入马来西亚市场。先完成开工四问，再给一页结论和章节大纲。
```

### Codex

```bash
codex plugin marketplace add Alovera525/fashion-market-entry --ref main
codex plugin add fashion-market-entry@fashion-market-entry
```

安装后开启一个新的 Codex 任务，并直接描述目标市场、品牌身份和货盘条件。

## Skill 工作流

| 阶段 | 主要动作 | 交付 |
|---|---|---|
| 1. 开工判断 | 确认四个关键前提 | 明确研究边界 |
| 2. 方向确认 | 建立关键判断与否决点 | 一页结论 + 大纲 |
| 3. 调研与分析 | 查证市场、平台、竞品、合规和本地化 | 带来源的完整报告 |
| 4. 交付验证 | 核对数字、时间、一致性和可读性 | 数据缺口与待办清单 |

## 仓库结构

```text
fashion-market-entry/
├── .agents/plugins/marketplace.json
├── .claude-plugin/marketplace.json
├── plugins/fashion-market-entry/
│   ├── .claude-plugin/plugin.json
│   ├── .codex-plugin/plugin.json
│   └── skills/fashion-market-entry/
│       ├── SKILL.md
│       └── references/
├── README.md
└── LICENSE
```

## References

| 文件 | 用途 |
|---|---|
| `output-template.md` | 完整报告结构、表格骨架和可复用措辞 |
| `research-sources.md` | 按数据类型选择来源和检索路径 |
| `localization-checklist.md` | 气候、尺码、支付、履约、语言与文化核查 |
| `delivery-gates.md` | 数字、时间、逻辑、去重和交付前验证 |

## 使用边界

- 市场数据、法规、平台政策和价格会变化，使用时必须重新查询并注明日期。
- 推算值必须展示假设与算式，不把建议测试值写成市场事实。
- 社媒关注、榜单和评分只能作为代理指标，不能冒充真实销售份额。
- 本 Skill 提供研究与决策框架，不替代当地法务、税务或商业授权确认。

## 许可证

[MIT](LICENSE) © 2026 Alovera525
