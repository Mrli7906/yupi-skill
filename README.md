# yupi-skill —— 程序员鱼皮 Agent Skill

> 把我自己蒸馏成了一个 AI 技能包。装上它，AI 就能用我的思维方式、判断逻辑、说话习惯来回答问题。

[![Claude Code](https://img.shields.io/badge/Claude%20Code-Skill-blueviolet)](https://claude.ai/code)
[![Cursor](https://img.shields.io/badge/Cursor-Skill-blue)](https://cursor.com)
[![AgentSkills](https://img.shields.io/badge/AgentSkills-Standard-green)](https://agentskills.io)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

---

## 这是什么？

一个 [Agent Skills](https://agentskills.io) 标准的技能包，让 AI 以 **程序员鱼皮** 的身份回答问题。

不是简单的 "模仿语气"，而是完整蒸馏了我的：

- **心智模型** —— 我怎么看问题、怎么做判断
- **决策规则** —— 先生存再理想、不跳台阶、口头承诺不算数……
- **表达风格** —— 结论先行、自嘲式幽默、编号分点、"加油" 收尾
- **知识体系** —— 编程学习路线、求职指导、AI 编程、创业经验

## 我是谁？

98 年，前腾讯全栈工程师（SSP offer，竞赛冠军，5 星员工），现科技公司 [鱼鸢网络](https://yuyuanweb.com) CEO。

全网 200 万+ 粉丝的 AI + 编程知识博主，[编程导航](https://www.codefather.cn) 创始人，GitHub 中国区关注者前 7。

做了 10+ 个产品（编程导航、面试鸭、老鱼简历等），带大家做了近 30 套项目教程，累计创作近千万字。

> 更多信息：[B 站](https://space.bilibili.com/12890453) · [GitHub](https://github.com/liyupi) · [产品大全](https://dogyupi.com) · [公众号：程序员鱼皮]()

## 效果演示

### 求职咨询

```
用户：拿到银行外包 offer 13K，要不要接？

鱼皮：说实话，13K 双休、SpringCloud 技术栈、有微服务和高并发场景，
这个 offer 本身条件不算差。

我的建议是：先接了，但别停下找工作。有 offer 在手心态会好很多，
面试状态也会更好。

另外他说的"干两年调到资深中级给 15K"，这种口头承诺听听就好，别当真。

总结就是：有保底不慌，骑驴找马是最稳的策略。
```

### 学习规划

```
用户：Python 基础，想转 Java 全栈负责 AI 项目，怎么最快上手？

鱼皮：你有 Python 基础，转 Java 其实就是换个语法，上手会很快。
建议直接跟着项目学，先做用户中心项目把 Java + Vue3 的开发流程跑通，
然后做 AI 答题应用平台项目。之后再把 AI 超级智能体项目做了。
两到三个月够了。

另外日常开发记得用 AI 编程工具，学新技术栈效率能翻倍。
```

### 技术趋势

```
用户：大三学完 Spring Boot 了，要不要现在学 AI？

鱼皮：说直白点：现在不需要专门系统学 AI，但简历上必须有 AI 相关的东西。

会 AI 已经不是加分项，而是筛选条件。先把 Java 后端打扎实，
再做一个结合 AI 的项目就够了。大模型当调味料用就行，不用喧宾夺主。加油！
```

## 安装

### Claude Code

```bash
# 安装到当前项目
mkdir -p .claude/skills
git clone https://github.com/liyupi/yupi-skill.git .claude/skills/yupi-skill

# 或全局安装（所有项目可用）
git clone https://github.com/liyupi/yupi-skill.git ~/.claude/skills/yupi-skill
```

### Cursor

```bash
# 安装到当前项目
mkdir -p .cursor/skills
git clone https://github.com/liyupi/yupi-skill.git .cursor/skills/yupi-skill
```

### OpenClaw

```bash
git clone https://github.com/liyupi/yupi-skill.git ~/.openclaw/workspace/skills/yupi-skill
```

安装后 AI 会自动识别并在合适的场景使用此 Skill，也可以直接对 AI 说"用鱼皮的风格回答"来触发。

## Skill 结构

```
yupi-skill/
├── SKILL.md                          # 入口：触发条件、工作流、回答模式、局限性
└── references/
    ├── identity.md                   # 身份、7 个心智模型、决策规则、底线原则
    ├── voice.md                      # 句式特征、口头禅、幽默方式、回答模板
    └── knowledge-sources.md          # 6 个指定信息源、联网搜索规则
```

### 核心文件说明

| 文件 | 作用 | 何时加载 |
|------|------|----------|
| `SKILL.md` | 工作流入口，判断问题类型和回答模式 | AI 识别到相关场景时自动加载 |
| `identity.md` | 心智模型、决策规则、底线原则 | 需要做判断时加载 |
| `voice.md` | 表达风格、语气样本、回答模板 | 组织输出时加载 |
| `knowledge-sources.md` | 信息源映射、联网搜索指引 | 需要查实时信息时加载 |

## 覆盖的能力

| 场景 | 能力 | 信息源 |
|------|------|--------|
| 编程学习路线、项目教程 | 按阶段推荐项目，给时间预估 | [codefather.cn](https://www.codefather.cn) |
| 求职 / 简历 / 面试 | 简历写法指导，offer 选择建议 | [mianshiya.com](https://mianshiya.com) / [laoyujianli.com](https://laoyujianli.com) |
| AI 编程 / AI 工具 | AI 编程实战指导，工具推荐 | [ai.codefather.cn](https://ai.codefather.cn) |
| 技术选型 / 方向判断 | 以市场需求为锚点的技术判断 | 联网搜索 |
| 创业 / 自媒体经验 | 基于真实经历的方法论 | 内置知识 |
| 开源 / GitHub 运营 | 涨星涨粉技巧 | [github.com/liyupi](https://github.com/liyupi) |

## 蒸馏过程

这个 Skill 不是拍脑袋写的，而是经过系统化的蒸馏流程：

1. **素材收集** —— 整理了 20+ 篇原创文章、13 条真实咨询对话、3 篇视频文案、1 份内部工作文档
2. **分类归档** —— 按 6 个维度（经历、产品、观点、答疑风格、他人评价、工作方法）结构化
3. **人物分析** —— 生成完整的人物分析报告，提炼心智模型和表达特征
4. **深度追问** —— 12 个追问挖掘观点边界、决策失误、说做不一致、绝对不做的事
5. **Skill 编写** —— 将提炼结果写入 AgentSkills 标准格式
6. **自测验证** —— 用 3 个典型问题模拟回答，对比真实样本评估相似度

## 局限性

- 基于截至 2026 年 4 月的素材，最新动态可能未覆盖
- 技术细节问题需要联网搜索补充
- 无法还原视频中的表情、语调和肢体语言
- 涉及未公开的私人或商业信息时会如实说明

## 持续更新

向 `references/` 目录补充新素材即可迭代：

- 新的文章 / 视频文案 → 更新 `voice.md`
- 新的咨询对话 → 更新 `voice.md` 中的样本
- 新的产品 / 项目 → 更新 `knowledge-sources.md`
- 新的追问回答 → 更新 `identity.md`

## 制作你自己的 Skill

想把自己也蒸馏成 Skill？参考我的流程：

1. 收集你的素材（文章、聊天记录、视频文案、工作文档）
2. 让 AI 分析你的表达风格和思维模式
3. 让 AI 追问你 10-15 个深度问题，挖掘观点边界
4. 用 [Agent Skills 标准](https://agentskills.io) 打包成 Skill

也推荐 [colleague-skill](https://github.com/titanwings/colleague-skill) 项目，可以自动化完成蒸馏过程。

## License

MIT License © [程序员鱼皮](https://github.com/liyupi)
