# 更新日志 / Changelog

所有版本均同步回技能目录 `Time AI · Krea 2 Anime Prompt Director`。

---

## Site — 2026-10-20（案例画廊 / case gallery）

**落地页新增 24 个真实案例画廊**（网页更新，非技能版本变更）

- 新增 **24 组真实案例**：原始输入 + skill 返回的完整 POSITIVE 提示词 + Krea 2 成图
- 画廊位于 Hero 正下方，成为页面核心：3 列卡片（移动端 1 列）、滚动带横向预览、点击开灯箱
- 移除了 Hero 的「输入 → 输出」终端演示，以及原来的 6 组 tab 示例区 —— 它们与 24 个真实案例重复，
  留着反而分散注意力；页面因此从 88KB 降到 64KB，导航也更短
- 灯箱内含大图、双语标题、作品名、中文画面摘要、完整输入与输出，输出可一键复制
- 支持 `←` `→` 翻页、`Esc` 关闭，以及 `#case-7` 这样的深链接直接分享单个案例
- 图片按用途分三档压缩：1600px 大图（灯箱）、760px 缩略（网格）、440px 迷你（滚动带）
- 卡片 hover 边框光晕取自每张图自身的主色
- **默认排序按用户输入的词数从少到多**（中文按字、英文按词），输入越短越靠前；
  卡片与灯箱都标出该案例的输入长度，翻页顺序跟随显示顺序，`#case-N` 深链仍指向固定编号

**24-case gallery**

- 24 real cases: the original one-line input, the full POSITIVE prompt the skill returned, and the Krea 2 render
- The gallery sits right under the hero as the page's centrepiece: 3-column cards, a marquee strip, and a lightbox on click
- Removed the hero's "input → output" terminal mock-up and the old six-tab examples section — both duplicated
  what the 24 real cases already show; the page drops from 88KB to 64KB and the nav gets shorter
- Lightbox shows the full image, bilingual title, work name, a Chinese summary, and copyable input and output
- Arrow-key paging, Esc to close, and shareable deep links such as `#case-7`
- Three image sizes: 1600px for the lightbox, 760px for the grid, 440px for the strip
- Each card's hover glow is sampled from its own image
- **Default order is by input length, shortest first** (CJK per character, everything else per word);
  the input length is shown on each card and in the lightbox, paging follows the on-screen order, and `#case-N` still points at a fixed case

---

## Site — 2026-10-20（教程板块 / tutorial section）

**新增「视频教程」板块，放在能力之后**

- 收录 B 站视频《Krea 2 完全体（下）》里与本 skill 直接相关的两段，各自带时间戳，点开直接从该处播放
- `09:38` 动漫角色参考工具 —— 页面上 24 个案例的选角都出自这一步，先定角色，再把名字交给 skill
- `12:08` 这个 skill 的安装与使用 —— 从放进 skills 目录到写出第一句输入、拿回完整提示词
- 版面为「左封面 + 右两条章节」：封面即视频封面（1280px / 640px 两档 WebP，共 ~287KB），
  悬停轻抬 + 播放键放大；≤860px 收成单列，封面在上、两条章节在下
- 板块底色按新的交替顺序重排：案例（白）→ 能力（浅底）→ 教程（白）→ 为什么（浅底）→ …，导航新增「教程」

**Video walkthrough**

- Adds a walkthrough section right after the features, collecting the two chapters of the Bilibili video
  that are relevant here, each linked at its exact timestamp
- `09:38` the anime character reference tool every case was cast with; `12:08` installing and using this skill
- Layout is a cover on the left and two chapter rows on the right; the cover ships as 1280px and 640px WebP
  (~287KB together) and lifts slightly on hover; below 860px it stacks into one column
- Section band colours re-alternated for the new order, and "Tutorial" was added to the nav

---

## Site — 2026-10-20（视觉改版 / visual refresh）

**整站换成暖白底、图片优先的简洁风格**

- 底色从纯白改为暖白 `#fcfcfb`，叠一层极淡纸纹；区块之间用统一的 84px 竖向节奏切分，白底区与浅底区交替
- 画廊卡片去掉压在图片左上角的编号胶囊，编号下移到标题下方的灰字行 —— 图片不再被任何控件遮挡
- 能力区 8 张卡片补一张「去安装」收尾卡，3×3 网格不再留空位
- 更新日志默认只展开当前版本，1.5.0 及更早折叠进「更早的 6 个版本」，长页面一下子短了一半
- 工作流步骤收窄到 760px 居中，长文不再贴左阅读
- 标题渐变由紫→青改为靛→天蓝，去掉荧光感；按钮、导航、卡片统一 14px 圆角与两档柔和阴影
- 修好目录树的换行问题（此前所有行被压成一整行）
- 移动端（390px）重新校对：标题不断词、语言开关留在导航内、卡片单列
- 板块顺序重排：案例 → 能力 → 为什么 → 画风 → 安装 → 边界 → 工作流 → 更新日志，
  导航同步调整；「为什么」紧跟能力之后，工作流与日志沉到页尾
