---
title: 'Home'
date: 2024-10-21
type: landing

# Enable FAQ structured data on homepage
faq_page: true
faqs:
  - question: "什么是智库?"
    answer: "AI Knowledge Hub 是你系统掌握 AI 工具、提升效率的一站式资源库。我们提供专家解答、实用指南与社区经验，帮助你更高效地用好 AI。"
  
  - question: "这个知识库可以免费使用吗?"
    answer: "可以！我们的知识库完全免费并向所有人开放。我们相信 AI 知识应当被普及，让全球个人与组织都能受益。"
  
  - question: "内容多久更新一次?"
    answer: "我们每天都会更新知识库，补充新的问题、答案和洞见。你可以订阅我们，持续了解最新 AI 动态。"

sections:
  - block: search-hero
    content:
      badge:
        text: "千里之行始于足下"
        show_pulse: True
      title: |
        个人 ==数据库==
        
        探索一切 ====
      subtitle: "从我们的综合知识库中快速获得 AI 问题答案。向专家学习最佳实践，始终走在 AI 前沿。"
      search_placeholder: "搜索 AI 工具、提示词或工作流相关问题..."
      suggestions:
        - "ChatGPT 提示词"
        - "Midjourney 技巧"
        - "AI 自动化"
        - "Claude 与 GPT-4 对比"
      stats:
        - value: "2,500+"
          label: "专家解答"
        - value: "50K+"
          label: "月活用户"
        - value: "4.9/5"
          label: "用户评分"
    design:
      background:
          gradient_mesh:
            enable: true
            style: "orbs"  # Options: orbs, waves, dots, grid
            animation: "pulse"  # Options: pulse, float, rotate, none
            intensity: "subtle"  # Options: subtle, medium, bold
            colors:
              - "primary-500/20"
              - "primary-600/20"
            # Optional: customize orb positions and sizes
            # orb_count: 2
            # positions: ["top-0 left-1/4", "bottom-0 right-1/4"]
            # sizes: ["w-96 h-96", "w-96 h-96"]
      spacing:
        padding: ["8rem", "0", "6rem", "0"]

  - block: knowledge-categories
    id: categories
    content:
      title: 按分类浏览
      subtitle: 按主题与难度快速找到答案
      categories:
        - category: "入门"
          title: "入门"
          description: "刚接触 AI？从基础概念与核心知识开始"
          icon:
            name: rocket-launch
            bg_color: "bg-green-100 dark:bg-green-900/50"
            text_color: "text-green-600 dark:text-green-400"
        
        - category: "ChatGPT"
          title: "ChatGPT 与 Claude"
          description: "掌握对话式 AI 与提示词工程"
          icon:
            name: chat-bubble-left-right
            bg_color: "bg-blue-100 dark:bg-blue-900/50"
            text_color: "text-blue-600 dark:text-blue-400"
        
        - category: "图像生成"
          title: "图像生成"
          description: "用 Midjourney、DALL-E 等工具创作高质量视觉内容"
          icon:
            name: photo
            bg_color: "bg-purple-100 dark:bg-purple-900/50"
            text_color: "text-purple-600 dark:text-purple-400"
        
        - category: "AI 自动化"
          title: "AI 自动化"
          description: "构建工作流，用 AI 自动完成重复任务"
          icon:
            name: cog
            bg_color: "bg-orange-100 dark:bg-orange-900/50"
            text_color: "text-orange-600 dark:text-orange-400"
        
        - category: "编程"
          title: "AI 编程"
          description: "GitHub Copilot、Cursor 与 AI 驱动开发实践"
          icon:
            name: code-bracket
            bg_color: "bg-indigo-100 dark:bg-indigo-900/50"
            text_color: "text-indigo-600 dark:text-indigo-400"
        
        - category: "AI 商业应用"
          title: "AI 商业应用"
          description: "面向企业场景的解决方案与实践"
          icon:
            name: briefcase
            bg_color: "bg-gray-100 dark:bg-gray-800"
            text_color: "text-gray-600 dark:text-gray-400"
        
        - category: "伦理与安全"
          title: "伦理与安全"
          description: "负责任地使用 AI 的原则与安全指南"
          icon:
            name: shield-check
            bg_color: "bg-red-100 dark:bg-red-900/50"
            text_color: "text-red-600 dark:text-red-400"
        
        - category: "最新动态"
          title: "最新动态"
          description: "AI 领域最新新闻与趋势更新"
          icon:
            name: newspaper
            bg_color: "bg-yellow-100 dark:bg-yellow-900/50"
            text_color: "text-yellow-600 dark:text-yellow-400"
          
      view_all:
        text: "查看全部分类"
        link: "/categories/"

  - block: trending-questions
    id: trending
    content:
      title: "🔥 热门问题"
      subtitle: "社区当前最关注的话题"
      questions:
        - question: "如何写出更好的 ChatGPT 编程提示词？"
          answer_preview: "掌握 5 个关键技巧：描述具体目标、补充上下文、提供示例、明确约束并持续迭代..."
          link: "/questions/chatgpt-coding-prompts/"
          badge:
            text: "热门"
            color: "bg-red-100 text-red-800 dark:bg-red-900/30 dark:text-red-200"
          author: "Alex Chen"
          views: "12.5k"
          upvotes: 234
        
        - question: "GPT-4 和 Claude 3 的区别是什么？"
          answer_preview: "从能力、价格和适用场景对比两款主流模型。GPT-4 擅长..."
          link: "/questions/gpt4-vs-claude3/"
          badge:
            text: "已更新"
            color: "bg-blue-100 text-blue-800 dark:bg-blue-900/30 dark:text-blue-200"
          author: "Sarah Liu"
          views: "8.3k"
          upvotes: 189
        
        - question: "AI 会取代我的开发工作吗？"
          answer_preview: "理解 AI 对软件开发职业的影响，并学习如何打造更有韧性的技能组合..."
          link: "/questions/ai-developer-jobs/"
          author: "Mike Johnson"
          views: "15.2k"
          upvotes: 412
        
        - question: "如何在 Midjourney 中创建稳定一致的角色？"
          answer_preview: "学习 seed 技巧与风格参考，在不同画面中保持角色一致性..."
          link: "/questions/midjourney-consistent-characters/"
          badge:
            text: "趋势"
          author: "Emma Davis"
          views: "6.7k"
          upvotes: 156
          
      view_all:
        text: "浏览全部问题"
        link: "/questions/"
    design:
      background:
        color: "bg-gray-50 dark:bg-gray-900"
      spacing:
        padding: ["4rem", "0", "4rem", "0"]

  - block: features
    content:
      title: 为什么选择 AI Knowledge Hub？
      text: 由 AI 专家打造，帮助每个人把人工智能真正用到工作与生活中
      items:
        - name: 专家审核
          icon: shield-check
          description: 每个答案都经过 AI 从业者与行业专家审核验证。
        
        - name: 持续更新
          icon: arrow-path
          description: 每日更新最新 AI 动态、工具进展与实践方法。
        
        - name: 社区驱动
          icon: user-group
          description: 向 50,000+ AI 爱好者与专业人士组成的活跃社区学习。
        
        - name: 注重实战
          icon: beaker
          description: 提供真实案例、代码片段与可直接落地的行动建议。
        
        - name: 新手友好
          icon: academic-cap
          description: 面向不同水平用户提供清晰解释与学习路径。
        
        - name: 永久免费
          icon: gift
          description: 无付费墙、无订阅门槛。知识应当对所有人开放。

  - block: faq
    content:
      title: 常见问题
      subtitle: 关于平台的高频问题速览
      items:
        - question: "如何为知识库做贡献？"
          answer: |
            你可以通过以下方式参与：
            - 提出尚未被回答的新问题
            - 为已有问题补充高质量答案
            - 给有帮助的内容点赞
            - 提交修改建议与优化意见
            
            点击导航栏中的“贡献”按钮即可开始！
        
        - question: "我可以把这些内容用于自己的项目吗？"
          answer: "可以！所有内容均基于 Creative Commons 许可发布。你可以在标注来源为 AI Knowledge Hub 的前提下使用、改编和分享。"
        
        - question: "你们如何保证答案质量？"
          answer: "我们采用多层审核机制：社区投票、专家复核，以及基于用户反馈的持续更新。过时或错误信息会被快速标记并修正。"
        
        - question: "提供 API 访问吗？"
          answer: "目前我们提供 RSS 订阅和 JSON 导出。完整 API 已在路线图中，目标发布时间为 2025 年 Q2。欢迎订阅获取更新！"
        
        - question: "你们和 ChatGPT 或 Claude 有什么不同？"
          answer: "相比通用聊天机器人，我们提供的是经过筛选、可验证、格式统一、并聚焦 AI 实操场景的知识答案。你可以把我们理解为专注 AI 的专业参考手册。"
    design:
      spacing:
        padding: ["4rem", "0", "4rem", "0"]

  - block: cta-card
    content:
      title: "准备好掌握 AI 了吗？"
      text: 加入数千名专业人士与爱好者，一起学习如何最大化发挥 AI 的价值。
      button:
        text: "立即开始探索 →"
        url: "/questions/"
    design:
      card:
        css_class: "bg-gradient-to-r from-primary-200 to-primary-300 dark:from-primary-800 dark:to-primary-900"
---
