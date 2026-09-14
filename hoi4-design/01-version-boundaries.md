# 版本、DLC 与证据边界

[返回总览](README.md) · [系统地图](00-design-map.md) · [来源索引](02-sources.md)

## 稳定版基线

核对截至 2026-09-13。官方 2026-06-30 说明默认公开版为 **1.19.2**；2026-09-04 工作室更新把 **1.19.3** 列为计划 9 月 17 日发布。因此本套以 1.19.2 的现行机制结构为锚点，不把测试分支或未来方案当稳定版。[^1][^2]

1.19.0 公告发表于 6 月 10 日，正文明确扩展次日发布。为避免混淆，本套区分补丁公告日与正式解锁日，不直接复制社区列表中的日期。[^3]

## 与本项目相关的变化

| 时间／版本 | 变化 | 对拆解的影响 |
| --- | --- | --- |
| 1.11 Barbarossa | 供应系统重做为当前枢纽、干线与末端结构 | 不采用更旧的补给区域模型 |
| 1.15 | 德国历史路线重做进入基础更新 | 不能将关闭 Götterdämmerung 等同旧德国树 |
| 1.17 | 陆海空学说由旧树改为 Grand／Subdoctrine／Mastery | 不沿用“攒经验逐格买满旧树”的概括 |
| 1.19 免费更新 | 新师设计界面、团级支援行、12 种团级支援与特殊部队学说改制 | 不把“五个普通支援槽”当全部编制系统 |
| Thunder at our Gates | Army HQ、HQ 专属支援及技能、相关新子学说 | 将官与保障机构的实体化是本次重要补充 |
| 2026 夏季 Open Beta | 多项实验数值 | 不混入稳定版事实 |
| 2026-09 开发稿 | Industrial Parks 等工业调整 | 仅作未来观察，不作为已发布地方军工模型 |

本表只覆盖所研究的系统，不罗列所有国家内容、外观包、海军和空军扩展。对应依据见补给页、官方改制与扩展说明。[^3][^4][^5][^6][^7][^8]

特殊部队的“新系统框架免费更新”，也不等于各扩展提供的所有特殊部队子学说免费。具体可选项要看相关 DLC；本套主要借鉴组织学习结构，而非购买指南。[^5]

## 四处明确保留的证据限制

**德国旧脚本不能代表当前运行结果。** 已核的固定提交标注 1.6.2；当前 Wiki 德国条目标 1.19，却有可疑的绕过条件表述。现版唯一后续仍待当前脚本与实机确认，详见 [13](modules/13-poland-counterfactual.md)。[^9]

**Wiki 不同页可能不同步。** 部分陆军、军官与科技模组页仍保留旧学说或旧编制叙述。出现冲突时，以明确对应版本的官方变更为主，旧页只用于稳定的结构性概念。

**不把 Wiki 全部数值当算法规格。** 本套不提供号称现版准确的战斗、侦察、研究和补给全公式；存在滞后或冲突的具体系数被排除。实际实现使用原创可配置参数。

**没有本地实机验证。** 资料结论来自官方发布与 Wiki／公开脚本核查；原型范围、古代配置、库存示例和测试矩阵均属于设计建议，不是已经完成的游戏或史实考据。

## 更新维护顺序

先更新稳定版锚点，再复查团级支援、HQ、学说、生产与德国历史链。若新工业模型正式发布，优先重读 [04](modules/04-equipment-and-replenishment.md) 和 [10](modules/10-technology.md)；若国策条件变化，复查 [12 系统分工](modules/12-focus-events-and-ai.md)、[13 波兰案例](modules/13-poland-counterfactual.md)、[14 历史框架](modules/14-history-director.md)、[15 生命周期](modules/15-event-contract.md)与 [16 反事实案例](modules/16-butterfly-cases.md)。

同一机制只指定一个主责模块。其他模块引用它，不各自维护一份完整数值或国策条件，减少跨文档矛盾。

## 来源

[^1]: Paradox Development Studio，[Thunder at our Gates — Patch 1.19.2](https://store.steampowered.com/news/app/394360/view/717908846920599778)，2026-06-30；访问 2026-09-13。
[^2]: Paradox Development Studio，Steam 官方公告列表，[Studio Gold Update — September 2026；Industrial Might & Military Production](https://store.steampowered.com/news/posts/?appids=394360&enddate=1788872885&feed=steam_community_announcements)，2026-09-04／2026-09-08；访问 2026-09-13。
[^3]: Paradox Development Studio，Steam 公告，[Thunder at our Gates — Patch Notes (1.19.0)](https://store.steampowered.com/news/app/394360/view/712277443918955865)，2026-06-10 公告；明确次日发布；访问 2026-09-13。
[^4]: Paradox Development Studio，Steam 公告，[Thunder at our Gates: Ship Captains & Division Designer](https://store.steampowered.com/news/app/394360/view/668366079168348304)，2026-05-21；新增功能以正式补丁交叉确认；访问 2026-09-13。
[^5]: Paradox Development Studio，Jaboth／Zwirbaum，[Thunder at our Gates: Army HQs & Special Forces](https://store.steampowered.com/news/app/394360/view/710025009936993029)，2026-06-03；访问 2026-09-13。
[^6]: Paradox Development Studio，[No Compromise, No Surrender — Patch Notes, Live Stream & Mods!](https://store.steampowered.com/news/app/394360/view/606425106922602562)，2025-11-20；1.17；访问 2026-09-13。
[^7]: HOI4 Community Wiki，补丁转录，[Patch 1.15](https://hoi4.paradoxwikis.com/Patch_1.15)，2024-11-14；访问 2026-09-13。
[^8]: Paradox Community Wiki，[Logistics](https://hoi4.paradoxwikis.com/Logistics)，动态机制页；补给重做始于 1.11；访问 2026-09-13。
[^9]: HOI4 Community Wiki，[German national focus tree: industrial / historical branches](https://hoi4.paradoxwikis.com/German_national_focus_tree:_industrial/_historical_branches#Danzig_or_War)，页面标 1.19；bypass 栏存在待核矛盾；访问 2026-09-13。
