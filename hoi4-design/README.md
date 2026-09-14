# 钢铁雄心 IV 机制拆解与古代中国军事框架

这套文档只研究 **战斗与军队建设、补给、科技与学说、历史事件的适应性**，不做 HOI4 全系统百科。目标是提炼可用于古代中国题材的机制关系，而不是把现代军制、坦克或铁路简单换名。

最重要的设计结论是：**编制提出需求，生产与训练兑现能力，补给决定能坚持多久；历史内容提出问题，当前世界决定还能用什么方式解决。**

古代部分采用不锁定朝代的可配置框架。文中的职能称谓、编制比例和数字示例不是史实定额；朝代确定后再校准军制、技术可用性、运输参数和术语。

## 优先阅读

| 想解决的问题 | 入口 |
| --- | --- |
| 先看系统如何接起来 | [设计总纲与系统地图](00-design-map.md) |
| 波兰提前消失，德国还会照剧本开战吗 | [13 波兰反事实案例](modules/13-poland-counterfactual.md) |
| 怎样让历史方向适应玩家改写 | [14 历史框架](modules/14-history-director.md) → [15 事件契约](modules/15-event-contract.md) → [16 蝴蝶效应案例](modules/16-butterfly-cases.md) |
| 粮草和补给线怎样做 | [07 HOI4 原机制](modules/07-hoi4-logistics.md) → [08 古代粮草模型](modules/08-supply-model.md) |
| 战兵、哨骑、传令与军需怎样进入编制 | [03 编制](modules/03-army-templates.md) → [05 人员职责](modules/05-personnel-and-training.md) → [06 指挥与侦察](modules/06-command-and-recon.md) |
| 科技怎样真正改变军队 | [10 科技与普及](modules/10-technology.md) → [11 学说与改革](modules/11-doctrine-and-reform.md) |
| 如何缩成能做完的游戏 | [17 完整远征案例](modules/17-worked-campaign.md) → [19 最小原型](modules/19-prototype.md) |

## 军事模块

| 模块 | 核心内容 | 借鉴重点 |
| --- | --- | --- |
| [01 时间、地图与尺度](modules/01-time-and-scale.md) | 战略、战役和战斗的分工 | 持续模拟、暂停决策与不同过程计时 |
| [02 战斗结算](modules/02-combat.md) | 组织、人员装备、战宽、预备与撤退 | 胜负不必靠杀光敌人 |
| [03 自定义编制](modules/03-army-templates.md) | 模板、实例、主战与多层支援 | 纸面结构不等于实配战力 |
| [04 装备与补充](modules/04-equipment-and-replenishment.md) | 制造、配发、补缺、换装与回收 | 更好装备需要真实交付与采用 |
| [05 人员与训练](modules/05-personnel-and-training.md) | 战兵、辅助职责、兵源与合练 | 支援人员有服务能力，也有成本 |
| [06 指挥与侦察](modules/06-command-and-recon.md) | 将官、HQ、命令、报告与通信 | 指挥链比单纯光环更有意义 |

## 补给与科技模块

| 模块 | 核心内容 | 借鉴重点 |
| --- | --- | --- |
| [07 HOI4 补给](modules/07-hoi4-logistics.md) | 干线、枢纽、末端、地方补给与需求 | 区分容量、覆盖与单位状态 |
| [08 古代粮草模型](modules/08-supply-model.md) | 库存、运输、时间、竞争与断粮 | 网络之外还需守恒账本 |
| [09 战役行动](modules/09-campaign-operations.md) | 集结、截粮、围城、追击与恢复 | 后勤目标能够改变另一处战斗 |
| [10 科技与普及](modules/10-technology.md) | 知识、制度、制造、训练与配发 | 研究完成不等于全军升级 |
| [11 学说与改革](modules/11-doctrine-and-reform.md) | 新版 Mastery 与军事组织学习 | 采用方向与练会分开 |

## 历史适应与制作模块

| 模块 | 核心内容 | 借鉴重点 |
| --- | --- | --- |
| [12 国策、事件与历史 AI](modules/12-focus-events-and-ai.md) | 路线、条件、回应和实际行动的分工 | 日期与倾向不覆盖事实 |
| [13 波兰反事实案例](modules/13-poland-counterfactual.md) | 旧脚本、当前前提与证据缺口 | 不把目标消失机械变为对新主人宣战 |
| [14 历史框架](modules/14-history-director.md) | 史实参考、压力、目标与行动候选 | 保留问题，允许解决方式改变 |
| [15 事件契约](modules/15-event-contract.md) | 绑定、有效期、失效、复核与一次性结算 | 内容需要完整生命周期 |
| [16 蝴蝶效应案例](modules/16-butterfly-cases.md) | 十二种改史情境和多种终局 | 以有限通用规则覆盖组合 |
| [17 完整远征案例](modules/17-worked-campaign.md) | 从改编和备粮到政权更替 | 军事系统与历史内容共享事实 |
| [18 架构与验证](modules/18-architecture-and-validation.md) | 对象边界、守恒、引用与测试情景 | 世界逻辑统一，内容不绕过规则 |
| [19 最小原型](modules/19-prototype.md) | 小地图、少量部队与两条历史章节 | 先验证闭环，再扩展时代内容 |

## 版本和证据

研究核对日为 2026-09-13，稳定版参考锚点为 PC 1.19.2。新版学说、团级支援与 Army HQ 已纳入；计划发布的补丁、夏季测试服和工业园开发稿不混作现行机制。详见[版本边界](01-version-boundaries.md)。

原始资料与适用范围见[来源索引](02-sources.md)。较细的接口语义和冲突保留在[历史脚本证据备忘](evidence/history-script-audit.md)与[科技证据备忘](evidence/technology-audit.md)。它们供查证，不是必须先读的入门章节。

文档明确区分 HOI4 事实、设计判断与原创方案。没有进行本地实机复现；尤其不把旧德国脚本写成现版唯一结果。

## 使用方式

所有模块可独立阅读，有关联链接、反向索引和来源。整套使用相对路径，移动文件夹后仍可相互跳转。

需要和前一套研究合看时，可对照 [CK3 总览](../ck3-design/README.md)中的人物、臣属、继承和制度模块；本套先保证军队与战役成立，不把完整人物政治作为第一版依赖。该链接是跨资料集引用，单独搬运本套时需要同时保留上级目录中的 CK3 文档。

