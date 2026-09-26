# Keiry Product Article

一套面向 AI 产品体验与行业分析文章的 Codex Skill。

它覆盖选题判断、事实与竞品核查、个人体验取样、文章结构、自然中文改稿、配图规划，以及根据人工终稿持续校准个人写作习惯的完整流程。

## 为什么做这个 Skill

很多 AI 产品文章的问题并不在文笔，而在写作顺序。材料还没核实，结构已经列好；产品没有亲自体验，结论却先写出来；所谓去 AI 化，只是在段落里随机加入“其实”和“说起来”。

这个 Skill 把顺序倒过来。先确认事实、体验与未知项，再决定文章能写到哪里。成稿以后，配图承担证据或叙事作用。作者完成最终人工修改后，Skill 继续对照前后版本，把稳定偏好沉淀下来。

## 核心工作流

1. 明确产品、目标读者、发布渠道和真正要讨论的问题。
2. 收集官方事实、竞品路径、产品页面与亲身体验。
3. 区分亲自验证、主观体感、官方声明、外部证据和未知项。
4. 将体验还原为进入、操作、反馈、等待、结果和下一步的时间线。
5. 从一个真实体验矛盾中提炼文章判断，再决定结构。
6. 用户明确要求后才生成全文，并完成自然中文改稿。
7. 配图前先确认策略，让官方截图负责举证，概念图负责表达体验。
8. 对照人工终稿，区分稳定偏好、单篇选择和需要纠正的表达。

## 适用场景

- AI 产品体验文章
- 产品机制与交互流程分析
- AI 行业观察与竞品比较
- 公众号、人人都是产品经理等中文长文
- 已有草稿的去 AI 化修改
- 根据人工终稿持续学习作者风格

它不适合在没有亲身体验或可靠材料时，直接拼接一篇看似完整的行业结论。

## 目录结构

```text
keiry-product-article/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── drafting-and-revision.md
    ├── keiry-style.md
    ├── research-and-evidence.md
    └── visuals-and-learning.md
```

- `SKILL.md` 定义触发条件、完整流程和不可省略的边界。
- `research-and-evidence.md` 负责事实、竞品和体验素材。
- `drafting-and-revision.md` 负责结构、成稿和去 AI 化修改。
- `visuals-and-learning.md` 负责配图与人工终稿学习。
- `keiry-style.md` 保存可继续校准的个人写作偏好。

## 安装

把仓库克隆到 Codex 的 Skills 目录。

```bash
git clone https://github.com/YOUR_USERNAME/keiry-product-article.git ~/.codex/skills/keiry-product-article
```

如果已经下载到本地，也可以复制整个目录。

```bash
cp -R ./keiry-product-article ~/.codex/skills/keiry-product-article
```

Skill 目录需要包含一个 `SKILL.md`，详细规则可以放入 `references/`。这是 OpenAI 官方文档建议的基本组织方式。

## 使用

在 Codex 中直接调用：

```text
使用 $keiry-product-article，帮我研究并写一篇关于某款 AI 产品的体验文章。
```

也可以从工作流中的任意阶段开始：

```text
使用 $keiry-product-article，先整理这款产品的事实、竞品和体验素材，不要开始写全文。
```

```text
使用 $keiry-product-article，对照我的人工终稿，分析改动并更新写作偏好。
```

## 更新

如果 Skill 是通过 Git 克隆安装的，可以在本地拉取新版本。

```bash
git -C ~/.codex/skills/keiry-product-article pull
```

`references/keiry-style.md` 可能包含本地积累的个人偏好。更新前请先检查本地是否有未提交修改，避免被远端版本覆盖。

## 设计原则

- 材料不足时继续研究、追问或缩小文章，不用重复解释填字数。
- 主观体感不能冒充性能数据。
- 官方声明不能改写成亲测结果。
- 未验证能力明确保留为未知。
- 去 AI 化依靠真实观察和自然节奏，不依靠口头词堆砌。
- 学习作者风格时，不把事实错误、病句或偶然表达固化成规则。
