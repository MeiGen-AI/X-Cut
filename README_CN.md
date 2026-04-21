<div align="center">

<img src="assets/figs/x-cut.png" alt="X-CUT" width="140" style="border-radius: 15px;">

# X-CUT：对话驱动的可实时渲染的视频剪辑 Agent

[![Python 3.12+](https://img.shields.io/badge/Python-3.12%2B-3776AB?style=flat-square&logo=python&logoColor=white)](https://www.python.org/downloads/) [![React 18](https://img.shields.io/badge/React-18-61DAFB?style=flat-square&logo=react&logoColor=white)](https://react.dev/) [![TypeScript](https://img.shields.io/badge/TypeScript-5.2-3178C6?style=flat-square&logo=typescript&logoColor=white)](https://www.typescriptlang.org/) [![FastAPI](https://img.shields.io/badge/FastAPI-0.110+-009688?style=flat-square&logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com/) [![Remotion](https://img.shields.io/badge/Remotion-4.0-0B84F3?style=flat-square)](https://www.remotion.dev/) [![Agno](https://img.shields.io/badge/Agno-Agent_Framework-FF6B35?style=flat-square)](https://github.com/agno-agi/agno) [![License](https://img.shields.io/badge/License-AGPL--3.0-blue?style=flat-square)](LICENSE)

[核心特性](#-核心特性) · [演示](#-演示) · [快速开始](#-快速开始) · [技能系统](#-技能系统) · [路线图](#-路线图)

[🇨🇳 中文](README_CN.md) · [🇬🇧 English](README.md)

</div>

---

## 📖 概述

X-CUT 是一个 AI 视频剪辑 Agent——通过**自然语言对话**将创意变为成片。只需在聊天界面描述想法，Agent 理解意图、按需澄清、动态选择和组合技能、编辑多轨时间线。成片过程基于Remotion实时渲染到轨道上，每一步操作即时可见，满意后一键导出。

不用拖时间线，不用调关键帧，只需要向X-Cut描述你的剪辑需求

> **"帮我把这段旅拍素材剪成一个 Vlog，加点轻松的背景音乐和字幕"**
> — Agent 接手一切：素材分析、脚本生成、画面编排、配乐、配音、MG 动效、最终渲染——一句话搞定。

---

## ✨ 核心特性

- 🎬 **智能素材分析与剧本生成：** 自动分析上传的视频/图片素材——景别分析、运镜分析、内容理解。基于用户意图和素材内容，Agent 生成剧本预览。
- 🎨 **MG 动画生成：** 内置 LLM 驱动的MG动画代码生成器，借助remotion skills将自然语言指令实时转化为 Remotion JSX 组件。支持添加转场、片头片尾以及任意自然语言描述的动画渲染到视频任意位置，提供新建和修改两种模式。只需描述需求："在右侧加一个旅游攻略信息卡"、"让标题更活泼一点"——Agent 即时生成、转译并渲染。
- 🎵 **智能配乐、配音与字幕：** 基于素材分析结果自动生成匹配视频氛围的背景音乐，基于剧本旁白自动合成配音（支持多种音色选择、音色克隆），并渲染时间轴对齐的字幕——所有环节由 Agent 在一次对话中统一编排。
- 💬 **对话式剪辑：** 通过对话可任意剪辑操作，包括但不限于增删改配音、动画、字幕、音色等，基于 Remotion Player 实时渲染——所见即所得，满意即导出。
- 📌 **引用式修改：** 轨道上的渲染结果，由原始素材叠加生成的配音、配乐、动画组合而成，对任意部分可进行引用式修改，修改不改变其余部分结果，实现精准剪辑
- 🖱️ **轨道自由拖动：** 对对话剪辑结果不满意？可以通过timeline上实时渲染的结果，手动进行素材拖拽、换位、删除、新增等。
- ⚡ **剪辑风格沉淀与分享：** 将任意项目的剪辑配方保存为可复用的 Skill——涵盖结构、节奏、音乐风格、配音偏好和 MG 动画模式。下次只需导入新素材并应用 Skill，即可一键复刻同款风格，实现高效批量生产。同时也支持按照md文件分享。

---

## 🎬 演示

### 界面总览

<!-- TODO: 替换为实际截图 / 视频 -->
| | | |
|:---:|:---:|:---:|
| ![总览 1](assets/figs/interface/entry.png) | ![总览 2](assets/figs/interface/chat-canvas.png) | ![总览 3](assets/figs/interface/chat-edit.png) |
| *X-Cut 首页* | *对话 + 画布* | *对话 + 编辑器* |

### 成片展示

> *为满足 GitHub 视频上传体积要求，所有视频均经过极致的压缩。在 X-CUT 中，你可以导出各种分辨率的视频，保证成片的质量。*

#### Vlog 制作

> **素材：** 5 段旅拍视频  
> **指令：** *"帮我做一个海边旅行 Vlog"*

<table>
<tr>
<td width="50%">

**录屏演示**

https://github.com/user-attachments/assets/9eff8013-518c-44fa-8bc7-2d44d6551882

</td>
<td width="50%">

**成片效果**

https://github.com/user-attachments/assets/fbd2f4e2-f3f0-4415-96fa-11ea7c69c269

</td>
</tr>
</table>

#### 营销宣传片制作

> **素材：** 9 张产品图片（截图自小米官网）  
> **指令：** *"帮小米 YU7 做一个宣传视频"*

<table>
<tr>
<td width="50%">

**录屏演示**

https://github.com/user-attachments/assets/8007d668-ecbd-4acf-976b-4a76794b6797

</td>
<td width="50%">

**成片效果**

https://github.com/user-attachments/assets/981e1cbc-f6a2-4ed0-9228-07288399d851

</td>
</tr>
</table>

#### 自由编辑

> **素材：** 1 段视频  
> **指令：** *"在画面右侧三分之一处生成一个海南旅游攻略，mock一份数据，尽量详细一点"*  
> **后续：** *"把背景改成透明"*

<table>
<tr>
<td width="50%">

**录屏演示**

https://github.com/user-attachments/assets/db586ca5-34b8-41c1-8e45-dcf71865eeb7

</td>
<td width="50%">

**成片效果**

https://github.com/user-attachments/assets/1aae6060-ba99-4d94-a3f8-ce6c912dbd79

</td>
</tr>
</table>

> **素材：** 多段视频片段  
> **指令：** *"给这几个素材加上转场"*  
> **后续：** *"1.修改为推拉效果； 2.增加一个森林里VLOG标题，中英文排版，英文为副标题，并增加一些几何元素装饰，透明背景"*

<table>
<tr>
<td width="50%">

**录屏演示**

https://github.com/user-attachments/assets/c28bdf7a-3592-4058-8786-f8f49e828e47

</td>
<td width="50%">

**成片效果**

https://github.com/user-attachments/assets/71d975e4-a5ed-44f9-94d9-63fcc9287b8f

</td>
</tr>
</table>

#### 风格分享与复用

> 通过「分享」按钮将剪辑风格提炼为可复用模板，以 `.md` 文件分享或保存到个人空间。下次创建新项目时，可直接使用该模板生成相似风格的视频。

**录屏演示**

https://github.com/user-attachments/assets/46b244ce-3ebb-459d-b320-80e696807a8f


## 🧩 技能系统

技能（Skills）是 X-CUT Agent 的能力核心，按类别组织，易于扩展。Agent 根据用户意图动态选择和组合技能，无固定流水线，灵活可组合。

```
.xcut_skills/system/
├── entry/           → Agent 加载的顶层入口技能
├── scenes/          → vlog-generation, marketing-generation, free-edit,
├── operations/      → audio-edit, dubbing-edit, mg-edit, opening-ending-edit,
│                      track-delete, transition-edit
├── styles/          → marketing-conversion, vlog-natural（可分享的剪辑风格）
├── templates/       → marketing-hook-sell-cta, vlog-story
├── tools/           → analyze-assets, build-script, generate-visuals,
│                      generate-music, add-dubbing, mg-animation,
│                      resolve-voice-id, apply-timeline-strategy, references
└── prompt-specs/    → script-from-style
```

### Agent + 技能协作机制

1. **入口技能** — Agent 始终加载入口技能作为顶层能力。
2. **场景选择** — 根据用户意图，Agent 选择合适的场景技能（Vlog、营销等）。
3. **技能装配** — `RuntimeSkillBuilder` 将入口技能拷贝到任务级目录，并将选中的场景/用户/共享技能装配为引用。
4. **灵活执行** — Agent 读取装配的技能引用，灵活编排工具——没有固定流水线，而是技能驱动的智能决策。

### 风格分享与导入

风格是一种特殊的技能，记录了剪辑配方——结构、节奏、音乐风格、配音偏好等。用户可以：

- **浏览** 首页风格广场，发现社区风格
- **预览** 风格的完整配置详情
- **应用** 任何风格，一键创建新项目并按该创意方向开始
- **分享** 将你的项目剪辑配方发布到社区，生成新的风格技能
- **导入** 从 `.md` 文件导入风格，支持分享
- **下载** 将任意风格导出为便携的 `.md` 文件

---

## 🚀 快速开始

我们正在整理开源模型/API接入方案，代码即将释放

---

## 🗺 路线图

| 状态 | 里程碑 |
|:---:|:---|
| 🔜 | Web版本源码+部署指南发布 |
| 🔜 | 独立 Skills 发布——可接入 Claude、OpenClaw 等 |
| 🔜 | CLI 版本发布 |
| 🔜 | 长视频拆解剪辑 |
| 🔜 | 口播视频剪辑 |
| 🔜 | 更多可能...... |

---

## 🤝 参与贡献
---

## 📄 许可证

本项目基于 GNU Affero General Public License v3.0 开源 — 详见 [LICENSE](LICENSE) 文件。

---

<div align="center">

**X-CUT** — 和 Agent 对话，看它实时剪辑。

[报告问题](../../issues) · [功能建议](../../issues) · [讨论](../../discussions)

</div>
