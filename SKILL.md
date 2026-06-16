---
name: amazon-product-intelligence
description: Evaluate Amazon new-product development opportunities from ASINs, Amazon links, product images, or 1-2 product keywords. Use when an Amazon seller needs a complete feasibility report covering product identification, main-image and positioning analysis, market capacity, 24-month trend, Top ASIN competition and health, price structure, seller-country structure, variation structure, sales attribution, profit model, PPC difficulty, VOC review insights, differentiation opportunities, XEWEA/Liccyy brand synergy, AI scoring, and final go/no-go development recommendations.
---

# Amazon Product Intelligence

## Goal

Generate a complete Amazon new-product feasibility report to decide whether a product is worth developing.

Accept any of these inputs:

- Amazon product link
- ASIN
- Product image, including main image or lifestyle image
- 1-2 product keywords

Use Chinese by default unless the user asks for another language.

## Data Handling Rules

- Prefer current, source-backed marketplace data when available. Use Amazon pages, user-provided exports, keyword tools, review data, ad data, fee calculators, or credible third-party research if accessible.
- Clearly label every important number as `已验证`, `估算`, or `假设`.
- If live data is unavailable, still produce a useful first-pass report using directional estimates, scenario ranges, and a missing-data list.
- Never invent precise ASIN metrics, review counts, CPC, seller country, variation count, parent sales, or 24-month sales history as facts. If estimating, say how the estimate was derived.
- For Amazon links or ASINs, identify marketplace, category, price, rating, reviews, image structure, variations, seller/brand, fulfillment method, and visible competitive context.
- For image-only inputs, first identify the likely product, category, buyer, use case, price band, and nearest keyword set, then note the data needed for a full decision.
- For keyword-only inputs, analyze the niche and likely product directions before choosing representative ASINs.
- Separate mature-market strength from entry opportunity. A large market can still be a bad development target if reviews, brands, PPC, price compression, seller concentration, variation complexity, or differentiation barriers are too strong.

## Required Analysis Procedure

1. Normalize the input into a target product, marketplace, category, and keyword set.
2. Build or infer a Top20 competitor set. For exact reports, include ASIN, brand, seller country, fulfillment method, price, rating, review count, launch time, monthly sales, parent ASIN, variation count, and sales share.
3. Estimate market capacity from monthly sales, Top10/Top20 sales, search volume, keyword breadth, and traffic structure.
4. Evaluate trend using 24-month monthly sales, yearly sales for the last 2 years, quarterly sales, CAGR, and seasonality.
5. Analyze listing images and positioning. Pay special attention to main-image composition, visible bundle/value cues, and whether the style resembles strong professional brands such as Klein or Milwaukee.
6. Analyze price structure, seller-country structure, variation structure, and ASIN sales attribution before judging competitive intensity.
7. Build a profit model with all major Amazon costs and PPC assumptions. Use the price-band findings to judge whether the product has enough gross-profit room.
8. Extract VOC from reviews. Prioritize 1-3 star complaint patterns, explicit improvement requests, and unmet needs.
9. Rank differentiation opportunities by practical development value, with function first.
10. Score the opportunity out of 100 and make a direct development decision. Let price compression, OEM concentration, high variation complexity, and weak ASIN sales control affect the competition, profit, ASIN health, and final recommendation.

## Market Classification Rules

Classify the market as one of:

- `蓝海`: modest competition, weak listing quality, low review barriers, visible unmet demand, acceptable PPC, and no severe price compression.
- `浅红海`: demand exists, competition is meaningful, but differentiation or niche entry is still realistic.
- `红海`: high review concentration, expensive CPC, strong incumbent brands, price war signs, little visible differentiation space, or low margin.
- `成熟稳定市场`: demand is steady but growth is limited; only enter with strong cost, channel, brand, or product advantage.
- `品牌垄断市场`: Top ASINs are dominated by recognized brands, review moat is high, and buyers show brand-driven trust behavior.
- `OEM市场`: seller-country concentration is high, China sellers or factory-style listings dominate, price competition is visible, and brand moats are weak.
- `混合市场`: OEM sellers and local/brand sellers both have meaningful share; entry is possible but positioning must be clear.
- `新品窗口市场`: recent ASINs under 6 months are gaining share, Top listings are not fully entrenched, or new use cases/materials/bundles are expanding demand.

## Required Output Structure

