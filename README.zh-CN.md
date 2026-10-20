# Time AI · Krea 2 Anime Prompt Director

![Krea 2](https://img.shields.io/badge/Krea-2-7C5CFF?style=flat-square)
![Version](https://img.shields.io/badge/version-1.6.0-111827?style=flat-square)
![Format](https://img.shields.io/badge/format-Agent%20Skill-0EA5E9?style=flat-square)
![License](https://img.shields.io/badge/license-MIT-22C55E?style=flat-square)

**[English](README.md) · 简体中文 · [在线页面 →](https://shiguanggougouo.github.io/krea2-anime-prompt-director/)**

一个可复用的 Agent 技能：把一句中文或英文的简短想法，扩写成**完整、可直接投喂 Krea 2 的动漫提示词**，并附一份忠实的中文对照。

它做五件通用「提示词优化器」做不到的事：

1. **把角色身份落在可见证据上** —— 发型形状与走向、眼睛与标志性纹样、轮廓、标志性服装层次、颜色与材质、随身道具，并按照你要求的镜头远近做取舍。
2. **还原地点，而不是报出名字** —— 「天下第一武道会」会被写成高起的浅色石质擂台、红色边界线、环绕的阶梯看台、刷漆的立柱、旗帜和带瓦顶的入口楼阁。
3. **自动补全没指定的环境** —— 只给一个角色名时，它会从该角色所属动漫、漫画或游戏的原著里，挑一个极具故事感的经典场景，并把环境具体画出来。
4. **重复请求不撞车** —— 同一角色在一次对话里再次出现时，场景与剧情节点、动作都会换新。
5. **动作和互动真的有戏** —— 只定格一个决定性瞬间：意图、重心与支撑、发力方向，以及环境里看得见的后果。多人画面则是可读取的交流：谁先动手、谁回应、视线与接触点落在哪里。不会写「动态姿势」「战斗姿势」，也不会让几个角色并排各摆各的。

依据来自 Krea 官方的两篇动漫指南，加上一套对社区 Krea2 Character Catalog 保持证据意识的取用流程。

---

## 快速开始

### 安装

把整个文件夹放进你的 agent 读取的 skills 目录。`SKILL.md` 与 `references/` 必须放在一起 —— 参考文件是按需加载的，拆开就失效。

```bash
# Codex / 仓库级
git clone https://github.com/shiguanggougouo/krea2-anime-prompt-director.git .agents/skills/krea2-anime-prompt-director

# WorkBuddy / Claude 风格用户级
git clone https://github.com/shiguanggougouo/krea2-anime-prompt-director.git ~/.workbuddy/skills/krea2-anime-prompt-director
```

### 使用

说人话就行，剩下的交给技能：

```
用 krea2-anime-prompt-director 扩写：旗木卡卡西
```

```
Use krea2-anime-prompt-director: Sailor Moon, classic moonlit scene
```

```
用 krea2-anime-prompt-director：京都动画风格，雨后的日本高中教室，不要人物
```

### 输出

只有两段，没有多余的东西，没有过程说明：

```
POSITIVE:
A cinematic 2D shonen-anime key illustration of Hatake Kakashi from Naruto, identifiable by his
unruly silver hair swept into sharp spikes, a Leaf forehead protector slanted over his left eye,
one relaxed visible eye, the black mask covering his nose and mouth, and the high collar and
segmented pockets of his green flak jacket over a dark undersuit. He sits sideways on the curved
ridge of a tiled rooftop in the Hidden Leaf Village, casually reading a small orange-covered
paperback...

中文对照：
一幅具有电影感的二维少年热血动漫关键插画，描绘《火影忍者》中的旗木卡卡西。他蓬松的银发向上分成
清晰尖束，木叶护额斜压在左眼上方，一只放松却警觉的眼睛露在外面，黑色面罩遮住鼻子和嘴……
```

---

## 和通用方案的区别

| 通用提示词助手 | 本技能 |
|---|---|
| 堆 Danbooru 标签加质量宏（`masterpiece`、`8k`、`best quality`） | 写连贯的自然语言散文 —— 只有你明确要标签列表时才用标签 |
| 背景只写「在室内」「户外」 | 挑一个原著场景，把建筑、材质、尺度、光线和天气写清楚 |
| 写「在天下第一武道会」，指望模型自己认识 | 把专有名词翻译成可画的物理布局与可识别特征 |
| 所有场景复用同一套默认造型 | 先判定角色的**剧情阶段版本** —— 篇章、地点、身份、变身状态 |
| 同一个角色永远是同一个姿势同一个地点 | 记录已用过的场景与动作组合，重复请求时两者都换 |
| 写「动态姿势」「战斗姿势」，几个人并排摆造型 | 一个可画的瞬间：肢体力学、发力方向、环境反应；多人则是有角色分工与回应的真实交流 |
| 声称「我查过 catalog 了」 | 只有真的翻过某条记录，才会说查过 |

---

## 更新日志

版本历史见 [CHANGELOG.md](CHANGELOG.md) —— 覆盖 1.0.0 到 1.6.0，每条都写清它修掉的到底是什么生成问题。

## 文件说明

| 文件 | 内容 |
|---|---|
| `SKILL.md` | 核心行为、工作流、强制输出格式 |
| `references/action-direction.md` | 动作与角色互动规范：决定性瞬间、肢体力学、环境反应、多人交流 |
| `references/style-language.md` | 画风选择矩阵、场景描述语料库、提示词骨架 |
| `references/examples.md` | 完整中英对照示例 —— 角色入景、动作、纯背景、变体选择 |
| `references/catalog-workflow.md` | 如何取用 Krea2 Character Catalog 而不过度声称可靠性 |
| `references/source-notes.md` | 来源链接、来源可推得结论、核实边界 |
| `docs/index.html` | 项目落地页（GitHub Pages 源，含中英文切换） |
| `docs/cases.js` | 24 个案例的数据：原始输入、返回的提示词、双语标题与摘要 |
| `docs/gallery/` | 24 张成图（1600px 大图、760px 缩略、440px 滚动带） |
| `CHANGELOG.md` | 从 1.0.0 到 1.6.0 的版本历史 |
| `README.md` | 英文版 README（默认） |

## 内置画风锚点

每条提示词一个主锚点，最多加一个有边界的偏置：

- 吉卜力美学 —— 手绘水彩质感、克制的自然色盘
- 新海诚 / CoMix Wave Films —— 高饱和天空、云缘光、都市光斑
- 京都动画 —— 温暖窗光、纤细线条、生活化细节
- Madhouse / 都市黑色 —— 冷蓝绿调、湿沥青、钠黄点缀
- 1990s Sunrise / 经典 OVA 机甲 —— 硬边赛璐璐、工业感背景
- 少女向 / 青年向语域
- 经典战斗少年漫赛璐璐动画

## 诚实的边界

- 本技能**不打包** Krea2 Character Catalog 数据集，也不声称会自动查询它。有可用的条目、导出文件或用户提供的文件时才用，没有就据实继续。
- Catalog 条目是**暂定性的**。匹配上是有用的证据，但既不等于原著事实，更不等于该角色一定存在于 Krea 2 的训练数据里。
- 只靠提示词文本无法保证跨图集的完美角色一致性。要这个效果，得用 Krea 2 的风格参考，或者 20–40 帧规模的 mood board。

## 来源

- [Anime Backgrounds with Krea 2](https://www.krea.ai/blog/anime-backgrounds-with-krea-2) —— Krea 官方
- [Studio Anime Aesthetics with Krea 2](https://www.krea.ai/blog/studio-anime-aesthetics-with-krea-2) —— Krea 官方
- [Krea2 Character Catalog](https://github.com/ukr8b3g-cmyk/Krea2-Character-Catalog) —— 社区项目
- [Agent Skills 格式](https://developers.openai.com/api/docs/guides/tools-skills) —— OpenAI

## License

MIT —— 见 [LICENSE](LICENSE)。
