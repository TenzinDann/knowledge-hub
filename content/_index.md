---
title: 'Home'
date: 2024-10-21
type: landing

# Enable FAQ structured data on homepage
faq_page: true
faqs:
  - question: "什么是智库?"
    answer: "Knowledge Hub 是你系统掌握 AI 工具、提升效率的一站式资源库。我们提供专家解答、实用指南与社区经验，帮助你更高效地用好 AI。"
  
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
        Knowledge Hub ==智库==
        
        质疑一切 ==探索一切==
      subtitle: "个人综合数据库，涵盖本人使用的各类领域和各类数据"
      search_placeholder: "搜索 AI 工具、提示词或工作流相关问题..."
      suggestions:
        - "机器学习流程"
        - "prompts技巧"
        - "前端数据集合"
        - "游戏模组数据备份"

      stats:
        - value: "1000+"
          label: "机器学习数据集"
        - value: "50+"
          label: "前端网络设计资源"
        - value: "100+"
          label: "prompt技巧"

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


  - block: faq
    content:
      title: 常见问题
      subtitle: (其实没人问)
      items:
        - question: "这个智库是干啥的"
          answer: |
            这个智库本质是本人的网络仓库，但是会用于与他人分享资源，包括但不限于：
            - 用于prompt的各种skills
            - 用于不同类型的agent.md
            - 用于前端的各种资源
            - 用于娱乐的游戏模组资源
            
            希望这个仓库麻雀虽小五脏俱全，如果能帮到你的话，非常荣幸！
        
        - question: "我可以把这些内容用于自己的项目吗？"
          answer: "可以！所有内容都是用于分享的。你可以在标注来源为 TenzinDann 的前提下使用、改编和分享"
        
        - question: "提供 API 访问吗？"
          answer: "我就一学生，莫得钱搭建服务器来给你提供API"
        
        - question: "网站上的AI是真的吗"
          answer: "是真的，但是用的是通过免费的API接入的基础模型，相比常见的通用聊天机器人，性能可能有些许不足，但是能用就行了"
    design:
      spacing:
        padding: ["4rem", "0", "4rem", "0"]

  - block: cta-card
    content:
      title: "关于作者"
      text: 本人是一名社科出身的机器学习在读研究生，有关本人的更多资料，可以点击下方按钮来进入我的个人网站参观
      button:
        text: "联系作者"
        url: "https://tenzindann.github.io/"
    design:
      card:
        css_class: "bg-gradient-to-r from-primary-200 to-primary-300 dark:from-primary-800 dark:to-primary-900"
---
