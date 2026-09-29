# AI-Film-Director-System

Personal AI filmmaking workflow system for cinematic MV, commercial film, cinematography and AI video generation.

面向个人导演的中文 AI 影像工作流：把创意需求转化为导演方案、摄影设计和可执行的视频生成提示词，适用于 MV、商业广告与概念短片。

## 当前版本

首批提供三个可独立阅读的 Skill。它们是工作方法与交付规范，不是视频生成软件；仓库本身不会调用模型、生成影片或自动上传素材。

| Skill | 用途 | 主要交付 |
| --- | --- | --- |
| [01 导演总控](skills/01-director-core/SKILL.md) | 从需求到完整创作方向 | 项目简报、叙事节奏、镜头任务、执行顺序 |
| [04 摄影设计](skills/04-cinematography/SKILL.md) | 将情绪转成可见的镜头选择 | 构图、机位、运动、光线、连续性设计 |
| [05 Seedance 执行](skills/05-seedance/SKILL.md) | 将镜头设计整理成生成输入 | 单镜头提示词、参考素材说明、参数核对与迭代记录 |

## 工作流

需求简报 → 导演方案 → 摄影镜头表 → Seedance 单镜头输入 → 生成结果检查 → 剪辑与交付。

镜头统一使用 S001、S002 等编号；修改提示词时保留编号并增加版本。摄影设计和生成执行沿用已确认的角色、服装、场景、运动方向与画幅。

## 仓库结构

```text
AI-Film-Director-System/
├── README.md
├── skills/
│   ├── 01-director-core/SKILL.md
│   ├── 04-cinematography/SKILL.md
│   └── 05-seedance/SKILL.md
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

## 后续规划

以下模块尚未实现，不应当作已可调用功能：

- 02-mv-production：音乐结构、表演与节奏剪辑。
- 03-commercial-film：品牌诉求、产品镜头与广告交付。
- 06-female-character：女性角色设计与跨镜头一致性。
- 07-asset-management：角色、场景、服装与素材版本管理。
- 08-color-lighting：色彩与光线系统。
- 09-storyboard：可拍摄、可生成的分镜。
- 10-project-manager：排期、版本与交付管理。

## 参考资料与项目内容

参考资料整理方式见 [references](references/README.md)。当前没有导入《Lonely》《天地龙鳞》《S·DEER × MOMA》等项目，也不对其内容或创作方法作推断。公开仓库只保存适合公开且有权分享的资料；客户简报、未公开素材和访问凭据不放入本仓库。
