# Kiro 安装说明

这是基于 Figma「蓝莓风格抓取」整理的 Blueberry 租售商城风格 Skill。

## 目录内容

- `SKILL.md`：Skill 主入口和触发说明
- `references/style-rules.md`：视觉风格、颜色、字体、间距、图片规则
- `references/blueberry-fidelity.md`：首页、列表、详情、订单等页面骨架和高保真约束
- `references/figma-source-inventory.md`：两个 Figma 源的完整索引，区分页面/组件源和车型素材源
- `references/figma-component-scan.md`：蓝莓详情页、筛选、Picker、弹窗等组件扫描规则
- `references/high-fidelity-generation.md`：高还原生成流程、页面类型规则、资产优先级和自检标准
- `references/components.md`：Banner、推荐入口、产品卡、分类 tab、底部导航、弹层等组件规则
- `references/interaction-states.md`：浏览、筛选、选车、骑行人、支付/押金等状态
- `references/copywriting.md`：蓝莓租售场景常用文案
- `references/assets.md`：本地车型 SVG 资产索引
- `references/sku-vehicle-assets.md`：从「sku 色值」设计稿提取的真实 SKU 车型图分类
- `references/vehicle-assets-classification.md`：设计稿车辆图片分类和使用建议
- `assets/images/sku-clean/`：去白底并处理边缘白边后的真实 SKU 车型 PNG，详情页大图优先使用
- `assets/images/sku-transparent/`：第一版去白底 SKU PNG，作为中间资产保留
- `assets/images/sku/`：从设计稿导出的原始真实 SKU PNG，用于归档和比对
- `assets/images/`：历史 Figma 截图、商品卡图和 SVG fallback 图片
- `agents/openai.yaml`：agent 元信息

## 当前版本重点

- 详情页支持蓝莓原生结构和「得物式头部结构参考」两种方向，但只借结构，不借第三方视觉风格
- 颜色/配色优先使用车辆小图预览，纯色点只作为兜底
- 如果头部已有车辆缩略图选择，详情页选择卡里不能重复再放一组颜色卡
- 线上预约流程为点击 `预约/立即预约` 后用日历选择租车时间，详情页不提前放 `日租/时租` 选择卡
- 紧凑卡片不允许出现中文单字断行或尴尬换行，例如 `保 障`、`骑 行`、`灵 活`
- 车辆详情页应让用户先确认配色、尺寸、门店库存，再进入预约日历

## 安装方式

1. 解压 `blueberry-rental-commerce-style-kiro.zip`
2. 将整个 `blueberry-rental-commerce-style` 文件夹放到 Kiro 的自定义 Skill / Rules / Agent 指令目录
3. 在 Kiro 中启用或引用该 Skill
4. 后续生成页面时，在需求里明确写：

```text
使用 blueberry-rental-commerce-style 风格生成页面
```

## 推荐使用场景

- 蓝莓骑行首页
- 车型租售商城
- 车辆列表 / 甄选好物
- 车辆详情页 / 得物式头部详情页
- 推荐入口/分类页
- 产品卡片列表
- 租车确认页
- 骑行人信息弹层
- 支付/押金确认页
- 底部 Liquid Glass 导航页面

## 风格关键词

白底、浅灰、产品摄影、圆角白卡、黑色胶囊按钮、横向滑动推荐、轻奢租售、Liquid Glass 底部导航。
