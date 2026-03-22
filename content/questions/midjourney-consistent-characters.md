---
title: "如何在 Midjourney 中创建稳定一致的角色？"
date: 2024-10-19
lastmod: 2024-10-21
draft: false

# Q&A specific fields
question: "如何在 Midjourney 中创建稳定一致的角色？"
answer: "可结合角色参考（--cref）、seed 数字、详细角色设定表以及 Style Reference 功能，在多次生成中保持角色一致性。"

summary: "系统掌握 Midjourney 角色一致性创作：角色参考、风格表、seed 优化与高级参数实战。"

difficulty: "高级"
categories: ["图像生成"]
tags: ["midjourney", "ai-艺术", "角色设计", "一致性", "stable-diffusion", "提示词"]

upvote_count: 276
downvote_count: 4

# Trending status
trending: true
trending_weight: 4  # Lower number = higher priority
badge:
  text: "🎨 创意"
  color: "bg-purple-100 text-purple-800 dark:bg-purple-900/30 dark:text-purple-200"
views: "8.7k"

# Additional expert answers
suggested_answer:
  - text: "专业建议：先做一张角色三视图/转面图！用 ‘character turnaround, front view, side view, back view, three-quarter view’ 一次生成多角度形象，把它作为后续全部创作的主参考图。"
    author: "Alex Rivera，数字艺术家"
    date: 2024-10-18
    upvote_count: 92
  
  - text: "对我最关键的是把 --cref 和 --cw（character weight）一起用。先用 --cw 100 保证高度一致；当你想换服装或表情时，降到 50-70，既保留脸部特征又保留变化空间。"
    author: "Maya Patel，Ubisoft 概念艺术师"
    date: 2024-10-17
    upvote_count: 78

seo:
  title: "Midjourney 角色一致性：2024 完整指南"
  description: "学习如何用角色参考、seed、风格表与高级参数，在 Midjourney 中稳定生成一致角色。"
---

在 Midjourney 中跨多张图保持角色一致，一直是 AI 艺术创作的难点。随着 Midjourney V6 与新功能更新，这件事已经变得可控得多。下面是完整实战指南。

## 先理解问题本质

角色一致性难，主要因为：
- 每次生成都从随机噪声开始
- 提示词的微小变化会带来明显差异
- 模型对描述的理解会波动
- 五官、比例和细节容易漂移

但 Midjourney 现在已经提供了多种非常有效的解决方案。

## 方法 1：角色参考（--cref）🎯

**角色参考参数** 是目前最强的一致性工具。

### 基础用法

```
/imagine prompt: [your scene description] --cref [image URL]
```

### 分步流程

1. **先生成基础角色**
   ```
   /imagine prompt: beautiful female elf warrior, long silver hair, 
   violet eyes, detailed face, fantasy art style --v 6 --ar 2:3
   ```

2. **保存最佳结果**
   - 右键复制图片地址
   - 或上传到 Discord 后复制链接

3. **作为参考复用**
   ```
   /imagine prompt: the same elf warrior sitting in a tavern 
   --cref https://[your-image-url] --v 6
   ```

### 角色权重（--cw）

控制 Midjourney 对参考图的贴合程度：

```
--cw 100  (default) = Exact match (face, hair, clothing)
--cw 0    = Only facial features
--cw 50   = Balance between face and overall appearance
```

换装时的示例：
```
/imagine prompt: elf warrior in modern clothing 
--cref [URL] --cw 50 --v 6
```

## 方法 2：Seed 一致性 🌱

Seed 可以提供可复现的生成起点。

### 如何获取 Seed

1. 先生成角色图
2. 使用 ✉️ 表情反应
3. 在私信里查看 seed 编号

### 如何使用 Seed

```
/imagine prompt: male detective, noir style, trench coat 
--seed 777 --v 6
```

同一个 seed 做不同动作变体：
```
/imagine prompt: male detective, noir style, smoking 
--seed 777 --v 6

/imagine prompt: male detective, noir style, running 
--seed 777 --v 6
```

**专业建议**：把 seed 和 style reference 结合使用，一致性更高。

## 方法 3：角色转面图（Turnaround Sheet）📐

先生成一张含多个角度的主参考图：

### 推荐提示词结构

```
/imagine prompt: character turnaround sheet, female pirate captain, 
red hair, eye patch, multiple poses, front view, side view, 
back view, three-quarter view, white background, 
character design sheet --ar 16:9 --v 6
```

### 如何应用

1. 生成转面图
2. 将其作为后续 `--cref`
3. Midjourney 能更好理解角色在不同角度下的样子

## 方法 4：风格参考（--sref）🎨

在改变动作或场景时保持美术风格一致：

```
/imagine prompt: character doing [action] 
--sref [style image URL] --cref [character URL] --v 6
```

这样可以同时稳定“角色”和“画风”。

## 方法 5：详细模板化提示词 📝

先建立角色主模板：

