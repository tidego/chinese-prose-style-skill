# Chinese Prose Style

一个用于 Codex 的中文写作与产品文案 Skill。它处理工整但空泛的“AI 味”、为了显得像真人而添加的虚构现场，以及把调研或开发过程泄漏进最终成品的元叙述。

这套规则不维护高频词黑名单。它要求模型回到来源，检查每段是否有明确事实，并把替代机制的排比、抽象名词和装饰性比喻改成可核对的表达。

## Install

```bash
npx skills add tidego/chinese-prose-style-skill
```

显式调用：

```text
Use $chinese-prose-style to edit this Chinese article or product copy. Preserve verified facts, prioritize the main claim, state evidence boundaries, and remove decorative metaphors and process-focused meta-narration.
```

## What it checks

- 第一人称经历、情绪和场景是否有来源；
- 假设风险是否被误写成已经发生的事件；
- 长文是否有明确主张，章节是否按重要性分配篇幅；
- 具体案例和权威归因是否能追溯到来源；
- 重要结论是否区分事实、推断和未决问题；
- 正文是否残留调研障碍、修改记录、章节预告或措辞选择；
- 产品文案是否描述用户对象和状态，而不是开发计划或 Agent 汇报；
- 排比和对称句是否提供了真实信息；
- 抽象名词是否省略了行动者和动作；
- 比喻是否准确对应某个机制，还是只增加结论感；
- 一个比喻是否被继续拆成整段映射，相邻章节是否重复同一模板；
- 情绪强度是否来自作者原稿；
- 口语、反问和短句是否在表演“像真人”。

Skill 不会机械禁用破折号、冒号或某个高频词。单个形式不是证据，反复出现且没有信息作用时才需要修改。

完整的设计背景和研究资料见[中文“AI 味”是怎样被训练出来的？](https://guzhaolin.art/blog/chinese-ai-prose-style)。

## Limits

Skill 只在推理时提供约束，不会改变模型参数。它不能证明一段文字是否由 AI 生成，也不能替代作者的事实、经历和判断。目前没有正式基准证明它能稳定提升所有中文文体；仓库因此不声明确定的效果增益。

## License

[MIT](LICENSE)
