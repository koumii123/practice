# practice

专四口语思辨陪练 Skill：AI 出英文思辨话题和正反参考句型，你口头作答后获得逐字转写、1 版口语优化和简短点评，支持同话题深度追问与重答循环。

## 项目解决什么问题

备考专四口语（TEM-4）需要开口练思辨表达，但自己练往往面临三个问题：不知道说什么、说不出来中式英语、说错了没人指出来。

本项目（practice Skill）解决这个问题：它像一个回合制口语陪练，AI 先给英文思辨话题和正反参考句型帮你开口，再对你的口头作答逐字转写、改写优化并点评，明确指出中式英语问题，帮你越说越地道。

## 主要功能

- **回合制训练**：出题 → 口头作答 → 反馈 → 二选一，一轮只推进一个环节。
- **每轮 Topic + 参考句型**：AI 出英文思辨话题（TEM-4 难度、可正反辩论），配 2 句纯英文参考句型（1 句肯定立场、1 句否定立场），供你模仿开口；也可指定话题。
- **反馈三件套**：
  - ①【我的原句】原样转写你的口述，一字不改；
  - ②【优化句】只给 1 版适配专四口语的改写，专治中式英语（中文直译、中式搭配、逻辑断层、母语负迁移），拒绝浅层换词，核心改动加粗；
  - ③【简短点评】指出本次中式英语问题，并说明逻辑、句式与用词地道度。
- **继续 / 重新回答**：输入【继续】对当前话题深度追问开启新一轮；输入【重新回答】不换话题重答，循环到【继续】为止。
- 纯模型能力实现，无脚本、无外部工具、无 API。

## 安装方法

把 `practice/` 整个目录放入支持 Agent Skills（SKILL.md）的智能体环境的 skills 目录即可（如 Doubao、OpenAI Agents、Codex），无需其他配置。

## 使用方法

对 AI 说出启用口令「开始练口语」即启动训练，也可直接指定话题，如「开始练口语，练 AI 进课堂这个话题」。

1. AI 输出 **Topic** 和 2 句参考句型（纯英文，一正一反）；
2. 你用英文口头作答（把口头说的话打出来）；
3. AI 给出反馈三件套；
4. 随后二选一：
   - 输入 **继续**：AI 对当前话题深度追问，开启新一轮；
   - 输入 **重新回答**：不换新话题，你再答一遍，循环到输入"继续"为止。

## 输入输出示例

**输入**（未指定话题时 AI 自动选题）

> 开始练口语

**AI 输出**

> **Topic**: Is social media making us more connected or more lonely?
>
> **参考句型**：
> - 肯定：I believe social media brings people closer, because it lets us stay in touch with friends and family no matter how far apart we are.
> - 否定：I don't think social media makes us truly connected, since likes and comments can never replace real face-to-face conversation.

**输入**（你的口头作答）

> I think social media can make people more lonely. Because people just look phone, not talk each other. Very bad.

**AI 输出**

> ①【我的原句】
> I think social media can make people more lonely. Because people just look phone, not talk each other. Very bad.
>
> ②【优化句】
> I think social media **can make people feel lonelier**, because people **just keep staring at their phones** instead of **talking to each other**, **and that weakens real relationships**.
>
> ③【简短点评】
> 主要问题是中文直译："look phone" 是"看手机"的逐词对译，应说 look at / keep staring at 或 use；"not talk each other" 缺介词 with，整句缺主语且与上句缺因果连接。结尾 "Very bad" 是无主语碎片句，也没说清什么糟糕，逻辑断层。句式碎片化、用词偏简单，地道度中等。
>
> 【继续】/【重新回答】

**输入**

> 继续

**AI 输出**：基于当前话题的深度追问 + 2 句新参考句型，进入新一轮。

## 不支持

网页抓取、PDF、图形界面。
