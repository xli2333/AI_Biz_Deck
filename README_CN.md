# Strategy.AI Deck Builder

[English Version](README.md)

**Strategy.AI** 是一个基于 React 和 Google Gemini 3.0 Pro 模型的智能商业 PPT 生成引擎。它能够模拟顶级咨询公司（McKinsey, BCG, Bain）的逻辑框架和视觉风格，自动将你的文档或简短想法转化为专业的战略演示文稿。

![Project Banner](banner.png)

## 最新功能

### 自定义咨询风格
不再局限于预设的三大咨询公司！
- **AI 反向工程**: 上传任何你喜欢的 PDF 报告或图片，或者输入一段风格描述（例如“赛博朋克极简风”、“专业投行风格”）。
- **风格提取**: Gemini 3.0 Pro 会自动分析并提取其 **逻辑架构** 和 **视觉 DNA**。
- **即时应用**: 生成的自定义风格将直接应用于后续的所有幻灯片生成，从配色到叙事逻辑完全定制。

### NotebookLM 幻灯片一键 4K 化
专为 NotebookLM 用户打造的视觉增强工作流。
- **无缝导入**: 直接支持导入 Google NotebookLM 生成的简陋 PDF 幻灯片。
- **智能重绘**: AI 识别原有内容结构，保留核心信息。
- **4K 增强**: 使用 `gemini-3-pro-image-preview` 模型将原本模糊、简单的图表一键重绘为 4K 超高清、专业设计风格的商业图表。

---

## 核心功能

本项目不仅仅是一个“PPT生成器”，它是一个模拟咨询顾问思考过程的 AI 代理系统。

### 1. 智能情境分析
- **多模态输入**: 支持上传 PDF, TXT, MD, DOC, DOCX 文档，或者直接输入你的核心目标（Purpose）。
- **逻辑解构**: 内置 SCQA (Situation, Complication, Question, Answer) 框架，AI 会像分析师一样拆解你的输入，提取关键战略信息。

### 2. 顶级咨询风格定制
系统内置了三大顶级咨询公司的“思维与视觉”预设：
- **McKinsey (麦肯锡风格)**: 金字塔原理，MECE 原则，经典蓝系。
- **BCG (波士顿咨询风格)**: 增长/份额矩阵，强调洞察，标志性绿系。
- **Bain (贝恩风格)**: 结果导向，数据严谨，红色强调 (Cardinal Red)。

### 3. 高级生成工作流
- **幽灵甲板 (Ghost Deck)**: 先生成纯文字逻辑大纲，确认叙事结构。
- **分步构建**: 蓝图 (Blueprint) -> 渲染 (Render)。
- **实时控制**: 支持 **暂停/恢复** 生成过程，随时干预。

### 4. 深度编辑与细化
- **全局重构 (Director's Cut)**: 一句话重写整个大纲逻辑。
- **单页精修 (Slide Refine)**: 针对单张幻灯片进行逻辑重写。
- **视觉微调 (Visual Edit)**: 自然语言修改图片细节。
- **历史回溯 (Undo/History)**: 完整的版本控制。

### 5. 输出与导出
- **4K Upscaling**: 无损放大至 4K 超高清。
- **PDF 导出**: 一键合成高分辨率 PDF。

## 技术栈

- **前端框架**: React 19, Vite, TypeScript
- **UI 组件**: Tailwind CSS (v3.4), Lucide React
- **AI 核心**: Google Gemini API (gemini-3-pro-preview / gemini-3-pro-image-preview)
- **文档处理**: `jspdf`, `pdfjs-dist`

## 快速开始

### 前置要求
- Node.js (v18+)
- 有效的 **Google Gemini API Key** (必须以 `AIza` 开头)。

### 本地运行

1.  **克隆项目**
    ```bash
    git clone https://github.com/xli2333/AI_Biz_Deck.git
    cd AI_Biz_Deck
    ```

2.  **安装依赖**
    ```bash
    npm install
    ```

3.  **启动开发服务器**
    ```bash
    npm run dev
    ```

4.  **访问应用**
    打开浏览器访问 `http://localhost:3000`。

### 部署

本项目完全适配 **Vercel** 部署。
1.  在 Vercel 中 Import Project。
2.  **重要**：将 **Root Directory** 设置为 `AIDECK V1`。
3.  点击 Deploy。无需配置环境变量，API Key 由前端输入。

## 使用指南

1.  **输入密钥**: 首页输入 Gemini API Key。
2.  **提供上下文**: 上传文档或输入目的。
3.  **选择风格**: 
    - 选择经典风格 (McKinsey/BCG/Bain)。
    - 或点击 **Custom** 上传一张你喜欢的 PPT 图片，AI 会自动模仿其风格。
    - 或点击 **Visual Engine** 导入 NotebookLM PDF 进行 4K 重绘。
4.  **生成与微调**: 生成大纲 -> 构建 Deck -> 细节微调。
5.  **导出**: 点击 "Upscale (4K)" -> "Export PDF"。

## License

MIT
