---
name: ai-technology-article-image
description: 为 AI、科技、产品、商业和职场类微信公众号文章规划并生成统一风格的章节配图。先通过对话收集文章主题、账号定位、目标读者、正文结构和图片要求，再建立视觉母版、拆解逐图内容提示词并调用 ImageGen 生成。适用于公众号长文配图、系列文章组图和已有图片去 AI 味；不用于品牌 Logo 设计或要求精确还原的产品界面。
---

# AI Technology Article Image

为公众号文章生成一组内容对应准确、视觉风格统一、适合手机阅读的编辑插画。

图片需要帮助读者理解文章，不能只做气氛装饰。默认追求克制、清晰和人工设计感，避免常见的 AI 图片特征。

## 何时使用

用户提出以下需求时使用本 Skill。

- 给 AI、科技、产品、商业或职场类公众号文章生成配图
- 给文章的每个章节制作图片
- 根据大纲规划一组风格统一的插图
- 把已有 AI 图片改得更自然、更有编辑感
- 延续用户之前认可的公众号插画风格
- 为同一账号建立稳定的文章配图语言

如果用户只需要单张真人封面、品牌 Logo、产品图精修或精准 UI 还原，使用更适合该任务的能力。

## 第一阶段：收集必要信息

开始生成前，检查用户已经提供的信息。已有内容不要重复询问。

至少需要明确以下信息。

1. 文章主题或暂定标题
2. 公众号定位和主要读者
3. 完整正文、大纲或小标题
4. 需要几张图片以及放置位置
5. 图片比例和主要使用场景
6. 必须保留或明确避开的视觉元素
7. 是否有参考图、品牌色或历史配图

缺少关键信息时，优先一次询问三个问题以内。

推荐提问方式如下。

- 这篇文章的标题、核心观点和主要读者分别是什么？
- 请发我文章正文或小标题，并说明希望给哪些章节配图。
- 有没有需要沿用的颜色、参考图片，以及明确不想出现的元素？

如果用户已经提供完整文章，可以从正文推断主题、受众和章节关系，只补问会明显改变结果的信息。

## 第二阶段：确认视觉方向

根据用户输入，用一小段话总结视觉方案，包括主色、插画形式、人物与界面元素的处理方式、图片整体情绪以及明确排除的视觉特征。

用户没有指定风格时，默认使用本 Skill 的公众号编辑插画风格。

批量生成六张以上图片，且用户没有提供参考图时，可以先提供视觉方案并询问是否需要生成一张样图。用户要求直接生成时，不增加确认步骤。

用户已经给出认可的参考图时，直接沿用参考图中可观察的颜色、质感、构图密度和抽象程度，不复制其中的 Logo、文字、受保护界面或具体角色。

## 默认风格

默认风格用于科技、AI、产品、商业和职场类公众号文章。

### 视觉特征

- 克制的科技媒体编辑插画
- 扁平 2D 为主，保留少量 2.5D 空间层次
- 统一而纤细的线条
- 轻微纸张颗粒、丝网印刷或拼贴质感
- 构图存在人工调整感，避免过度光滑和绝对对称
- 每张图只保留一个主要视觉中心
- 使用留白建立阅读节奏
- 同一组图片保持颜色、线条和纹理一致
- 不同图片更换构图方式，避免像同一个模板反复替换图标

### 默认配色

- 深海军蓝
- 钴蓝
- 低饱和青色
- 柔和淡紫
- 暖白色
- 少量珊瑚橙作为提示色

默认只允许背景出现一处轻微渐变。主体尽量使用平涂、叠色和纹理。

### 默认禁止项

除非用户明确要求，不出现以下元素。

- 发光的可爱机器人
- 塑料质感的 3D 人物
- 过度美化的真人面孔
- 大量蓝紫霓虹光
- 悬浮在空中的密集界面卡片
- 通用的未来城市背景
- 镀铬材质和过度电影感光效
- 没有信息作用的盆栽、咖啡杯和装饰物
- 无法辨认的伪文字
- 随机英文、数字和时间
- 品牌 Logo、水印和未经授权的商标
- 与章节无关的脑袋、芯片、灯泡和握手图标
- 多余手指、错误设备结构和不合理透视

## 风格母版提示词

调用 ImageGen 时，将下面的内容作为每张图共享的风格提示词。

```text
Create a horizontal editorial illustration for a premium Chinese technology magazine and WeChat Official Account article.

The image must look deliberately art-directed by a human illustrator rather than like generic AI-generated artwork.

Use restrained flat 2D vector forms with a small amount of 2.5D depth, consistent thin linework, subtle paper grain or screen-print texture, slightly imperfect hand-cut geometric edges, generous negative space, asymmetric composition, and one clear focal point.

Use a limited palette of deep navy, cobalt blue, muted cyan, soft lilac, warm off-white, and one small coral accent. Use no more than one subtle background gradient.

Keep the composition clean, calm, practical, professional, and easy to read on a mobile screen.

Do not use photorealistic people, glossy plastic robots, cute AI mascots, cinematic stock-photo lighting, neon overload, crowded floating interface cards, futuristic city skylines, decorative office plants, pseudo-3D chrome, or generic AI brain imagery.

Do not include readable text, pseudo-text, letters, numbers, timestamps, logos, trademarks, signatures, or watermarks. Interface elements should use abstract lines and simple geometric shapes only.

Keep all important subjects inside the central safe area.
```

## 第三阶段：拆解每张图片的内容

不要直接把小标题交给图片模型。先提取每个章节的核心信息关系。

每张图至少明确四项内容。

