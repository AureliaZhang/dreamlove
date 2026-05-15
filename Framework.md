# Lia Design System · Framework

> 雾霾蓝设计系统 — 面向城市规划 (Urban Planning) × 人机交互 (HCI)

---

## 目录

- [设计理念](#设计理念)
- [文件结构](#文件结构)
- [色彩系统](#色彩系统)
- [排版规范](#排版规范)
- [间距与圆角](#间距与圆角)
- [动效系统](#动效系统)
- [组件库](#组件库)
- [城市规划组件](#城市规划组件)
- [HCI 交互模式](#hci-交互模式)
- [图标库](#图标库)
- [背景效果](#背景效果)
- [响应式断点](#响应式断点)
- [雾中酒馆 Tavern](#雾中酒馆-tavern)
- [互动剧情小说三部曲](#互动剧情小说三部曲)

---

## 设计理念

**Lia** 是一套面向城市规划与人机交互领域的个人设计系统。

- **主色调**：黑白灰 + 雾霾蓝 (`#6b8ca4`) 作为温柔底色
- **强调色**：洋红 (`#e91e8c`) 仅用于关键交互元素（主按钮、关键操作）
- **状态色**：Sasaki 风格低饱和土色调（鼠尾草绿、赭石、赤陶）
- **风格**：克制、冷静、不失温度

---

## 文件结构

```
/app/style/
├── Framework.md          ← 本文件
├── demo.html             ← 组件库演示（最完整）
├── design-demo.html      ← 设计规范文档
├── index.html            ← 图标库
├── refstyle/             ← 原始参考文件（只读）
└── tavern/               ← 雾中酒馆 · AI 聊天 + 翻译
    ├── tavern.html
    └── stories/          ← 互动剧情小说三部曲
        ├── 01-cultivation/  ← 九州问道（修仙）
        ├── 02-court/        ← 荆棘王冠（宫廷）
        └── 03-xianxia/      ← 六界浮生（仙侠）
```

| 文件 | 内容 | 大小 |
|------|------|------|
| `demo.html` | 色彩、排版、组件、城市规划、HCI、模式、响应式 | ~90KB |
| `design-demo.html` | 色彩、排版、布局、空间设计、交互设计、组件、模式、响应式 | ~75KB |
| `index.html` | 8 类 96 个 SVG 图标 + 清单表 | ~78KB |
| `tavern/tavern.html` | 酒馆风格 AI 聊天 + 多对话管理 + RAG 知识库 + 角色日记 + 对话摘要 + 每日日记 + 欧路词典翻译 + 离线词典选词 + CODEC 双向编码 + 互动剧情小说 | ~190KB |
| `tavern/stories/` | 三部互动剧情小说（修仙/宫廷/仙侠），每部 ~10 万字，含 18+ 感情线 | ~940KB |

所有文件均为**单文件 HTML**（CSS + HTML + JS 内联），可直接双击打开。

---

## 色彩系统

### 底色层级

| Token | 值 | 用途 |
|-------|-----|------|
| `--bg-primary` | `#eef1f5` | 页面底色 |
| `--bg-secondary` | `#e0e5eb` | 次级背景 |
| `--bg-tertiary` | `#f5f7fa` | 三级背景 |
| `--bg-card` | `#f8f9fc` | 卡片背景 |
| `--bg-input` | `#eef1f5` | 输入框背景 |
| `--bg-code` | `#e4e8ee` | 代码块背景 |

### 结构线

| Token | 值 | 用途 |
|-------|-----|------|
| `--border` | `#c4ccd6` | 默认边框 |
| `--border-hover` | `#98a5b5` | 悬停边框 |
| `--border-strong` | `#6b7a8d` | 强调边框 |
| `--rule` | `#d4dbe4` | 分割线 |
| `--rule-light` | `#e4e9f0` | 轻分割线 |

### 文字阶序

| Token | 值 | 用途 |
|-------|-----|------|
| `--text-primary` | `#1e2a3a` | 主文字 |
| `--text-secondary` | `#5a6876` | 次级文字 |
| `--text-tertiary` | `#8a95a2` | 辅助文字 |
| `--text-disabled` | `#b5bcc5` | 禁用文字 |

### 强调色

| Token | 值 | 用途 |
|-------|-----|------|
| `--accent` | `#e91e8c` | 洋红 — 仅限主按钮 |
| `--accent-hover` | `#c41777` | 洋红悬停 |
| `--accent-light` | `#fdf2f9` | 洋红浅底 |
| `--amber` | `#6b8ca4` | 雾霾蓝 — 通用强调 |
| `--amber-hover` | `#5a7a92` | 雾霾蓝悬停 |
| `--amber-light` | `#edf3f8` | 雾霾蓝浅底 |

### 状态色（Sasaki 风格低饱和）

| Token | 值 | 用途 |
|-------|-----|------|
| `--success` | `#6a8a6e` | 鼠尾草绿 — 成功 |
| `--warning` | `#a68a5a` | 赭石 — 警告 |
| `--error` | `#a86a6a` | 赤陶 — 错误 |

### 用地分类色（GB 50137）

| Token | 值 | 对应用地 |
|-------|-----|----------|
| `--zone-residential` | `#7ba7c2` | R 居住用地 |
| `--zone-commercial` | `#c4a46b` | B 商业服务业 |
| `--zone-industrial` | `#8a8a8a` | M 工业用地 |
| `--zone-green` | `#5a9a6a` | G 绿地广场 |
| `--zone-mixed` | `#a47bc4` | 混合用地 |
| `--zone-water` | `#6b9ac4` | E1 水域 |
| `--zone-road` | `#d4dbe4` | S 道路交通 |

### 六线控制色

| Token | 值 | 含义 |
|-------|-----|------|
| `--line-red` | `#c45a5a` | 道路红线 |
| `--line-green` | `#5a9a6a` | 城市绿线 |
| `--line-blue` | `#5a7ac4` | 城市蓝线 |
| `--line-purple` | `#8a5aaa` | 城市紫线 |
| `--line-yellow` | `#b4a44a` | 城市黄线 |
| `--line-eco` | `#c45a5a` | 生态红线 |

### 热力图色阶

| Token | 值 |
|-------|-----|
| `--heat-low` | `#eef1f5` |
| `--heat-mid` | `#6b8ca4` |
| `--heat-high` | `#e91e8c` |

---

## 排版规范

### 字体栈

| 用途 | 字体 |
|------|------|
| 正文 | `'Noto Sans SC', system-ui, -apple-system, sans-serif` |
| 标题 | `'Noto Serif SC', serif` |
| 代码 | `'JetBrains Mono', monospace` |
| 辅助代码 | `'IBM Plex Mono', monospace` |

### 字号阶梯

| Token | 值 | 用途 |
|-------|-----|------|
| `--text-xs` | `11px` | 标签、角标 |
| `--text-sm` | `12px` | 辅助文字 |
| `--text-base` | `14px` | 正文 |
| `--text-md` | `15px` | 中号正文 |
| `--text-lg` | `18px` | 小标题 |
| `--text-xl` | `20px` | 数字展示 |
| `--text-2xl` | `28px` | 段落标题 |
| `--text-3xl` | `36px` | 页面大标题 |

---

## 间距与圆角

### 间距模数（4px 基准）

| Token | 值 |
|-------|-----|
| `--sp-1` | `4px` |
| `--sp-2` | `8px` |
| `--sp-3` | `12px` |
| `--sp-4` | `16px` |
| `--sp-5` | `20px` |
| `--sp-6` | `24px` |
| `--sp-8` | `32px` |
| `--sp-10` | `40px` |
| `--sp-12` | `48px` |
| `--sp-16` | `64px` |

### 圆角

| Token | 值 | 用途 |
|-------|-----|------|
| `--radius-sm` | `4px` | 小元素（badge、input） |
| `--radius-md` | `6px` | 卡片、按钮 |
| `--radius-lg` | `8px` | 大卡片、模态框 |

### 阴影

| Token | 值 | 用途 |
|-------|-----|------|
| `--shadow-soft` | `0 1px 2px rgba(30,42,58,0.06)` | 轻阴影 |
| `--shadow-float` | `0 4px 6px rgba(30,42,58,0.08)` | 浮动阴影 |

---

## 动效系统

| Token | 值 | 用途 |
|-------|-----|------|
| `--ease-out` | `cubic-bezier(0.16, 1, 0.3, 1)` | 缓出曲线 |
| `--duration-fast` | `120ms` | 微交互（hover、focus） |
| `--duration-normal` | `200ms` | 常规过渡 |

### 柔和磁吸

滚动停止 150ms 后，若距段落顶部 < 80px，以 400ms `ease-out` 缓动吸合。

---

## 组件库

### 按钮 Buttons

| 类名 | 说明 |
|------|------|
| `.btn` | 基础按钮 |
| `.btn-primary` | 洋红主按钮 |
| `.btn-secondary` | 雾霾蓝次按钮 |
| `.btn-ghost` | 透明幽灵按钮 |
| `.btn-danger` | 危险按钮 |
| `.btn-sm` / `.btn-lg` | 尺寸变体 |
| `.btn-group` | 按钮组 |

### 徽章 Badges

| 类名 | 说明 |
|------|------|
| `.badge` | 基础徽章 |
| `.badge-accent` | 洋红强调 |
| `.badge-amber` | 雾霾蓝 |
| `.badge-success` / `.badge-warning` / `.badge-error` | 状态色 |
| `.badge-dot` | 带圆点徽章 |

### 卡片 Cards

| 类名 | 说明 |
|------|------|
| `.card` | 基础卡片 |
| `.card-header` / `.card-body` / `.card-footer` | 卡片区域 |
| `.card-title` / `.card-text` | 卡片文字 |
| `.cards-grid` | 卡片网格 |

### 表单 Forms

| 类名 | 说明 |
|------|------|
| `.input` | 文本输入框 |
| `.textarea` | 多行文本 |
| `.select` / `.select-wrap` | 下拉选择 |
| `.toggle-switch` | 开关 |

### 标签页 Tabs

| 类名 | 说明 |
|------|------|
| `.tabs-bar` | 标签栏容器 |
| `.tab-item` | 标签项 |

### 表格 Tables

| 类名 | 说明 |
|------|------|
| `.data-table` | 数据表格 |
| `.data-table-wrap` | 表格外层（可滚动） |
| `.table-mono` | 等宽字体表格 |

### 模态框 Modal

| 类名 | 说明 |
|------|------|
| `.modal-overlay` | 遮罩层 |
| `.modal` | 模态框容器 |
| `.modal-header` / `.modal-body` / `.modal-footer` | 模态框区域 |
| `.modal-title` / `.modal-close` | 标题与关闭按钮 |

### 提示 Toast

| 类名 | 说明 |
|------|------|
| `.toast-container` | 提示容器 |
| `.toast` | 基础提示 |
| `.toast-success` / `.toast-warning` / `.toast-error` | 状态提示 |

### 空状态 Empty State

| 类名 | 说明 |
|------|------|
| `.empty-state` | 空状态容器 |
| `.empty-state-icon` / `.empty-state-title` / `.empty-state-desc` | 空状态元素 |

---

## 城市规划组件

### 项目概况卡片 `.project-card`

展示城市设计/规划项目的核心信息：项目名称、状态标签、用地面积、容积率、绿化率、建筑密度。

### 用地分析图例 `.zoning-legend`

基于 GB 50137-2011 的用地分类色块图例，使用 `--zone-*` 色彩变量。

### 时间轴 `.timeline`

规划项目阶段时间轴：现状调研 → 概念方案 → 深化设计 → 评审汇报 → 实施导则。

### 指标仪表盘 `.metric-card`

城市规划关键指标卡片：人口密度、绿地覆盖率、步行可达性、公共交通覆盖率。带进度条可视化。

### 方案比选表 `.data-table`

多方案横向对比表格：方案 A / B / C 的密度、绿地率、容积率、限高等控制指标对比。

### 用户画像 `.persona-card`

城市规划师/设计师用户画像卡片：头像、姓名、角色、目标 (GOALS)、痛点 (PAIN POINTS)。

### 可用性指标 `.metric-card`

HCI 可用性指标：SUS 评分、任务完成率、操作时长、错误率。

### A/B 测试卡片 `.ab-card`

变体对比卡片：展示 A/B 方案的置信区间与差异。

### WCAG 合规徽章 `.wcag-badge`

无障碍合规等级标识：A / AA / AAA。

---

## HCI 交互模式

### 交互状态矩阵

所有组件遵循统一的状态定义：

| 状态 | 说明 |
|------|------|
| Default | 默认状态 |
| Hover | 鼠标悬停 |
| Focus | 键盘聚焦（`focus-visible`） |
| Active | 按下激活 |
| Disabled | 禁用 |
| Loading | 加载中 |

### 焦点环规范

```css
:focus-visible {
  outline: 2px solid var(--amber);
  outline-offset: 2px;
}
```

### 触控目标

最小触控区域 44×44px（WCAG 2.5.5）。

---

## 图标库

`index.html` 包含 8 个分类、96 个 SVG 图标。

### 分类

| 目录 | 名称 | 数量 |
|------|------|------|
| `navigation/` | 导航 | 12 |
| `action/` | 操作 | 12 |
| `status/` | 状态 | 12 |
| `data/` | 数据 | 12 |
| `communication/` | 沟通 | 12 |
| `urban/` | 城市规划 | 12 |
| `hci/` | 人机交互 | 12 |

### 图标规范

- 视口：`viewBox="0 0 24 24"`
- 描边：`stroke="currentColor"` `stroke-width="1.8"`
- 端点：`stroke-linecap="round"` `stroke-linejoin="round"`
- 格式：描边式 SVG，无填充

### 城市规划图标 (`urban/`)

| 文件名 | 说明 |
|--------|------|
| `parcel.svg` | 用地地块 |
| `far.svg` | 容积率 |
| `setback.svg` | 建筑退界 |
| `height-limit.svg` | 建筑限高 |
| `road-redline.svg` | 道路红线 |
| `green-line.svg` | 城市绿线 |
| `blue-line.svg` | 城市蓝线 |
| `metro.svg` | 轨道交通 |
| `eco-corridor.svg` | 生态廊道 |
| `wind-rose.svg` | 风玫瑰图 |
| `sunlight.svg` | 日照分析 |
| `mixed-use.svg` | 混合用地 |

### HCI 图标 (`hci/`)

| 文件名 | 说明 |
|--------|------|
| `cursor.svg` | 光标 |
| `hand-gesture.svg` | 手势 |
| `touch.svg` | 触控 |
| `drag.svg` | 拖拽 |
| `pinch.svg` | 缩放 |
| `swipe.svg` | 滑动 |
| `accessibility.svg` | 无障碍 |
| `interaction.svg` | 交互 |
| `prototype.svg` | 原型 |
| `persona.svg` | 用户画像 |
| `feedback.svg` | 反馈 |
| `flow.svg` | 流程 |

---

## 背景效果

### 粒子背景

所有页面使用 canvas 动态粒子背景：

- 60 个雾霾蓝色调粒子缓慢漂浮
- 粒子间距 < 120px 时自动连线（星座效果）
- 固定定位，`z-index: -1`，不影响内容交互
- 窗口缩放自动适配

### 磨砂玻璃

关键 UI 元素使用 Apple 风格磨砂玻璃：

```css
background: rgba(245,247,250,0.72);
backdrop-filter: saturate(180%) blur(20px);
-webkit-backdrop-filter: saturate(180%) blur(20px);
```

应用于：Header、卡片、模态框、Toast、表格容器。

---

## 响应式断点

| 断点 | 宽度 | 说明 |
|------|------|------|
| Mobile | `< 480px` | 单列布局，隐藏导航 |
| Tablet | `480px – 768px` | 两列网格，简化布局 |
| Desktop | `> 768px` | 完整布局 |
| Wide | `> 1024px` | 宽屏优化 |

### 响应式行为

- 导航栏：< 768px 隐藏
- 卡片网格：< 768px 单列，768px+ 自适应
- 表格：< 768px 水平滚动
- 间距：< 768px 缩小段落内边距

---

## 雾中酒馆 Tavern

`tavern/tavern.html` — 单文件 AI 聊天应用，SillyTavern 布局 + Lia 配色。

### 功能模块

| 模块 | 说明 |
|------|------|
| AI 聊天 | OpenAI 兼容 + Anthropic 原生 API，自动检测格式 |
| 多对话管理 | 新建/切换/删除对话，每个对话独立消息历史 |
| RAG 知识库 | 故事内容分块索引，关键词检索，自动注入相关背景到 system prompt |
| 角色记忆 | 角色级记忆，按对话归属，支持清除全部记忆 |
| 角色日记 | 提取当天出场角色，生成第一人称视角日记 |
| 对话摘要 | 对话超过 10 条时自动摘要，减少 token 消耗 |
| 每日日记 | 23:00 北京时间自动生成当日日记 |
| 翻译面板 | 右侧欧路词典风格：查词、音标、释义、生词本 |
| 离线词典 | 内置 ~350 词，覆盖基础词汇 + 酒馆主题词 |
| 选词查询 | 鼠标选中消息文本弹出查词/翻译气泡 |
| CODEC 双向编码 | 敏感词 ↔ 文学化编码互转，独立可复用模块 |
| 互动剧情小说 | 三部 10 万字级互动小说，角色扮演模式（AI 演角色，非写小说） |

### API 双格式兼容

`callChatAPI()` 统一函数自动检测 API 格式：

| 检测条件 | 格式 | 端点 | 认证方式 |
|----------|------|------|----------|
| URL 含 `anthropic` | Anthropic 原生 | `/v1/messages` | `x-api-key` header |
| 其他 | OpenAI 兼容 | `/v1/chat/completions` | `Authorization: Bearer` |

- Anthropic 格式：`system` 提取为顶层字段，响应取 `content[].text`
- OpenAI 格式：`system` 在 messages 数组中，响应取 `choices[0].message.content`
- 所有 API 调用点（聊天、翻译、摘要、日记）统一走 `callChatAPI()`

### CODEC 分级双向编码系统

独立可复用模块，支持 0-100 分级控制的文本编解码。

**级别定义**：

| 级别 | 名称 | 效果 |
|------|------|------|
| 0 | 🤍 纯爱 | 拥抱亲吻即止，朦胧唯美 |
| 25 | 💗 暧昧 | 暗示性张力，点到为止 |
| 50 | 💖 微露 | 部分身体描写，文学化 |
| 75 | ❤️‍🔥 直白 | 完整身体描写，情欲张力 |
| 100 | 🔥 全开 | 乙女级别，不加掩饰 |

**原理**：
- AI 始终生成编码词（如「玉峰」「覆唇」「律动」）
- `CODEC.decode(text)` 根据当前级别将编码词转换为对应显示文本
- `CODEC.getPromptAddon()` 动态生成系统提示，控制 AI 输出的内容风格和编码词列表
- 级别 0 时 AI 收到纯爱指令，级别 100 时 AI 收到全开指令 + 完整编码词表

**映射格式**：`{ c:编码词, l0:纯爱, l25:暧昧, l50:微露, l75:直白, l100:全开, cat:分类 }`

**API**：
- `CODEC.decode(text)` — 按当前级别解码
- `CODEC.getLevel()` / `setLevel(n)` — 获取/设置级别
- `CODEC.getPromptAddon()` — 获取系统提示附加内容
- `CODEC.addMapping(m)` / `removeMapping(idx)` — 管理映射
- `CODEC.exportJSON()` / `importJSON(str)` — 导入导出

**集成**：
- `sendMsg()` 中系统提示自动注入 `CODEC.getPromptAddon()`
- `addMsg()` 中 AI 回复自动经过 `CODEC.decode()` 处理
- 所有对话和故事模式均生效

**UI**：侧栏「编码系统」按钮 → 管理面板，含级别滑块、搜索、分类筛选、添加/删除、导入导出、测试解码。

**复用**：可直接复制 `CODEC` IIFE 模块到其他项目。

### 角色扮演模式

所有互动小说采用 SillyTavern 风格角色扮演：AI 演角色本身，不是写小说。

**核心原则**：
- AI 是角色本人，不是旁白或叙述者
- 回复风格：自然对话 + 简短动作描写，像真人聊天
- 严禁代替玩家（【你】）说话、行动或思考
- 每次回复 300-800 字，精炼有信息量

**格式规则**：
- 单角色场景：`【角色名】对话+动作`
- 多角色场景：按角色分段，各角色交替说话
- 玩家（【你】）：只用客观外在描写，不代写台词或内心

**示例（正确）**：
```
【云无涯】我靠在药园门口，看着她蹲在地上摆弄那株清心草。"……别碰那株。"我开口提醒，"有毒。"
【苏子衿】我笑着走过来，从她手里接过清心草。"云师兄说得对，这株要戴手套才能碰。"
```

**示例（错误）**：
```
"在那阳光明媚的午后，药园中弥漫着淡淡的药香。云无涯静静站在门口，心中泛起了一丝说不清的情绪……"
← 这是写小说，不是角色扮演。
```

### RAG 向量知识库

浏览器端轻量级关键词索引系统，将故事内容分块存储，自动检索相关背景。

**原理**：
- 故事 .md 文件按 `##` 标题分块存储在 `st_rag`
- 每个 chunk 提取关键词（角色名、地名、事件）
- `sendMsg()` 时根据用户消息匹配相关 chunks，注入 system prompt

**数据结构**：
```js
st_rag = {
  cultivation: [
    { id: 'ch00_s1', title: '序章·凡尘旧梦', content: '...', keywords: ['青石镇','李婆婆'] }
  ]
}
```

**注入位置**：system prompt 末尾，`CODEC.getPromptAddon()` 之前

### 角色日记系统

提取当天出场角色，调用 API 生成第一人称视角日记。

**流程**：
1. AI 回复后提取文中出现的角色名
2. 调用 API 为每个出场角色生成日记
3. 日记以特殊样式显示（`.msg-group.diary`）

**日记 Prompt**：
```
你是{角色名}，请以第一人称写一篇简短日记（100-200字），记录今天与女主的互动，
包含你的真实想法和情感。直接写内容，不加标题。
```

**存储**：`st_char_diary = { "2026-05-14": { "云无涯": "今天在练武场...", "苏子衿": "..." } }`

### 对话摘要系统

对话超过 10 条时，自动压缩为摘要发送，减少 token 消耗。

**逻辑**：
- 对话 ≤ 10 条：直接发送完整历史（当前逻辑）
- 对话 > 10 条：发送 `摘要 + 最近 5 条消息`
- 摘要存储在 `st_summary`，按对话 ID 索引

**摘要 Prompt**：
```
请将以下对话总结为简洁的剧情摘要，包含：当前场景、角色状态、关键事件、
未完成的选择。200字以内。
```

**Token 节省**：预计减少 60-80% 的 token 消耗（长对话场景）

### 数据模型（localStorage，前缀 `st_`）

| Key | 类型 | 说明 |
|-----|------|------|
| `st_cfg` | Object | API 配置（url、key、model、persona） |
| `st_convs` | Array | 对话列表 `[{id, title, messages, createdAt}]` |
| `st_currentConv` | String | 当前对话 ID |
| `st_mem` | Array | 记忆 `[{type, content, date, convId}]` |
| `st_diary` | Object | 日记 `{日期: 内容}` |
| `st_char_diary` | Object | 角色日记 `{日期: {角色名: 日记内容}}` |
| `st_summary` | Object | 对话摘要 `{convId: 摘要文本}` |
| `st_rag` | Object | RAG 知识库 `{storyKey: [{id, title, content, keywords}]}` |
| `st_thist` | Array | 翻译历史 |
| `st_vocab` | Array | 生词本 |
| `st_codec` | Object | CODEC 配置 `{mappings: [{c,l0,l25,l50,l75,l100,cat}], level: 0-100}` |
| `st_story` | String | 当前故事 key（cultivation/court/xianxia/空） |

### 响应式

| 断点 | 行为 |
|------|------|
| ≥ 900px | 三栏布局：侧栏 260px + 聊天 flex:1 + 翻译 340px |
| < 900px | 侧栏抽屉 + 翻译全屏覆盖 + 移动端适配 |

**移动端视口修复**：使用 JS 计算 `window.innerHeight` 设置 `--app-height` CSS 变量，解决 `100vh` 在移动浏览器中包含地址栏/底部导航栏导致内容溢出的问题。监听 `resize` 和 `orientationchange` 事件动态更新。

---

## 互动剧情小说三部曲

`tavern/stories/` 内含三部大世界观互动小说，女主可攻略任意角色，结局由选择决定。

### 通用设定

- **女主体质**：万缘体质——天生亲和之力，所有角色初始好感为「友善」
- **交互模式**：关键节点给选项 + 日常自由对话（混合模式）
- **女主名字**：玩家自取
- **叙事视角**：【姓名】+ 第一人称视角，多角色场景按角色分段叙述
- **RAG 知识库**：故事内容分块索引，自动检索相关背景注入对话
- **角色日记**：每天生成出场角色的第一人称视角日记
- **对话摘要**：长对话自动压缩为摘要，节省 token

### 三部小说

| # | 名称 | 世界观 | 角色数 | 章节数 |
|---|------|--------|--------|--------|
| 1 | **九州问道** | 古代修仙·九州大陆 | 12人（6男6女） | 序章+7章+番外 |
| 2 | **荆棘王冠** | 西方宫廷·艾瑟兰王国 | 12人（6男6女） | 序章+7章+番外 |
| 3 | **六界浮生** | 仙侠世界·六界并立 | 12人（6男6女） | 序章+7章+番外 |

### 文件结构

```
stories/
├── README.md              ← 三部小说总览
├── 01-cultivation/        ← 古代修仙 · 九州问道
│   ├── world.md           ← 世界观设定
│   ├── characters.md      ← 角色档案（12人）
│   ├── ch00.md ~ ch08.md  ← 各章正文（~10万字）
│   └── routes.md          ← 攻略路线图
├── 02-court/              ← 西方宫廷 · 荆棘王冠
│   ├── world.md / characters.md / ch00~ch08 / routes.md
└── 03-xianxia/            ← 仙侠世界 · 六界浮生
    ├── world.md / characters.md / ch00~ch08 / routes.md
```

---

## 快速开始

1. 双击打开任意 `.html` 文件即可预览
2. 所有设计令牌通过 CSS 自定义属性定义在 `:root`
3. 组件样式内联在 `<style>` 标签中
4. 交互逻辑内联在 `<script>` 标签中
5. 图标点击即可复制 SVG 代码

---

*Lia Design System v1.0 · 雾霾蓝 · 城市规划 × HCI*
