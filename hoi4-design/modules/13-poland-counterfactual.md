# 13 波兰提前被吞并：从反例读懂历史脚本

[返回总览](../README.md) · [系统地图](../00-design-map.md) · [版本边界](../01-version-boundaries.md) · [来源索引](../02-sources.md)

## 先给结论

不能把 HOI4 理解为“1939 年 9 月无条件向波兰宣战”。历史倾向、国策顺序、事件回应、战争目标与实际宣战是不同环节。波兰提前消失会改变相关条件，但**不能据此自动推导德国转而在同一天攻击苏联**。[^1]

本次能确认旧版脚本的处理，也能确认现版表述中的关键前提；没有取得完整、可核实的 1.19.2 德国运行脚本及复现场景，因此不提供现版唯一后续结局。

## 先明确“吞并”指什么

| 情景 | 国家还存在吗 | 需要额外检查什么 |
| --- | --- | --- |
| 和约后完全吞并 | 原国家可能不再存在 | 但泽所有者、控制者与后续继承实体 |
| 投降但战争未结束 | 不一定消失 | 占领与所有权、阵营战争 |
| 成为苏联傀儡 | 通常仍是一个政治实体 | 宗主国、外交权限、战争牵连 |
| 流亡 | 仍可能保留政治与战争状态 | 宿主、法理权利、原有事件 |
| 只失去但泽 | 波兰可以继续存在 | 但泽条件失效，不等于全部对波兰关系失效 |

这些状态不能压成一个“波兰已失败”标记。更一般地说，领土属于谁、谁在控制、哪个政权仍存在，是三个不同问题。

## 可审查的旧版案例

固定在 2019-04-03、标注 1.6.2 的第三方历史脚本镜像里，Danzig or War 正常开始需要但泽由波兰系国家拥有且控制等条件。其绕过条件包含该组合不再成立。[^2]

所以，在这一**旧版快照**中，若国策尚未正常完成、路线可达、苏联已拥有并控制但泽，绕过资格成立。绕过不执行正常完成奖励，因此不会单靠这个节点继续向波兰发送原最后通牒，也不会单靠绕过自动取得对苏联的战争目标。[^2][^3]

即使正常链条走到波兰拒绝，旧事件后续的实际效果也是生成战争目标。某处看似宣战的关键词位于提示效果之中，不能当作真正执行的宣战。[^4]

这里的价值是展示条件、作用域和执行阶段如何协作；该镜像不是现版官方源码，也不证明德国其他行动永远不会攻击苏联。

## 现版资料为什么不能给出同样确定的句子

当前 Wiki 德国工业／历史分支标为 1.19，其正常条件仍包含但泽所有者与控制者的波兰原始标签要求。但绕过栏把相近的正向条件也列入其中，缺少旧版的关键否定，存在疑似整理错误。原始 Wiki 文本中也有这个问题。[^5]

因此只能说：按已读现版正常条件，苏联已拥有并控制但泽时，原外交节点的正常前提不成立。**最终是绕过、暂停、取消还是另有路径，需以当前脚本和具体存档确认；不能反过来声称现版必定卡住。**

另外，1.15 的德国历史树重做属于基础更新。关闭 Götterdämmerung 不等于恢复 2019 年旧历史树，不能用 DLC 开关把新旧证据混在一起。[^6]

## 你的游戏应该怎样处理等价问题

假设原章节是“朝廷计划讨伐边镇 A”，但 A 的领地提前被 B 兼并。依次检查：

1. 原诉求是什么：收复土地、阻止袭扰，还是惩罚某位人物？
2. 诉求是否已经解决：土地若已归己方，章节可标为以其他方式完成。
3. 原对象是否消失：消失的是人物、政权，还是仅仅失去领地？
4. 新对象是否仍符合诉求：B 占有争议土地，但未必延续 A 的袭扰。
5. 与 B 的当前关系和力量是否支持行动：盟友、附庸、条约和风险都要重评。
6. 选择交涉、备战、调整目标、暂缓或结束；不能只替换一个国家 ID。
7. 由真实行动系统执行，战争未发生就不播放“讨伐大捷”。

## 开始后才变化，更需要单独规则

对象可能在政策执行中、使者途中、弹窗打开时或最后结算前变化。每个阶段需要相应失效处理；检查一次“对象存在”并不能解决全部问题。[^3][^7]

当前官方仍会专门修复这种问题：例如 1.19 修复了伊拉克邀请目标消失或变成敌人时可能永久锁住的决议。[^8]

## 借鉴结论

保留历史中的因果问题，允许解决方式改变；保留具有身份约束的史实人物事件，不强行把别人替换成同一个历史人物；让“提前解决”成为被承认的结果，而不是违背编剧安排的失败。

## 关联模块

系统分工见 [12](12-focus-events-and-ai.md)；通用历史框架见 [14](14-history-director.md)；生命周期见 [15](15-event-contract.md)；原始证据定位见[历史脚本备忘](../evidence/history-script-audit.md)。

## 反向索引

[版本、DLC 与证据边界](../01-version-boundaries.md)

[版本、DLC 与证据边界](../01-version-boundaries.md) · [12 国策、事件、决议与历史 AI 的分工](12-focus-events-and-ai.md) · [14 历史方向与当前事实：可适应的历史框架](14-history-director.md) · [15 历史事件的配置契约与生命周期](15-event-contract.md)

## 来源

[^1]: Paradox Development Studio，Archangel85，[HoI4 Dev Diary — AI Plans](https://forum.paradoxplaza.com/forum/threads/hoi4-dev-diary-ai-plans.1151821/)，2019-02-13；访问 2026-09-13。
[^2]: Killeritch 第三方历史脚本镜像，[germany.txt，固定提交 b973b6b](https://github.com/Killeritch/Hearts-of-Iron-IV/blob/b973b6bd327df320fc01a45d0d8bd8d5a24a82a7/common/national_focus/germany.txt#L3207)，2019-04-03；标注 1.6.2，不是现行官方源码；访问 2026-09-13。
[^3]: HOI4 Community Wiki，[National focus modding](https://hoi4.paradoxwikis.com/National_focus_modding)，社区脚本接口说明；访问 2026-09-13。
[^4]: Killeritch 第三方历史脚本镜像，[Germany.txt，固定提交 b973b6b](https://github.com/Killeritch/Hearts-of-Iron-IV/blob/b973b6bd327df320fc01a45d0d8bd8d5a24a82a7/events/Germany.txt#L3805)，2019-04-03；标注 1.6.2；访问 2026-09-13。
[^5]: HOI4 Community Wiki，[German national focus tree: industrial / historical branches](https://hoi4.paradoxwikis.com/German_national_focus_tree:_industrial/_historical_branches#Danzig_or_War)，页面标 1.19；bypass 栏存在待核矛盾；访问 2026-09-13。
[^6]: HOI4 Community Wiki，补丁转录，[Patch 1.15](https://hoi4.paradoxwikis.com/Patch_1.15)，2024-11-14；访问 2026-09-13。
[^7]: HOI4 Community Wiki，[Event modding](https://hoi4.paradoxwikis.com/Event_modding)，社区脚本接口说明；访问 2026-09-13。
[^8]: Paradox Development Studio，Steam 公告，[Thunder at our Gates — Patch Notes (1.19.0)](https://store.steampowered.com/news/app/394360/view/712277443918955865)，2026-06-10 公告；明确次日发布；访问 2026-09-13。
