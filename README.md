# AI-Film-Director-System

Personal AI filmmaking workflow system for cinematic MV, commercial film, cinematography and AI video generation.

面向个人导演的中文 AI 影像工作流：把创意需求转化为导演方案、摄影设计和可执行的视频生成提示词，适用于 MV、商业广告与概念短片。

## 当前版本

现已提供十个可独立阅读、按需组合的中文 Skill。它们是工作方法与交付规范，不是视频生成软件；仓库本身不会调用模型、生成影片或自动上传素材。

| Skill | 用途 | 主要交付 |
| --- | --- | --- |
| [01 导演总控](skills/01-director-core/SKILL.md) | 从需求到完整创作方向 | 项目简报、叙事节奏、镜头任务、执行顺序 |
| [02 MV 制作](skills/02-mv-production/SKILL.md) | 音乐与视觉结构设计 | 段落表、表演与意象设计、剪辑落点 |
| [03 商业广告](skills/03-commercial-film/SKILL.md) | 品牌主张与产品表达 | 广告脚本、产品证明镜头、多版交付方案 |
| [04 摄影设计](skills/04-cinematography/SKILL.md) | 将情绪转成可见的镜头选择 | 构图、机位、运动、光线、连续性设计 |
| [05 Seedance 执行](skills/05-seedance/SKILL.md) | 将镜头设计整理成生成输入 | 单镜头提示词、参考素材说明、参数核对与迭代记录 |
| [06 女性角色](skills/06-female-character/SKILL.md) | 人物设计与跨镜头一致性 | 角色卡、造型状态、表演与参考需求 |
| [07 素材管理](skills/07-asset-management/SKILL.md) | 素材与镜头版本追踪 | 资产清单、版本关系、缺失项与变更影响 |
| [08 色彩光线](skills/08-color-lighting/SKILL.md) | 全片色光规则与段落变化 | 色光方案、镜头匹配表、后期交接 |
| [09 分镜](skills/09-storyboard/SKILL.md) | 将脚本转成可执行镜头 | 计时分镜表、动作与空间衔接、素材需求 |
| [10 项目总管](skills/10-project-manager/SKILL.md) | 排期、依赖与交付统筹 | 任务表、预算记录、进度与验收清单 |

## 工作流

需求简报 → 导演方案 → MV / 商业广告专项设计（按需）→ 角色与色光规则 → 分镜与摄影设计 → Seedance 单镜头输入 → 生成结果检查 → 剪辑与交付。

素材管理和项目总管贯穿各阶段。可直接使用单个 Skill，不必每次运行十个模块。

镜头统一使用 S001、S002 等编号；修改提示词时保留编号并增加版本。摄影设计和生成执行沿用已确认的角色、服装、场景、运动方向与画幅。

## 仓库结构

```text
AI-Film-Director-System/
├── README.md
├── skills/
│   ├── 01-director-core/SKILL.md
│   ├── 02-mv-production/SKILL.md
│   ├── 03-commercial-film/SKILL.md
│   ├── 04-cinematography/SKILL.md
│   ├── 05-seedance/SKILL.md
│   ├── 06-female-character/SKILL.md
│   ├── 07-asset-management/SKILL.md
│   ├── 08-color-lighting/SKILL.md
│   ├── 09-storyboard/SKILL.md
│   └── 10-project-manager/SKILL.md
├── references/
│   └── README.md
└── templates/
    └── project-brief.md
```

## 开始使用

1. 复制 [项目简报模板](templates/project-brief.md)，填写已有信息；未确定的内容可以保留“待定”。
2. 将简报和对应 SKILL.md 一起交给能够读取文件的 AI 助手，明确要求按该文件执行。先用导演总控，再按需要使用摄影设计与 Seedance 执行。
3. 检查导演方案是否符合意图，再逐镜头准备参考图和生成输入。
4. 在实际视频生成平台核对版本、支持的输入与参数；记录生成结果，再决定修改或进入剪辑。

示例请求：

> 请读取 skills/01-director-core/SKILL.md，设计一支 30 秒、9:16 的原创服装概念短片。主题为“从束缚到自由”，单一成年角色、两个场景。先给导演方案和镜头任务，不执行视频生成。音乐尚未提供，请用暂定节奏而非虚构音乐时间码。

随后可以请求：

> 按 skills/04-cinematography/SKILL.md 细化 S001–S003，保持角色造型与运动方向一致；再按 skills/05-seedance/SKILL.md 输出各镜头的中文提示词。平台版本未知的参数标为待核对。

这里只保存 Skill 源文件。上传到 GitHub 不等于在某个 AI 客户端完成安装或启用；具体加载方式取决于使用的客户端。本次未修改本机技能配置。

## 按任务选择模块

- 制作 MV：01 → 02 → 09 → 04 → 05；需要时加入 06 和 08。
- 制作商业广告：01 → 03 → 09 → 04 → 05；用 07 追踪产品和商标素材。
- 解决角色漂移：06 建立角色与造型锚点，07 记录参考版本，05 修订相关镜头输入。
- 统筹项目：10 管理依赖与交付，07 维护素材；按具体创作任务读取其他模块。

编号用于目录排序，不代表必须依次执行。十个模块均已提供初版，实际生成、绘图、音频分析和发布仍取决于所使用环境的工具与授权。

## 参考资料与项目内容

参考资料整理方式见 [references](references/README.md)。当前没有导入《Lonely》《天地龙鳞》《S·DEER × MOMA》等项目，也不对其内容或创作方法作推断。公开仓库只保存适合公开且有权分享的资料；客户简报、未公开素材和访问凭据不放入本仓库。