### 1. 产品识别模块

- 产品名称
- 类目
- 细分类目
- 使用场景
- 目标用户
- 竞品类型归类：工具 / 家用 / 工业 / DIY / 户外 / 办公 / 其他
- 预估售价区间

### 2. 主图与市场定位分析

- 主图结构解析：展示方式 / 构图逻辑 / 背景 / 尺寸比例 / 套装露出
- 核心卖点表达方式
- 品牌定位：低端 / 中端 / 专业级
- 是否强品牌占位：判断是否接近 Klein、Milwaukee 等强专业品牌风格，并说明原因

### 3. 市场容量分析

- 月销量
- Top10总销量
- Top20总销量
- 搜索量
- 关键词数量
- 核心流量词结构：头部词 / 长尾词占比
- 市场容量结论

### 4. 市场趋势分析

- 近24个月每月销量趋势
- 年销量：近2年
- 季度销量：Q1-Q4
- CAGR年增长率
- 是否存在明显淡旺季
- 季节性波动指数：旺季销量 / 淡季销量
- 市场状态判断：增长 / 稳定 / 衰退

### 5. ASIN竞争与健康度分析

List the Top20 ASINs when data is available. For each ASIN include:

- ASIN
- 品牌
- 卖家国家
- FBA / FBM
- 上架时间
- 月销量
- 星级评分
- Review数量
- 价格
- Parent ASIN
- 变体数量
- 当前ASIN销量占Parent比例
- 主要卖点或定位

Then output:

- Top10平均星级
- Top20平均星级
- Top10平均Review数
- Top20平均Review数
- 新品ASIN占比：上架时间 < 6个月
- 高Review门槛占比：>1000 reviews
- 是否存在老品霸榜
- 是否存在品牌垄断
- 是否存在新品机会窗口

### 6. 利润模型分析

- 建议售价
- 产品成本
- 包装成本
- 亚马逊佣金
- FBA费用
- 头程费用
- PPC广告成本：预估
- 退货损耗
- 最终利润
- 利润率
- 价格带利润空间判断：低价带 / 主流价带 / 高价带
- 关键敏感项：售价 / 成本 / CPC / 转化率 / 退货率 / 价格战风险

If cost data is missing, provide conservative, base, and optimistic scenarios.

### 7. 广告竞争分析

- 核心关键词CPC
- Top竞品广告强度
- 关键词竞争等级：低 / 中 / 高
- 广告可投放性评分：0-100
- 广告进入建议：精准词 / 长尾词 / ASIN投放 / 品牌防守 / 暂缓

### 8. 用户评论与VOC分析

- 1-3星差评Top10原因，含占比
- 4-5星好评Top5原因
- 用户未被满足需求：隐性需求
- 用户明确提出的改进建议
- 产品真实痛点归类：质量 / 功能 / 尺寸 / 兼容 / 安装 / 使用体验 / 包装 / 售后 / 预期不符

### 9. 差异化机会分析

Output by priority. Put function differentiation first unless evidence shows another route is clearly stronger.

#### 功能差异化

- 当前功能缺口
- 可增强方向
- 用户证据或假设
- 供应链难度
- 预计转化或溢价作用

#### 场景差异化

- 新使用场景
- 细分人群
- 对应关键词或内容方向

#### 组合差异化

- 套装升级空间
- SKU扩展方向
- 是否适合多变体或虚拟捆绑

#### 材质差异化

- 材料升级空间
- 成本影响
- 是否能形成可视化卖点

#### 包装差异化

- 收纳 / 工具箱 / 结构优化
- 对转化率、退货率、礼品属性或专业感的提升作用

### 10. 与现有品牌协同性分析（XEWEA/Liccyy）

- 是否可共用流量词
- 是否可共享广告结构
- 是否可做虚拟捆绑
- 是否属于同一用户群
- 品牌扩展适配度：0-100分
- 与 XEWEA 的适配逻辑
- 与 Liccyy 的适配逻辑

If the user has not provided existing product-line details, infer cautiously from brand context and mark the synergy as preliminary.

### 11. AI开发评分系统（100分）

Use this weighting:

- 市场容量：15
- 增长趋势：15
- 利润空间：15
- 竞争强度：10
- ASIN健康度：10
- 用户痛点强度：15
- 差异化空间：10
- 广告难度：10
- 品牌协同性：10