- 画廊卡片上的编号整个去掉，标题下的说明只留「作品 · 输入 N 词」；灯箱顶部改成「序号 / 24」的位置指示，
  翻页时连续，不再显示与排序无关的固定编号
- 图下那行小字（「作品 · 输入 N 词」）也一并去掉，卡片只剩一张图和一行标题；灯箱顶部的词数同去，
  只留「序号 / 24」——原始输入就在灯箱里，不缺这一处
- 首三张固定为千寻 × 龙猫、海绵宝宝 × 派大星、卡尔 · 气球屋，其余仍按输入词数从少到多
- 示例统一换成「海绵宝宝和派大星」（即画廊里第 11 个案例的真实会话）：
  `references/examples.md` 的第一个示例、两份 README 的「使用 / 输出」、落地页安装区的示例命令三处同步

**A calmer, image-first visual refresh**

- Background moves from pure white to a warm off-white `#fcfcfb` with a barely-there paper grain;
  sections now alternate between plain and lightly tinted bands on a consistent 84px vertical rhythm
- Gallery cards lose the number pill that sat on top of each image, so nothing covers the artwork
- The eight capability cards gain a ninth "go install" card, so the 3×3 grid no longer ends on an orphan
- The changelog opens the current version only; 1.5.0 and older fold into "six earlier versions",
  cutting the page length roughly in half
- Workflow steps narrow to a centred 760px column instead of hugging the left edge
- The headline gradient shifts from violet→teal to indigo→sky, losing the neon feel; buttons, nav and cards
  share a 14px radius and two soft shadow tiers
- Fixed the repository tree collapsing onto a single line
- Re-checked at 390px: no broken headline wraps, the language switch stays inside the nav, cards stack in one column
- Section order reshuffled to cases → features → why → styles → install → limits → workflow → changelog, with the nav
  following along: "why" now sits right after the features, and the workflow and changelog sink to the end of the page
- Card indices are gone entirely; the caption is just "work · N words in", and the lightbox header becomes a
  continuous "12 / 24" position indicator instead of a fixed case number that ignored the on-screen order
- That caption line goes too: a card is now one image and one title, and the lightbox header keeps only "12 / 24"
  — the original input already sits inside the lightbox, so the word count was pure repetition
- The first three cards are pinned: Chihiro & Totoro, SpongeBob & Patrick, Carl and the balloon house
- Doc examples now use SpongeBob and Patrick Star (the real session behind gallery case 11): the first example in
  `references/examples.md`, the "Use / Output" blocks in both READMEs, and the sample command in the install section

---

## 1.6.0 — 2026-10-19

**动作要让人记住，多人要有交流**

起因：出图里角色动作很"呆"——并排摆姿势、动作和环境没关系、多人之间没有互动。

- 新增 `references/action-direction.md`：动作与角色互动的完整方法
- 动作必须有明确意图、重心、发力方向，并在环境里留下可见后果；只写"动态姿势""战斗姿势"不算
- 只定格一个瞬间：预备、决定性的接触、或跟随动作。不把连续动作全塞进一帧
- 场景要参与动作：墙、树枝、栏杆、台阶、水流、阵风成为动作的支点或阻力，并给出接触点的反应
- 多人画面要有可读取的交流：谁先动手、对方如何回应、视线交汇在哪、接触点在哪、身体与空间各自发生了什么改变
- 新增两组中英案例：**林克暴雨山道跃越**（单人动作与环境耦合）、**悟空与比克对练**（双人攻防与反应）
- 参考了 Krea 对动势、重量感与焦点瞬间的说明，以及 Disney Animation 关于预备动作、跟随动作、清晰调度与角色反应的原则

**Memorable action, real interaction**

- Added `references/action-direction.md`: a full method for action and character interaction
- Every action needs a clear intention, weight shift and direction of force, with a visible consequence in the surroundings — "dynamic pose" is not enough
- One instant only: anticipation, the decisive contact, or follow-through — never a narrated sequence in a single frame
- The setting participates: walls, branches, railings, stairs, water and gusts enable, interrupt or redirect the movement, with a reaction at the contact point
- Multi-character images stage a readable exchange: who initiates, who responds, where eyelines meet, where contact happens, and what changes across bodies and space
- Two new EN/CN examples: **Link leaping a collapsed mountain path in a storm**, and **Goku sparring with Piccolo**
- Informed by Krea's notes on motion, weight and focal beats, and Disney Animation's principles of anticipation, follow-through, clear staging and character reaction

