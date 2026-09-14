# 15 历史事件的配置契约与生命周期

[返回总览](../README.md) · [系统地图](../00-design-map.md) · [版本边界](../01-version-boundaries.md) · [来源索引](../02-sources.md)

## 核心内容

一个历史事件不应只是“日期、标题、选项、奖励”。它还需要对象绑定、适用条件、有效期、失效策略和结算记录。HOI4 的接口与修复案例显示了这些问题的重要性；下文给出的是原创配置建议，不是可直接运行的 HOI4 脚本。[^1][^2][^3][^4]

## 一份内容配置至少说明什么

| 字段组 | 需要回答的问题 |
| --- | --- |
| 身份 | 这是什么内容版本？一次性还是可以出现新实例？ |
| 时间 | 最早何时、最晚何时？是固定日期还是机会窗口？ |
| 角色 | 谁是发起者、回应者、争议对象、受影响地区？ |
| 绑定方式 | 必须是指定人物，还是符合职责的当前人物？ |
| 硬前提 | 对象存在、领土关系、独立性、战争与条约是否符合？ |
| 目标 | 什么状态算解决？是否可被玩家提前用别的方法解决？ |
| 选项 | 能发起哪些真实行动，需要哪些资源和许可？ |
| 进行中检查 | 何时检查失效？哪些变化允许继承继续？ |
| 替代策略 | 终止、暂缓、重谈、换对象还是更换行动？ |
| 效果与记录 | 哪些状态改变？怎样防止重复领取、重复宣战？ |
| 文本依据 | 标题、描述和结果分别依赖哪些已经存在的事实？ |

## 生命周期

建议把“历史章节”与“其中一笔提议”分开。章节可持续多年，提议可能只有数日有效。

候选 → 已绑定 → 已呈现／已提议 → 进行中 → 完成、替代、失效或过期。

重要的是区分“预备候选没有显示”与“玩家已经接受的行动被取消”。后者需要说明原因、处理承诺和已占用资源；前者通常不必打断玩家。

## 三次必要的复核

| 时间点 | 检查什么 | 防止什么 |
| --- | --- | --- |
| 候选形成时 | 世界是否适合这条内容 | 向不存在的对象发起事件 |
| 呈现／回应时 | 对象和前提是否仍有效 | 使用使者出发前的陈旧状态 |
| 提交效果时 | 当前权属、资源、唯一实例状态 | 弹窗期间世界变化导致非法结果 |

正在进行的长期行动还可以订阅少数关键变化，例如人物死亡、目标政权消失、战争开始、争议地转手；无需每天遍历所有历史内容的全部条件。订阅是建议的效率方案，不代表必须使用复杂消息平台。

## 配置示意

以下为说明性伪配置，字段名是本套建议，并非任何引擎现成 API；条件细节还需在实现时定义。

```yaml
id: border_security_campaign
content_version: 1
kind: structural_history
window: scenario_defined

roles:
  sponsor: current_authority_of_origin
  territory: specified_border_region
  counterpart: actor_responsible_for_current_dispute

goal: border_security_problem_resolved
eligibility:
  - sponsor_has_legitimate_authority
  - dispute_is_still_relevant
  - counterpart_is_valid_for_selected_action

on_goal_already_met: resolve_by_existing_outcome
on_counterpart_changed: reassess_before_rebinding
on_relation_changed: invalidate_incompatible_actions
on_resource_shortage: offer_preparation_or_postponement
on_window_expired: expire_with_record

choices:
  - negotiate
  - reinforce_defense
  - prepare_campaign
```

其中“counterpart”不是永远取领土当前主人：边患若来自独立袭扰者，就不能因为土地归属某国而自动向该国宣战。对象选择必须与争端类型一致。

## 资源和效果要一次完整提交

玩家选了“出资备战”，先确认钱和仓储承诺仍可支付，再一次性创建项目与对应扣款；任何必要条件失败，就不留下半个项目。使用唯一实例编号，确保重复通知、存档重载或双次点击不会再次发奖励。

预订的资源与已经花掉的资源分开：未出发物资可按规则解除预订，已经消费的粮草不能退款，已经制造的装备不能因外交取消而消失。

若目标在行动途中改变，保留原绑定和变更理由，创建新版本或新提议；不能悄悄把玩家同意对 A 的条件改成对 B 同样生效。

## 防止“同名复活”的旧事件

政权、人物、地区和历史名称使用不同标识。新建立的同名政权不是自动继承所有旧交易；只有声明可由合法继承者接续的行动才允许继承。

HOI4 社区事件文档描述了对不存在国家的延迟计时行为，因此“对象消失后所有待办天然安全”不是可依赖的默认前提。原创游戏应主动规定过期与继承规则。[^2]

## 内容生产要求

编写者交付的不是单条理想剧情，还应有至少四种情境：正常、目标已完成、对象变化、资源／关系失效。通用结果模板负责解释原因，重要章节再提供更有历史辨识度的叙事。

## 关联模块

总框架见 [14](14-history-director.md)；反例见 [13](13-poland-counterfactual.md)；情景矩阵见 [16](16-butterfly-cases.md)；实现验证见 [18](18-architecture-and-validation.md)。

## 反向索引

[版本、DLC 与证据边界](../01-version-boundaries.md)

[12 国策、事件、决议与历史 AI 的分工](12-focus-events-and-ai.md) · [13 波兰提前被吞并：从反例读懂历史脚本](13-poland-counterfactual.md) · [14 历史方向与当前事实：可适应的历史框架](14-history-director.md) · [16 蝴蝶效应案例：该改写什么，不该改写什么](16-butterfly-cases.md) · [18 模块边界、内容生产与验证](18-architecture-and-validation.md) · [19 最小可玩原型与后续扩展](19-prototype.md)

## 来源

[^1]: HOI4 Community Wiki，[National focus modding](https://hoi4.paradoxwikis.com/National_focus_modding)，社区脚本接口说明；访问 2026-09-13。
[^2]: HOI4 Community Wiki，[Event modding](https://hoi4.paradoxwikis.com/Event_modding)，社区脚本接口说明；访问 2026-09-13。
[^3]: HOI4 Community Wiki，[Decision modding](https://hoi4.paradoxwikis.com/Decision_modding)，社区脚本接口说明；访问 2026-09-13。
[^4]: Paradox Development Studio，Steam 公告，[Thunder at our Gates — Patch Notes (1.19.0)](https://store.steampowered.com/news/app/394360/view/712277443918955865)，2026-06-10 公告；明确次日发布；访问 2026-09-13。