Note: the listed weights total 110. Normalize the final score to 100 while showing the raw dimension scores. Explain the main deductions.

Scoring must incorporate the new structural signals:

- Price compression or no profitable price band lowers `利润空间` and raises `竞争强度`.
- High China/OEM seller concentration with price war signals lowers `竞争强度` unless the user has a clear supply-chain cost advantage.
- Brand-dominated US/EU seller concentration lowers `竞争强度` and `ASIN健康度` if review barriers are high.
- High variation complexity lowers `ASIN健康度` and can lower `利润空间` because inventory risk rises.
- Low current-ASIN sales share inside a parent family lowers the probability that the exact SKU can be a main push SKU.
- A high-profit blank price band, balanced seller mix, low variation complexity, and independent ASIN sales control can raise the final recommendation.

Suggested decision bands:

- 80-100：强烈推荐
- 65-79：可做
- 50-64：谨慎验证
- 0-49：不建议

### 12. 最终开发决策输出

- 是否建议开发：强烈推荐 / 可做 / 不建议
- 推荐切入方式：功能 / 场景 / 组合 / 材质 / 包装
- 推荐售价
- 推荐首批备货量
- 预计月销量
- 预计利润
- 回本周期
- 开发风险说明
- 价格结构风险
- 卖家结构风险
- 变体与库存风险
- 是否适合作为主推SKU
- 下一步验证清单

### 13. 价格结构补充字段

Use this module to strengthen competition, profit, and positioning judgment.

- 当前ASIN售价
- Top20 ASIN售价列表
- 卖家国家：Seller Country
- FBA / FBM 标识
- 价格带分布：低 / 中 / 高
- 主流价格区间：Price Band

Then judge:

- 是否存在利润区间
- 是否存在价格战市场
- 是否存在高利润空白带
- 建议切入价格带：低价走量 / 主流价位 / 高价差异化 / 不建议进入

### 14. 卖家国家结构分析

Use this module to identify whether competition is factory/OEM-led, brand-led, or mixed.

- Top20 ASIN卖家国家分布
- 美国卖家占比
- 中国卖家占比
- 欧洲卖家占比
- 其他国家占比

Then output:

- 市场竞争结构评级：OEM市场 / 混合市场 / 品牌垄断市场
- 结构解释：为什么该卖家国家结构会影响价格、广告、Review门槛和利润
- 进入策略：成本优势进入 / 品牌化进入 / 差异化避开 / 不建议进入

### 15. ASIN变体结构分析

Use this module to judge listing structure complexity and inventory risk.

- 当前ASIN是否为子ASIN
- Parent ASIN识别
- 变体数量：Variation Count
- 变体类型：Size / Color / Kit / Mixed

Then output:

- 变体复杂度评分：低 / 中 / 高
- 库存管理难度评级：低 / 中 / 高
- 变体策略建议：单SKU切入 / 小变体测试 / 套装变体 / 暂不扩展变体

### 16. 销量归属分析

Use this module to decide whether the current ASIN is suitable as a main push SKU.

- 当前ASIN月销量
- Parent ASIN总销量
- 当前ASIN销量占比：ASIN / Parent

Then output ASIN control rating:

- 独立型ASIN：>50%，适合作为主推SKU
- 依赖型ASIN：20-50%，可测试但需确认变体流量分配
- 被动型ASIN：<20%，不宜直接判断为主推SKU，需找出Parent内真正主销变体

Also explain how the sales-attribution result affects:

- 推荐首批备货量
- SKU开发优先级
- 广告投放结构
- 是否适合作为主推SKU

## Integration Rules for Modules 13-16

- Use price structure findings inside Modules 5, 6, 11, and 12.
- Use seller-country structure inside Modules 5, 7, 11, and 12.
- Use variation structure inside Modules 5, 9, 11, 12, and 16.
- Use sales attribution inside Modules 5, 11, and 12.
- If any module 13-16 data is missing, include a `结构数据缺口` note and explain how missing data could change the final decision.

## Minimum Viable Answer

When the available input is incomplete, still produce:

1. Product identification and likely category.
2. A preliminary market and competition judgment.
3. A scenario-based profit estimate.
4. A preliminary price-band, seller-country, variation, and sales-attribution assessment when possible.
5. The most important missing data that could change the decision.
6. A preliminary development decision and validation plan.
