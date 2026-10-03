# Visual Aesthetics · 视觉审美与设计

版本 2.0.0。用于 agent 的视觉设计教材与审美指导，覆盖平面设计、图像、品牌、出版、信息、界面和动态内容。目标是把具体的视觉关系做得鲜明、有吸引力，不把不同任务统一为一种稳妥风格。

## 安装与使用

将完整仓库放进 Codex 的个人技能目录，并将文件夹命名为 `visual-aesthetics`。

macOS / Linux：

```bash
git clone https://github.com/non-convex/visual-aesthetics-skill.git "${CODEX_HOME:-$HOME/.codex}/skills/visual-aesthetics"
```

Windows PowerShell：

```powershell
$skillHome = if ($env:CODEX_HOME) { $env:CODEX_HOME } else { Join-Path $env:USERPROFILE '.codex' }
git clone https://github.com/non-convex/visual-aesthetics-skill.git (Join-Path $skillHome 'skills/visual-aesthetics')
```

如果目标目录已存在，请先确认其中是否有自己的修改，再决定如何更新。其他支持 `SKILL.md` 的 agent，可按其技能加载方式安装整个目录。

在支持技能调用的环境里，可以在任务中明确写出 `$visual-aesthetics`，例如：

```text
用 $visual-aesthetics 为这张展览海报发展一个鲜明的视觉方向，保留现有标题和日期。
```

```text
用 $visual-aesthetics 检查这个页面的字体、密度和色彩关系，指出具体位置和可修改的关系。
```

本技能提供判断方法与教材，不附带图像生成、网页开发或文档制作工具；实际创作使用所在 agent 环境已有的工具。

## 入口与阅读

从 [SKILL.md](SKILL.md) 开始。主文件说明跨媒介的取舍，并按问题指向 17 章教材。章节中先解释概念，再展开作用、做法、常见失效与局部变化；少量练习用于理解差别，不是每次任务必须执行的流程。

初学平面设计可以依次阅读视觉语法、构图、网格、字体、色彩、图文关系，再进入编辑出版与视觉系统。需要形成更鲜明的方向时，读艺术方向；需要把画面变成运动时，接着读动画与镜头。已有具体问题则直接进入对应章节，再回查不熟悉的概念。

保留整个 `visual-aesthetics/` 目录。只复制主文件会失去教材正文和示意图。目录中的相对链接不依赖特定平台；具体的技能加载位置由所用 agent 环境决定。

## 章节

| 章节 | 教什么 |
|---|---|
| [01 视觉语法](references/01-visual-grammar.md) | 点线面、轮廓、分组、图底、视觉重量与层次。 |
| [02 艺术方向](references/02-art-direction.md) | 越过惯用答案，发展材料、形式、相互作用和鲜明气质。 |
| [03 构图](references/03-composition.md) | 画框、比例、密度、失衡、空隙、裁切与方向。 |
| [04 网格与版式](references/04-grids-layout.md) | 从真实内容推导栏、栏距、版心、基线和跨栏结构。 |
| [05 字体与排版](references/05-typography.md) | 字形、选字、间距、断行、正文、光学调整与中西文。 |
| [06 色彩](references/06-color.md) | 色相、明度、彩度、面积、邻接、叠色与配色判断。 |
| [07 图文关系与海报](references/07-image-text-posters.md) | 图与字怎样互相塑造，信息怎样进入整体。 |
| [08 编辑与出版](references/08-editorial.md) | 真实文稿、单页、跨页、序列、图注、导航与封面。 |
| [09 视觉系统与识别](references/09-identity-systems.md) | 标志、字标、图标、稳定关系与可变系列。 |
| [10 材料与载体](references/10-print-surface.md) | 纸墨、颜色管理、套印、网点、裁边、折叠与观看尺寸。 |
| [11 造型与图像](references/11-image-language.md) | 姿态、轮廓、线条、绘画、拼贴、纹样和风格化。 |
| [12 光与材料](references/12-light-material.md) | 用光、体积、支撑、接触、反射、材质差异和边缘。 |
| [13 动画与运动](references/13-motion.md) | 位移、路径、支点、重量、停顿、形变、循环和中断。 |
| [14 镜头与影像](references/14-cinematography.md) | 观看位置、场面、运镜、镜头内发展、省略和剪辑。 |
| [15 界面视觉](references/15-interfaces.md) | 内容组织、密度、响应式、状态、导航与使用中的个性。 |
| [16 信息设计](references/16-information.md) | 比较、编码、坐标、标签、图解、地图和数据艺术。 |
| [17 视觉诊断](references/17-critique.md) | 从现象定位原因，作出修改，并保住作品的性格。 |

## 示意图与依据

九组原创建模示意放在 `assets/figures/`。每组提供 PNG 与 SVG；章节直接引用 PNG，SVG 保留形状、位置与标注。它们解释分组、网格、字距、相对颜色、页序、裁边、位移、循环和面积编码，不是风格模板。图的关系在附近正文也有文字解释；不能查看图像时，仍可读懂概念，但不应声称已经做过视觉比较。

[来源说明](references/sources.md) 列出 34 组资料的阅读范围、采用内容与适用边界。真实作者案例与教学设想分开标注。资料并不组成统一流派；具体手法的使用始终要结合内容和观看条件。

## 验证范围

本次开源打包检查了技能格式、内部链接与锚点、图像文件完整性，以及教材和示意图与原始版本的一致性。没有运行真实 agent 的生成质量对照实验，因而不把文件校验或调研依据当成审美提升已经被证明。

## 许可证

仓库中的技能文本、教材与原创示意图采用 [MIT License](LICENSE)。来源说明中链接的第三方文章、书籍、作品、品牌和字体仍属于各自权利人，不因被引用而采用本仓库的许可证。