```yaml
Character Base:
  Name: Aria Starweaver
  Race: Elf
  Age: appears 25
  Hair: Long silver hair with blue highlights
  Eyes: Violet eyes with golden flecks
  Face: Heart-shaped face, high cheekbones
  Build: Athletic, 5'8" tall
  Clothing: Blue and silver robes with celestial patterns
  Accessories: Crystal pendant, silver circlet
  
Prompt Template:
  "Aria Starweaver, elf woman, long silver hair with blue highlights, 
  violet eyes with golden flecks, heart-shaped face, high cheekbones, 
  athletic build, blue and silver robes with celestial patterns, 
  crystal pendant, silver circlet, [SCENE DESCRIPTION]"
```

## 进阶技巧

### 1. 多图角色参考

Midjourney V6 支持多个角色参考图：

```
/imagine prompt: character in battle 
--cref [URL1] [URL2] [URL3] --v 6
```

可综合多张参考图特征，提升一致性。

### 2. 局部变化（Vary Region）

使用 Vary Region 功能：
1. 先生成基础图
2. 选择 Vary Region
3. 只改局部（背景、姿态等）
4. 保持角色主体不变

### 3. Blend 过渡生成

用于角色阶段演变：
```
/blend [young character URL] [old character URL]
```

再把混合结果作为中间年龄版本的参考图。

### 4. Permutation 批量测试

高效测试多个变体：
```
/imagine prompt: {young, middle-aged, old} wizard, 
same facial features --cref [URL] --v 6
```

## 常见问题与解决方案

### 问题：脸变形太大

**解决：**
- 把 `--cw` 提高到 100
- 在提示词补充 "same face, same person"
- 使用更近景的人脸图做 `--cref`

### 问题：细节容易丢失

**解决：**
- 提示词写得更具体
- 使用 `--quality 2` 提升细节
- 增加 "highly detailed, sharp focus"

### 问题：性别/年龄跑偏

**解决：**
- 每次都显式写明性别与年龄
- 使用 "definitely male" / "definitely female"
- 增加年龄描述，如 "young adult"、"elderly"

### 问题：画风不稳定

**解决：**
- 固定风格关键词
- 使用 `--sref` 风格参考图
- 增加艺术家风格或艺术流派关键词

## 一套可复用的专业工作流

### Step 1：角色开发
```
/imagine prompt: character design sheet, male cyberpunk hacker, 
Asian features, neon green mohawk, cybernetic eye implant, 
leather jacket with LED strips, multiple expressions, 
white background --ar 16:9 --v 6 --style raw
```

### Step 2：筛选与微调
- 选出最佳结果
- 用 Vary Subtle 做微调
- 保存最终参考图

### Step 3：建立场景库
```
Base prompt structure:
"Kenji (cyberpunk hacker), Asian male, neon green mohawk, 
cybernetic eye, leather jacket with LEDs, [SCENE]"

Scene 1: --cref [URL] "sitting at computer terminal"
Scene 2: --cref [URL] "running through neon city"
Scene 3: --cref [URL] "in combat with drone"
```

### Step 4：建立一致性记录

建议记录：
- 角色参考图 URL
- 成功 seed
- 高成功率提示词模板
- 不同场景下的 `--cw` 配置

## 快速参数备忘

```markdown
Essential Parameters:
--cref [URL]        : Character reference
--cw [0-100]       : Character weight
--sref [URL]       : Style reference
--seed [number]    : Reproducible randomness
--v 6              : Latest version

Consistency Formula:
Base Prompt + --cref + --seed + --sref = Maximum Consistency

Prompt Structure:
1. Character name/description
2. Physical attributes
3. Clothing/accessories
4. Action/scene
5. Style descriptors
6. Technical parameters
```

## 社区经验

💡 **建立角色圣经（Character Bible）**：把有效和无效提示词都记录下来，知道什么“不能用”同样关键。

💡 **使用真实照片作参考**：在写实风格中，把真实照片作为 `--cref` 往往更稳定。

💡 **批量生成再筛选**：一次生成 10-20 张，再挑最稳定的作为下一轮参考。

💡 **跨风格压力测试**：用同一个角色参考图套不同风格提示词，检验鲁棒性。

## 最新更新（2024 年 10 月）

- `--cref` 对种族特征保留更好
- 支持组合多个 `--cref` URL
- `--cw` 控制粒度更精细
- Vary Region 可结合角色参考使用
- 对年龄阶段变化处理更稳定

## 故障排查清单

当一致性失效时检查：
- [ ] `--cref` 链接是否仍可访问
- [ ] 是否明确包含 `--v 6`
- [ ] 提示词是否与参考图冲突
- [ ] 是否需要调整 `--cw`
- [ ] 是否可用 `--style raw` 降低模型主观解释
- [ ] 是否用相同 seed 复现

## 总结

如今在 Midjourney 中做角色一致性，已经比以前容易很多。核心是组合使用多种手段：用 `--cref` 锁定角色、用 seed 保证可复现、用模板化提示词控制细节。

建议先把 `--cref` 作为基线，再根据项目需求叠加其它方法。

记住：高质量一致性通常需要 5-10 次迭代。即使是专业艺术家，也依赖反复打磨。

---

**下一步建议**：你可以从资源区下载免费的 Midjourney 角色一致性模板，用于系统记录每次创作参数。

*如果你有更有效的方法，欢迎在评论区分享给社区！*