1. 章节想说明什么
2. 谁或什么是画面主体
3. 主体正在发生什么动作
4. 读者需要一眼看懂什么关系

优先使用动作和关系表达抽象概念。

- “手机成为任务入口”可以画成手机消息触发电脑文件整理
- “Agent 拆解长任务”可以画成协调节点把任务分给多个模块，再汇总为报告
- “权限安全”可以画成人工确认挡住高风险删除操作
- “跨设备接续”可以画成同一任务从手机连续进入桌面端
- “生态竞争”可以画成聊天、文档和工具共同连接到任务中心

一张图只承担一个主要命题。章节里信息较多时，选择最能支撑标题的关系，不把所有细节都塞进画面。

## 内容提示词模板

在共享风格提示词之后追加每张图的内容提示词。

```text
Section concept: {用一句话说明章节观点}.

Show {主体} {动作或变化}.

The visual relationship should make it immediately clear that {读者需要看懂的关系}.

Use {构图方式}. Keep {主要视觉元素} as the single focal point.

Include only {必要辅助元素}. Remove any element that does not help explain the section.
```

## 常用构图方式

根据内容关系选择构图，不固定套用同一种版式。

### 起点与结果

适合任务发起、流程执行和成果交付。画面一侧放输入，另一侧放结果，中间只保留一条清晰路径。

### 中心与分支

适合 Agent 协作、能力调用和任务拆解。中心节点负责协调，周围模块承担不同工作，最终汇入一个结果。

### 边界与拦截

适合权限、安全、审核和风险控制。用工作区域、门、边框或透明容器表示权限范围，用人工动作表示确认。

### 跨设备连续路径

适合手机、电脑和多端接续。同一个任务标记贯穿不同设备，避免把画面画成两个互不相关的场景。

### 来源与汇总

适合知识、文档、工具和信息整合。多个来源经过一个处理节点，输出数量更少、结构更清楚的结果。

### 前后状态

适合效率变化、工作方式变化和流程简化。两侧展示不同状态，但不要使用夸张的“混乱对比完美”套路。

## 第四阶段：建立组图一致性

批量生成前，先在内部建立图片清单。每张图记录图片序号、对应章节、核心命题、主体、动作、信息关系、构图方式和珊瑚色强调位置。

同一批图片需要保持画面比例、主色范围、线条粗细、颗粒质感、人物抽象程度、图标抽象程度、留白比例和光影强度一致。

人物位置、主体大小、视觉重心、信息流方向、局部强调色和近远景关系应当适当变化。

避免每张图都采用左侧人物、右侧电脑、中间发光连线的重复结构。

## 第五阶段：调用 ImageGen

使用 ImageGen 生成或编辑图片。首次使用 ImageGen 前，读取可用的 ImageGen Skill 并遵循其图片引用、编辑和结果返回规则。

生成新图片时，每张图使用同一份风格母版，加上独立的内容提示词。

编辑已有图片时，先查看原图，再说明需要保留的内容和需要删除的 AI 特征。用户要求“去 AI 味”时，重点处理以下问题。

- 把发光机器人换成抽象节点或功能符号
- 把写实人物换成编辑插画人物、局部手部或几何剪影
- 删除伪界面文字
- 减少悬浮卡片数量
- 降低蓝紫霓虹和镜面反射
- 简化背景
- 修正手部、设备和透视
- 增加轻微纹理和不完全对称
- 保留原图表达的核心内容关系

如果本地原图缺失，但章节主题和原图内容已经明确，可以重新生成，并向用户说明这是按原主题重绘，不能声称完成了像素级编辑。

批量图片可以并行生成。生成时间较长时，向用户发送简短进度更新。

## 第六阶段：逐张检查

生成后检查每张图片。

### 内容检查

- 是否对应正确章节
- 是否一眼能看懂主要关系
- 是否出现与正文矛盾的元素
- 是否加入未经正文支持的新事实

### 视觉检查

- 是否存在伪文字或乱码
- 是否出现多余手指和错误设备
- 是否使用了过多发光效果
- 是否出现塑料感人物或机器人
- 是否保持整组风格一致
- 是否有足够留白
- 是否适合手机端阅读

### 批次检查

- 全部图片能否看出属于同一系列
- 构图是否存在明显重复
- 强调色是否分布均衡
- 图片与章节顺序是否一一对应

发现问题时，只重新生成失败的图片，不重做已经合格的整批图片。

## 第七阶段：交付

按文章顺序展示图片，并提供清楚的映射。

推荐格式如下。

```markdown
1. 章节标题
   图片链接或本地文件

2. 章节标题
   图片链接或本地文件
```

如果用户要求写入 Markdown、飞书文档或其他成稿，再使用对应的文档能力。插入文章时，默认把图片放在对应章节正文的末尾。用户指定放在标题下、案例后或其他位置时，按用户要求处理。

本地环境允许时，把最终图片非破坏性地复制到当前项目的持久目录中。使用清楚的文件名，例如：

```text
article-images/
├── 01-message-to-task.png
├── 02-easy-setup.png
├── 03-local-execution.png
└── 04-agent-collaboration.png
```

复制文件时保留 ImageGen 原始输出，不删除用户已有图片。

## 输出原则

- 图片服务文章，不抢文章的主题
- 内容对应准确优先于画面复杂
- 一致性优先于单张图片炫技
- 人工设计感来自取舍、留白和信息结构
- 用户确认过的视觉方向，在同一项目中继续沿用
- 新对话中没有可靠记忆时，要求用户重新提供参考图或明确风格名称
