# 12 国策、事件、决议与历史 AI 的分工

[返回总览](../README.md) · [系统地图](../00-design-map.md) · [版本边界](../01-version-boundaries.md) · [来源索引](../02-sources.md)

## 核心内容

“历史模式”不是把所有历史事件放进日历，到点覆盖世界。HOI4 组合使用 AI 路线计划、国策、外交、事件和决议；路线偏好仍会碰到当前世界条件、互斥分支和行动资格。官方也明确承认，某些路线组合会令 AI 无法继续原计划。[^1]

## 六层职责

| 层次 | 回答什么 | 不保证什么 |
| --- | --- | --- |
| 游戏规则与历史模式 | 希望各国倾向哪条路径 | 所有日期和结果严格相同 |
| AI 战略计划 | 当前采用什么方向、尝试哪些国策 | 每个候选必定可执行 |
| 国策 | 国家持续投入哪项政策 | 对象一直存在、结果无须重查 |
| 事件 | 情境如何呈现、参与者如何回应 | 文本中的结果已经实际发生 |
| 决议／任务 | 当前可做什么、期限内要完成什么 | 倒计时结束必然走成功分支 |
| 外交与战争行动 | 是否获得目标、是否宣战、是否能打 | 获得战争目标等于已经开战 |

国策列表、启用／中止条件与权重可以协作选择路径；事件和决议则有各自生命周期。[^2][^3][^4][^5]

## 国策条件的关键区别

| 概念 | 正确理解 |
| --- | --- |
| 前置／互斥 | 树上的依赖与路线承诺 |
| available | 当前开展条件；进行中是否继续还受失效策略影响 |
| bypass | 节点绕过，不执行正常 completion_reward；可另配 bypass_effect |
| cancel_if_invalid | 条件失效时是否取消 |
| continue_if_invalid | 条件失效时是否继续；与取消开关组合会产生不同结果 |
| completion_reward | 正常完成时的效果，目标与资源仍需要有效 |
| will_lead_to_war_with | 预警与备战提示，不是宣战命令 |

这些是社区脚本接口说明，不是对所有国策采用同一配置的断言。一个节点“不再能点”，不等于 AI 永远停止；一个节点“可以绕过”，也不代表自动得到原正常奖励。[^3]

## 事件并非全都按日期轮询

事件可以由脚本调用、条件轮询或延迟调用触发。触发时的条件检查，与选项执行时是否仍能合法改变世界，是两个需要分别处理的阶段。不存在国家的延迟事件也不能一概假定会自动删除；社区文档记录了计时等待国家重新存在的情况。[^4]

决议接口中的 complete_effect 通常在点击开始时执行，倒计时结束又可走 remove_effect；任务还可能有超时和取消。名称中的“完成”不能代替对执行时间的核查。[^5]

## 两个当前官方实例

1.19 补丁说明：日本对暹罗的施压国策因对方加入另一阵营而不可用时，AI 会转向占领暹罗。这是明确编写的替代路径。[^6]

1.18.2 说明：捷克吞并奥地利会使德国历史计划取消；面对某些强大的捷克阵营局面，还增加了德国选择柏林—莫斯科路线的倾向。这不是“历史在固定日期继续原样发生”，而是世界偏离后改变计划。[^7]

这些实例也不意味着游戏有一个能推理任何反事实的通用历史智能。补丁仍在修复目标消失、关系改变、绕过条件和事件链问题。

## 对原创框架的启发

分别保存“历史想推动什么”“当前发生了什么”“行动是否合法”“AI 是否愿意做”。日期影响候选机会，条件决定资格，评分决定倾向，执行系统负责真正改变状态。

若把上述四件事都写在单个巨大事件里，后期每加一种改史方式都需要修改大量分支。应让内容调用共通规则，再为重要史实节点编写有质量的表现与特殊约束。

## 关联模块

波兰反例见 [13](13-poland-counterfactual.md)；历史调度见 [14](14-history-director.md)；事件生命周期见 [15](15-event-contract.md)；详细证据见[历史脚本备忘](../evidence/history-script-audit.md)。

## 反向索引

[版本、DLC 与证据边界](../01-version-boundaries.md) · [10 科技树：知识、制造与实际普及](10-technology.md) · [13 波兰提前被吞并：从反例读懂历史脚本](13-poland-counterfactual.md) · [14 历史方向与当前事实：可适应的历史框架](14-history-director.md)

## 来源

[^1]: Paradox Development Studio，Archangel85，[HoI4 Dev Diary — AI Plans](https://forum.paradoxplaza.com/forum/threads/hoi4-dev-diary-ai-plans.1151821/)，2019-02-13；访问 2026-09-13。
[^2]: HOI4 Community Wiki，[AI modding](https://hoi4.paradoxwikis.com/AI_modding#AI_strategy_plans)，社区脚本接口说明；访问 2026-09-13。
[^3]: HOI4 Community Wiki，[National focus modding](https://hoi4.paradoxwikis.com/National_focus_modding)，社区脚本接口说明；访问 2026-09-13。
[^4]: HOI4 Community Wiki，[Event modding](https://hoi4.paradoxwikis.com/Event_modding)，社区脚本接口说明；访问 2026-09-13。
[^5]: HOI4 Community Wiki，[Decision modding](https://hoi4.paradoxwikis.com/Decision_modding)，社区脚本接口说明；访问 2026-09-13。
[^6]: Paradox Development Studio，Steam 公告，[Thunder at our Gates — Patch Notes (1.19.0)](https://store.steampowered.com/news/app/394360/view/712277443918955865)，2026-06-10 公告；明确次日发布；访问 2026-09-13。
[^7]: Paradox Development Studio，Steam 官方公告列表，[Hearts of Iron IV — Patch 1.18.2](https://store.steampowered.com/news/posts/?appids=394360&enddate=1779408000&feed=steam_community_announcements)，2026-05-20；访问 2026-09-13。
