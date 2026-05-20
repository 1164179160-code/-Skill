# blueberry-rental-commerce-style

`blueberry-rental-commerce-style` 是一个面向蓝莓骑行租售商城页面设计的 Agent Skill。

它让 Kiro、Codex 或其他兼容 Agent Skills 的 AI 助手，在生成蓝莓骑行商城、车型列表、车辆详情、预约租车、订单确认、骑行人信息和支付/押金页面时，能够持续沿用蓝莓 Figma 方案里的页面结构、组件节奏、真实车辆素材和租售业务逻辑，而不是产出泛泛的移动端商城模板。

## 它适合谁

这个 Skill 适合这些场景：

- 你在做蓝莓骑行的租车、二手车、自研产品、甄选好物或友商合作页面
- 你希望 AI 使用真实车辆 PNG 素材，而不是线稿车、白底块或粗糙抠图
- 你希望详情页按真实租车决策组织：车型图、价格、配色、尺寸、门店库存、预约日历、保障和 CTA
- 你希望列表页、商品卡、筛选、底部导航、弹层和 Picker 都接近蓝莓线上/设计稿风格
- 你希望快速生成可打开预览的 H5 原型，也能输出结构化 PRD、交互说明或改版建议
- 你希望 AI 在生成前先判断用户场景、租期目标、门店库存、车型选择风险和预约转化路径

## 它能做什么

`blueberry-rental-commerce-style` 给 AI 提供了一套蓝莓租售商城的设计工作流：

- 从用户场景、页面入口、核心任务和转化目标开始分析
- 先确定页面类型、信息层级、首屏重点、主 CTA 和状态模型，再开始画界面
- 按 Figma 抓取的 Blueberry 页面/组件规则生成首页、车型列表、商品卡、详情页、订单页和弹层
- 按 `sku 色值` 设计稿沉淀的车辆 PNG 资产选择适合的车型图
- 区分详情页大图、商品卡封面图、推荐卡图和白底展示图，避免图片白块和车辆裁切
- 支持得物式头部结构参考，但只借商品图、缩略图和变体入口的结构，不复制第三方视觉风格
- 支持租车详情里的配色小图、尺寸说明、门店库存、最近门店、预约日历和底部 CTA
- 覆盖加载、空状态、无库存、不可租、门店缺货、日期不可选、尺寸不适配、预约成功等状态
- 避免泛 AI 页面习惯，例如大渐变、装饰光球、营销式 hero、卡片堆叠、假数据和不自然中文断行

默认输出模式是**独立 HTML/CSS/JS 的交互式 H5 原型**。如果用户明确要求，也可以输出 PRD、用户旅程、交互流程图、Figma 页面策略或设计评审建议。

## 安装

这个仓库的核心安装对象是 `blueberry-rental-commerce-style/` 目录。

```text
https://github.com/1164179160-code/-Skill/tree/main/blueberry-rental-commerce-style
```

| 工具 | 安装方式 |
| --- | --- |
| Kiro | 在 `Agent Steering & Skills` 中从 GitHub 导入上面的 Skill 目录链接 |
| Codex | 将 `blueberry-rental-commerce-style/` 放入 `~/.codex/skills/` |
| 其他 IDE | 将 `SKILL.md` 作为主说明，将 `references/` 作为规则参考目录，将 `assets/` 作为可复用素材目录 |

### Kiro

在 Kiro 中：

1. 打开 `Agent Steering & Skills`
2. 点击 `+`
3. 选择 `Import a skill`
4. 选择 GitHub
5. 粘贴上面的 Skill 目录链接

也可以下载仓库 ZIP 后，把 `blueberry-rental-commerce-style/` 文件夹导入到 Kiro 的自定义 Skill / Rules / Agent 指令目录。

## 使用示例

生成车型列表页：

```text
使用 blueberry-rental-commerce-style 生成蓝莓租车车型列表页，包含品牌筛选、车型分类、价格筛选、精选推荐车和商品卡。
```

生成车辆详情页：

```text
使用 blueberry-rental-commerce-style 生成一版车辆详情页，头部参考得物商品图结构，但整体保持蓝莓风格。预约时间通过点击立即预约后的日历弹层选择。
```

做改版策略：

```text
使用 blueberry-rental-commerce-style 分析现有蓝莓车辆详情页，输出一版按用户租车决策重排的信息层级和交互建议。
```

生成可交互原型：

```text
使用 blueberry-rental-commerce-style 生成可打开预览的 H5 原型，要求配色小图可切换、尺码可选择、预约按钮弹出日期选择。
```

## 工作方式

这个 Skill 使用 progressive disclosure 的结构：`SKILL.md` 只放核心流程、触发说明、输出模式和调度规则，具体页面骨架、组件、素材、交互状态和自检标准放在 `references/` 里，由 AI 在需要时读取。

| 文件或目录 | 作用 |
| --- | --- |
| `blueberry-rental-commerce-style/SKILL.md` | 主工作流、触发规则、输出模式、优先级和最终约束 |
| `blueberry-rental-commerce-style/agents/openai.yaml` | Agent Skills 工具可读取的展示信息 |
| `blueberry-rental-commerce-style/references/request-analysis.md` | 页面生成前的蓝莓租售场景分析 |
| `blueberry-rental-commerce-style/references/page-style-library.md` | 首页、列表、详情、预约、订单等页面级结构库 |
| `blueberry-rental-commerce-style/references/blueberry-fidelity.md` | 高还原页面骨架、尺寸比例和蓝莓识别规则 |
| `blueberry-rental-commerce-style/references/components.md` | 商品卡、筛选、详情选择卡、价格条、底部导航、弹层等组件规则 |
| `blueberry-rental-commerce-style/references/sku-vehicle-assets.md` | 真实 SKU 车辆素材分类、选图优先级和使用建议 |
| `blueberry-rental-commerce-style/references/figma-source-inventory.md` | 蓝莓设计稿和 SKU 设计稿的源文件索引 |
| `blueberry-rental-commerce-style/references/figma-component-scan.md` | Figma 组件扫描后的页面/组件规则 |
| `blueberry-rental-commerce-style/references/visual-quality.md` | 页面视觉锚点、层级、节奏、真实产品感和精致度规则 |
| `blueberry-rental-commerce-style/references/design-correctness.md` | 租售业务场景、用户决策、转化路径和状态正确性检查 |
| `blueberry-rental-commerce-style/references/anti-generic-ai.md` | 避免泛 AI 移动端页面的最终检查 |
| `blueberry-rental-commerce-style/references/review-checklist.md` | 交付前自检清单 |
| `blueberry-rental-commerce-style/assets/images/sku-clean/` | 详情页优先使用的清理后真实车辆 PNG |
| `blueberry-rental-commerce-style/assets/images/composite/` | 商品卡、推荐卡和详情推荐模块使用的合成图 |

## 仓库结构

```text
-Skill/
├── blueberry-rental-commerce-style/
│   ├── SKILL.md
│   ├── agents/
│   │   └── openai.yaml
│   ├── references/
│   └── assets/
├── blueberry-rental-commerce-style-kiro.zip
├── blueberry-rental-commerce-style.zip
└── README.md
```

真正被安装到 Kiro 或 Codex 的是 `blueberry-rental-commerce-style/` 这个目录。

## 更新

更新 GitHub 仓库后，在 Kiro 重新导入 GitHub Skill，或重新下载 ZIP 并替换本地 `blueberry-rental-commerce-style/` 文件夹即可。

## 要求

- Kiro、Codex，或其他兼容 Agent Skills 的工具
- 生成页面时建议明确写 `使用 blueberry-rental-commerce-style`

