# Time AI · Krea 2 Anime Prompt Director

![Krea 2](https://img.shields.io/badge/Krea-2-7C5CFF?style=flat-square)
![Version](https://img.shields.io/badge/version-1.6.0-111827?style=flat-square)
![Format](https://img.shields.io/badge/format-Agent%20Skill-0EA5E9?style=flat-square)
![License](https://img.shields.io/badge/license-MIT-22C55E?style=flat-square)

**[English](README.md) · 简体中文 · [在线页面 →](https://shiguanggougouo.github.io/krea2-anime-prompt-director/) · [视频教程（12:08 安装与使用）→](https://www.bilibili.com/video/BV1neJf6XEdA/?t=728&vd_source=a7826b5703f20f1ca10cf2ddd4fba044)**

一个可复用的 Agent 技能：把一句中文或英文的简短想法，扩写成**完整、可直接投喂 Krea 2 的动漫提示词**，并附一份忠实的中文对照。

它做五件通用「提示词优化器」做不到的事：

1. **把角色身份落在可见证据上** —— 发型形状与走向、眼睛与标志性纹样、轮廓、标志性服装层次、颜色与材质、随身道具，并按照你要求的镜头远近做取舍。
2. **还原地点，而不是报出名字** —— 「天下第一武道会」会被写成高起的浅色石质擂台、红色边界线、环绕的阶梯看台、刷漆的立柱、旗帜和带瓦顶的入口楼阁。
3. **自动补全没指定的环境** —— 只给一个角色名时，它会从该角色所属动漫、漫画或游戏的原著里，挑一个极具故事感的经典场景，并把环境具体画出来。
4. **重复请求不撞车** —— 同一角色在一次对话里再次出现时，场景与剧情节点、动作都会换新。
5. **动作和互动真的有戏** —— 只定格一个决定性瞬间：意图、重心与支撑、发力方向，以及环境里看得见的后果。多人画面则是可读取的交流：谁先动手、谁回应、视线与接触点落在哪里。不会写「动态姿势」「战斗姿势」，也不会让几个角色并排各摆各的。

依据来自 Krea 官方的两篇动漫指南，加上一套对社区 Krea2 Character Catalog 保持证据意识的取用流程。

▶ **视频教程（B 站）**：[这个 skill 的安装与使用 —— 12:08](https://www.bilibili.com/video/BV1neJf6XEdA/?t=728&vd_source=a7826b5703f20f1ca10cf2ddd4fba044) · [24 个案例选角用的动漫角色参考工具 —— 09:38](https://www.bilibili.com/video/BV1neJf6XEdA/?t=578&vd_source=a7826b5703f20f1ca10cf2ddd4fba044)

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
用 krea2-anime-prompt-director 扩写：海绵宝宝和派大星
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
Anime-style illustration of SpongeBob SquarePants and Patrick Star from SpongeBob SquarePants,
jellyfishing together in Jellyfish Fields. SpongeBob, a bright yellow square sponge with large blue
eyes, wears his white shirt, red tie, brown square pants, knee-high socks, and shiny black shoes.
He leans forward with a jellyfishing net raised, delighted as a glowing pink jellyfish drifts just
within reach...

中文对照：
《海绵宝宝》的海绵宝宝和派大星在水母田里一起捕捉水母。海绵宝宝是一块亮黄色的方形海绵，有一双
大大的蓝眼睛，穿着白衬衫、红领带、棕色方裤、及膝袜和擦得发亮的黑皮鞋。他兴奋地向前倾身，举起
捕网，正要接住一只漂到网边的粉色发光水母……
```

---

## 24 组真实案例

每一张都是一次真实生成。图下面那一行，就是当时输入的话——没有多加任何东西。

| <a href="docs/gallery/01.webp"><img src="docs/gallery/thumbs/01.webp" width="100%" alt="千与千寻 · 千寻 × 龙猫 · 雨后林间"></a><br>**千与千寻 · 千寻 × 龙猫 · 雨后林间**<br><sub>输入：千与千寻动漫里的千寻和龙猫.</sub> | <a href="docs/gallery/11.webp"><img src="docs/gallery/thumbs/11.webp" width="100%" alt="海绵宝宝 · 海绵宝宝 × 派大星 · 水母田"></a><br>**海绵宝宝 · 海绵宝宝 × 派大星 · 水母田**<br><sub>输入：海绵宝宝和派大星</sub> | <a href="docs/gallery/12.webp"><img src="docs/gallery/thumbs/12.webp" width="100%" alt="飞屋环游记 · 卡尔 · 气球屋门廊"></a><br>**飞屋环游记 · 卡尔 · 气球屋门廊**<br><sub>输入：Carl Fredricksen from Up.</sub> |
| <a href="docs/gallery/09.webp"><img src="docs/gallery/thumbs/09.webp" width="100%" alt="犬夜叉 · 犬夜叉 × 戈薇 · 御神木下"></a><br>**犬夜叉 · 犬夜叉 × 戈薇 · 御神木下**<br><sub>输入：犬夜叉和戈薇</sub> | <a href="docs/gallery/19.webp"><img src="docs/gallery/thumbs/19.webp" width="100%" alt="赛车总动员 · 闪电麦昆 · 最后一个弯道"></a><br>**赛车总动员 · 闪电麦昆 · 最后一个弯道**<br><sub>输入：lightning mcqueen from cars (movie…</sub> | <a href="docs/gallery/17.webp"><img src="docs/gallery/thumbs/17.webp" width="100%" alt="千与千寻 · 千寻 · 海上列车"></a><br>**千与千寻 · 千寻 · 海上列车**<br><sub>输入：千与千寻里的千寻，火车</sub> |
| <a href="docs/gallery/15.webp"><img src="docs/gallery/thumbs/15.webp" width="100%" alt="猫和老鼠 · 汤姆 × 杰瑞 · 厨房追逐"></a><br>**猫和老鼠 · 汤姆 × 杰瑞 · 厨房追逐**<br><sub>输入：猫和老鼠动漫里的猫和老鼠</sub> | <a href="docs/gallery/18.webp"><img src="docs/gallery/thumbs/18.webp" width="100%" alt="无敌破坏王 · 拉尔夫 × 云妮洛普 · 冲线击掌"></a><br>**无敌破坏王 · 拉尔夫 × 云妮洛普 · 冲线击掌**<br><sub>输入：无敌破坏王里的男主和女主</sub> | <a href="docs/gallery/13.webp"><img src="docs/gallery/thumbs/13.webp" width="100%" alt="机器人总动员 · 瓦力 × 伊娃 · 废墟递出植物"></a><br>**机器人总动员 · 瓦力 × 伊娃 · 废墟递出植物**<br><sub>输入：机器人总动员里的男主和女主</sub> |
| <a href="docs/gallery/24.webp"><img src="docs/gallery/thumbs/24.webp" width="100%" alt="龙珠 · 悟空救下 18 号 · 碎石战场"></a><br>**龙珠 · 悟空救下 18 号 · 碎石战场**<br><sub>输入：龙珠里孙悟空救下了18号，抱着她</sub> | <a href="docs/gallery/23.webp"><img src="docs/gallery/thumbs/23.webp" width="100%" alt="宝可梦 日月 · 莉莉艾 · 以太乐园温室"></a><br>**宝可梦 日月 · 莉莉艾 · 以太乐园温室**<br><sub>输入：lillie (pokemon), pokemon, 1girl, …</sub> | <a href="docs/gallery/10.webp"><img src="docs/gallery/thumbs/10.webp" width="100%" alt="飞天小女警 · 泡泡 · 救下失控巴士"></a><br>**飞天小女警 · 泡泡 · 救下失控巴士**<br><sub>输入：blossom (ppg) from powerpuff girls…</sub> |
| <a href="docs/gallery/02.webp"><img src="docs/gallery/thumbs/02.webp" width="100%" alt="宝可梦 · 喷火龙 vs 皮卡丘 · 雨夜决赛"></a><br>**宝可梦 · 喷火龙 vs 皮卡丘 · 雨夜决赛**<br><sub>输入：A non-human character. Appearance:…</sub> | <a href="docs/gallery/07.webp"><img src="docs/gallery/thumbs/07.webp" width="100%" alt="游戏王 · 海马濑人 · 战斗都市屋顶"></a><br>**游戏王 · 海马濑人 · 战斗都市屋顶**<br><sub>输入：kaiba seto from yu-gi-oh!. A male …</sub> | <a href="docs/gallery/04.webp"><img src="docs/gallery/thumbs/04.webp" width="100%" alt="超级马力欧 · 罗莎琳娜 · 彗星天文台"></a><br>**超级马力欧 · 罗莎琳娜 · 彗星天文台**<br><sub>输入：rosalina from mario (series). A fe…</sub> |
| <a href="docs/gallery/08.webp"><img src="docs/gallery/thumbs/08.webp" width="100%" alt="名侦探柯南 · 江户川柯南 · 深夜侦探所"></a><br>**名侦探柯南 · 江户川柯南 · 深夜侦探所**<br><sub>输入：edogawa conan from meitantei conan…</sub> | <a href="docs/gallery/20.webp"><img src="docs/gallery/thumbs/20.webp" width="100%" alt="樱花大战 · 真宫寺樱 · 帝国剧场庭院"></a><br>**樱花大战 · 真宫寺樱 · 帝国剧场庭院**<br><sub>输入：shinguuji sakura from sakura taise…</sub> | <a href="docs/gallery/06.webp"><img src="docs/gallery/thumbs/06.webp" width="100%" alt="女神异闻录 5 · 芳泽霞 · 殿堂走廊"></a><br>**女神异闻录 5 · 芳泽霞 · 殿堂走廊**<br><sub>输入：yoshizawa kasumi from persona. A f…</sub> |
| <a href="docs/gallery/03.webp"><img src="docs/gallery/thumbs/03.webp" width="100%" alt="英雄联盟 · 阿狸 · 艾欧尼亚月夜"></a><br>**英雄联盟 · 阿狸 · 艾欧尼亚月夜**<br><sub>输入：ahri (league of legends) from leag…</sub> | <a href="docs/gallery/21.webp"><img src="docs/gallery/thumbs/21.webp" width="100%" alt="新世纪福音战士 · 明日香 · 二号机插入栓"></a><br>**新世纪福音战士 · 明日香 · 二号机插入栓**<br><sub>输入：souryuu asuka langley from neon ge…</sub> | <a href="docs/gallery/22.webp"><img src="docs/gallery/thumbs/22.webp" width="100%" alt="VOCALOID · 初音未来 · 全息舞台"></a><br>**VOCALOID · 初音未来 · 全息舞台**<br><sub>输入：初音未来，Vocaloid, 1girl, 水蓝色的眼睛, 蓝眼睛,…</sub> |
| <a href="docs/gallery/05.webp"><img src="docs/gallery/thumbs/05.webp" width="100%" alt="美少女战士 · 水手火星 · 绯川神社黄昏"></a><br>**美少女战士 · 水手火星 · 绯川神社黄昏**<br><sub>输入：sailor mars from bishoujo senshi s…</sub> | <a href="docs/gallery/14.webp"><img src="docs/gallery/thumbs/14.webp" width="100%" alt="最终幻想 VII · 蒂法 · 第七天堂打烊后"></a><br>**最终幻想 VII · 蒂法 · 第七天堂打烊后**<br><sub>输入：tifa lockhart from final fantasy. …</sub> | <a href="docs/gallery/16.webp"><img src="docs/gallery/thumbs/16.webp" width="100%" alt="尼尔：机械纪元 · 2B · 雨中废墟"></a><br>**尼尔：机械纪元 · 2B · 雨中废墟**<br><sub>输入：machine (nier) from nier:automata.…</sub> |

高清大图在 [`docs/gallery/`](docs/gallery/)（1600px / 760px / 440px 三档）·
在线逐张查看：[在线页面 · 案例画廊](https://shiguanggougouo.github.io/krea2-anime-prompt-director/#gallery)

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