---

## 1.5.0 — 2026-10-18

**扩写输出长度**

- 输出长度目标提高：角色入景约 100–180 词 → **150–350 词**；纯背景约 80–160 词 → **120–300 词**
- 所有案例的英文提示词与中文对照同步扩写，增补角色姿态与服装细节、场景空间层次、光线氛围与画风
- 扩写以增加可视化信息为准，不用重复形容词凑长度

> 说明：这是**目标区间**，不是对每条输出精确 +50% 的承诺。案例扩写幅度约为 50% 或更多，但实际生成的长度仍取决于具体请求。

**Longer output**

- Raised output length targets: character-in-scene ~100–180 → **150–350 words**; background-only ~80–160 → **120–300 words**
- Expanded every example's English prompt and Chinese translation with pose/costume detail, spatial layering, light, atmosphere and rendering
- Expansion adds visual information, not repeated adjectives

> Note: these are **target ranges**, not a guarantee of exactly +50% per output.

---

## 1.4.0 — 2026-10-18

**把场景名还原成可画的画面**

- 新增"把场景名称转成可画描述"的规则：先说明物理类型与布局，再写出标志性建筑、物件、材质、空间关系、规模与氛围
- 场景专名只能作为辅助锚点，不能代替画面描述 —— AI 并不理解"天下第一武道会"这个名字
- 改写孙悟空案例：方形浅色石擂台、红色界线、环绕的阶梯观众席、瓦顶入口楼阁、赛事旗帜

**Names become drawable scenes**

- Added a rule for translating scene names into drawable descriptions: state the physical type and layout first, then visible identifiers, materials, spatial relations, scale and atmosphere
- A proper name is only a supporting anchor and never replaces the visual description
- Rewrote the Goku example: pale square stone ring, red boundary line, stepped stands, tiled entrance pavilion, tournament banners

---

## 1.3.0 — 2026-10-18

**未指定环境时自动补全经典场景**

- 只要用户没指定环境就自动补全 —— 不只是"只输入角色名"，给了动作、风格或情绪但没给地点同样适用
- 覆盖动漫、漫画与游戏角色
- 同一角色在对话中再次出现时，场景和动作都必须换（除非用户明确要求复现或续写）
- 新增《塞尔达传说：旷野之息》林克未指定环境的中英文案例

**Automatic canon setting when no environment is given**

- Fills in a classic canon setting whenever the environment is unspecified — not only for a bare character name, but also for requests that give an action, style or mood without a location
- Applies to anime, manga and game characters
- When the same character recurs in a conversation, both the setting and the action must change (unless a repeat or continuation is requested)
- Added a *Breath of the Wild* Link example with no environment specified

---

## 1.2.0 — 2026-10-18

**角色外观跟随剧情阶段**

- 先判定剧情阶段、地点、身份或变身状态，再写外貌和服装；不再把默认造型套到所有场景
- 禁止跨阶段混搭特征（例如不能把某一形态的头发和另一形态的服装拼在一起）
- 新增中英文对照案例：悟空那美克星超级赛亚人形态／地球普通形态；千寻汤屋工作装／非工作装

**Appearance follows the story moment**

- Resolve the story moment, location, role or transformation state before describing appearance and costume
- Never mix traits across story moments
- Added paired EN/CN examples: Goku Super Saiyan on Namek vs. ordinary on Earth; Chihiro at work in the bathhouse vs. off duty

---

## 1.1.0 — 2026-10-18

**强化角色具体特征**

- 强化角色特征描述标准：优先写清发型、脸部特征、身形轮廓、标志性服装与配饰
- 根据镜头远近取舍细节，避免特征被构图或特效遮住
- 角色案例的英文提示词与中文对照同步改写；纯场景案例保留原样

**Stronger character identity cues**

- Strengthened the character-identity standard: hair, face and markings, silhouette, signature costume and accessories come first
- Detail is selected by framing so identity cues are not hidden by composition or effects
- Character examples rewritten in both languages; environment-only examples left unchanged

---

## 1.0.0

**首个版本**

- 整合 Krea 官方两篇动漫指南（《Anime Backgrounds with Krea 2》《Studio Anime Aesthetics with Krea 2》）与社区项目 Krea2 Character Catalog 的证据化流程
- 定义 `POSITIVE` + `中文对照` 的双段输出格式
- 建立风格选择矩阵与场景设计语言库

**First release**

- Synthesizes Krea's two official anime guides and an evidence-aware workflow for the community Krea2 Character Catalog
- Defines the two-section output format: `POSITIVE` + Chinese translation
- Establishes the style-selection matrix and the scene-design language bank
