# Chinese Prose Style

一个用于 Codex 的中文写作 Skill。它处理两类常见问题：工整但空泛的“AI 味”，以及为了显得像真人而添加的口语、情绪和虚构现场。

这套规则不维护高频词黑名单。它要求模型回到来源，检查每段是否有明确事实，并把替代机制的排比、抽象名词和装饰性比喻改成可核对的表达。

## Install

```bash
npx skills add tidego/chinese-prose-style-skill
```

显式调用：

```text
Use $chinese-prose-style to edit this Chinese article. Preserve verified facts and remove decorative metaphors.
```

## What it checks

- 第一人称经历、情绪和场景是否有来源；
- 假设风险是否被误写成已经发生的事件；
- 排比和对称句是否提供了真实信息；
- 抽象名词是否省略了行动者和动作；
- 比喻是否准确对应某个机制，还是只增加结论感；
- 口语、反问和短句是否在表演“像真人”。

完整的设计背景和研究资料见[中文“AI 味”是怎样被训练出来的？](https://guzhaolin.art/blog/chinese-ai-prose-style)。

## Limits

Skill 只在推理时提供约束，不会改变模型参数。它不能证明一段文字是否由 AI 生成，也不能替代作者的事实、经历和判断。目前没有正式基准证明它能稳定提升所有中文文体；仓库因此不声明确定的效果增益。

## License

[MIT](LICENSE)
