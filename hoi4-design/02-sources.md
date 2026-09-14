# 来源索引与证据说明

[返回总览](README.md) · [系统地图](00-design-map.md) · [版本边界](01-version-boundaries.md)

## 证据使用方式

全部资料访问日为 **2026-09-13**。官方发布、日记与补丁用于确认功能变化、公开设计取舍和版本边界；用户指定的 HOI4 Wiki 用于详细机制与脚本接口。Wiki 是社区维护资料，不等于每项内容都由开发者保证。

官方 Steam 单篇链接有时只显示页面外壳，本套使用同一发行方的官方公告列表阅读正文；下表提供相应完整正文入口。列表中的其他日期文章不与目标文章混算。

对波兰反例，旧版固定提交仅用于展示可审查的历史实现。它们来自第三方镜像，不是官方仓库，也不作为 1.19.2 当前客户端脚本的证明。现版 Wiki 的绕过条件矛盾明确保留，没有通过猜测补全。

## 事实与建议的区分

“HOI4 核心内容”描述来源支持的机制；“设计判断”解释其可能作用，不冒充开发团队意图；古代框架、原型、数字账本和伪配置属于原创建议。只有在官方日记直接陈述时，才把某种取舍归因于开发者。

本套没有逐项复测稳定版数值、检查本地游戏安装或实现可玩原型。古代部分不锁定朝代，因此不提供伪造的真实编制比例、口粮定额或器械发明年份。

## 如何查证

先在模块脚注找到直接来源；需要接口细节和证据冲突时，读[历史脚本备忘](evidence/history-script-audit.md)与[科技备忘](evidence/technology-audit.md)。以下索引列出主要原始条目，并反向链接到引用它们的文档。

## 官方开发日志、补丁与公告

| 编号 | 来源 | 维护方与适用范围 | 本套引用位置 |
| --- | --- | --- | --- |
| 1 | [HOI4 Dev Diary — Traiiiiins](https://forum.paradoxplaza.com/forum/threads/hoi4-dev-diary-traiiiiins.1489330/) | Paradox Development Studio，Arheo 等；2021-09-01；最终上市前设计说明 | [07](modules/07-hoi4-logistics.md)、[08](modules/08-supply-model.md) |
| 2 | [Thunder at our Gates: Ship Captains & Division Designer](https://store.steampowered.com/news/app/394360/view/668366079168348304)；[正文入口](https://store.steampowered.com/news/posts/?appids=394360&enddate=1779408000&feed=steam_community_announcements) | Paradox Development Studio，Steam 公告；2026-05-21；新增功能以正式补丁交叉确认 | [设计总纲：从军事组织到可改写的历史](00-design-map.md)、[版本、DLC 与证据边界](01-version-boundaries.md)、[03](modules/03-army-templates.md)、[04](modules/04-equipment-and-replenishment.md)、[10](modules/10-technology.md)、[17](modules/17-worked-campaign.md) |
| 3 | [Thunder at our Gates: Army HQs & Special Forces](https://store.steampowered.com/news/app/394360/view/710025009936993029)；[正文入口](https://store.steampowered.com/news/posts/?appids=394360&enddate=1780531200&feed=steam_community_announcements) | Paradox Development Studio，Jaboth／Zwirbaum；2026-06-03 | [设计总纲：从军事组织到可改写的历史](00-design-map.md)、[版本、DLC 与证据边界](01-version-boundaries.md)、[01](modules/01-time-and-scale.md)、[06](modules/06-command-and-recon.md)、[11](modules/11-doctrine-and-reform.md) |
| 4 | [Thunder at our Gates — Patch Notes (1.19.0)](https://store.steampowered.com/news/app/394360/view/712277443918955865)；[正文入口](https://store.steampowered.com/news/posts/?appids=394360&enddate=1781107199&feed=steam_community_announcements) | Paradox Development Studio，Steam 公告；2026-06-10 公告；明确次日发布 | [版本、DLC 与证据边界](01-version-boundaries.md)、[历史方向、世界状态与事件脚本：证据核查备忘](evidence/history-script-audit.md)、[科技、学说与军备普及：证据备忘](evidence/technology-audit.md)、[03](modules/03-army-templates.md)、[06](modules/06-command-and-recon.md)、[11](modules/11-doctrine-and-reform.md)、[12](modules/12-focus-events-and-ai.md)、[13](modules/13-poland-counterfactual.md)、[14](modules/14-history-director.md)、[15](modules/15-event-contract.md)、[16](modules/16-butterfly-cases.md)、[18](modules/18-architecture-and-validation.md) |
| 5 | [Developer Diary — Doctrines](https://store.steampowered.com/news/app/394360/view/508466730850320835)；[正文入口](https://store.steampowered.com/news/posts/?appids=394360&enddate=1759240000&feed=steam_community_announcements) | Paradox Development Studio，Jack；2025-09-30 | [设计总纲：从军事组织到可改写的历史](00-design-map.md)、[科技、学说与军备普及：证据备忘](evidence/technology-audit.md)、[11](modules/11-doctrine-and-reform.md) |
| 6 | [No Compromise, No Surrender — Patch Notes, Live Stream & Mods!](https://store.steampowered.com/news/app/394360/view/606425106922602562)；[正文入口](https://store.steampowered.com/news/posts/?appids=394360&enddate=1764154454&feed=steam_community_announcements) | Paradox Development Studio；2025-11-20；1.17 | [版本、DLC 与证据边界](01-version-boundaries.md)、[科技、学说与军备普及：证据备忘](evidence/technology-audit.md)、[11](modules/11-doctrine-and-reform.md) |
| 7 | [HoI4 Dev Diary — AI Plans](https://forum.paradoxplaza.com/forum/threads/hoi4-dev-diary-ai-plans.1151821/) | Paradox Development Studio，Archangel85；2019-02-13 | [设计总纲：从军事组织到可改写的历史](00-design-map.md)、[历史方向、世界状态与事件脚本：证据核查备忘](evidence/history-script-audit.md)、[12](modules/12-focus-events-and-ai.md)、[13](modules/13-poland-counterfactual.md)、[14](modules/14-history-director.md)、[17](modules/17-worked-campaign.md) |
| 8 | [Studio Gold Update — September 2026；Industrial Might & Military Production](https://store.steampowered.com/news/posts/?appids=394360&enddate=1788872885&feed=steam_community_announcements) | Paradox Development Studio，Steam 官方公告列表；2026-09-04／2026-09-08 | [版本、DLC 与证据边界](01-version-boundaries.md)、[科技、学说与军备普及：证据备忘](evidence/technology-audit.md) |
| 9 | [Thunder at our Gates — Patch 1.19.2](https://store.steampowered.com/news/app/394360/view/717908846920599778)；[正文入口](https://store.steampowered.com/news/posts/?appids=394360&enddate=1782846000&feed=steam_community_announcements) | Paradox Development Studio；2026-06-30 | [版本、DLC 与证据边界](01-version-boundaries.md)、[科技、学说与军备普及：证据备忘](evidence/technology-audit.md) |
| 10 | [Hearts of Iron IV — Patch 1.18.2](https://store.steampowered.com/news/posts/?appids=394360&enddate=1779408000&feed=steam_community_announcements) | Paradox Development Studio，Steam 官方公告列表；2026-05-20 | [12](modules/12-focus-events-and-ai.md)、[14](modules/14-history-director.md)、[16](modules/16-butterfly-cases.md) |
| 11 | [Developer Diary — Military Industrial Organisations](https://steamstore-a.akamaihd.net/news/externalpost/steam_community_announcements/5220291886483387100)；[正文入口](https://store.steampowered.com/news/posts/?feed=steam_community_announcements&appids=394360&enddate=1696434881) | Paradox Development Studio，C0RAX；2023-09-27；用于设计分层，不推断现行全部数值 | [科技、学说与军备普及：证据备忘](evidence/technology-audit.md) |
| 12 | [Developer Diary — Historical Germany](https://store.steampowered.com/news/app/394360/view/4702411539888443151) | Paradox Development Studio，Paradox_Danne／ManoDeZombi；2024-10-16；发行前设计稿 | [历史方向、世界状态与事件脚本：证据核查备忘](evidence/history-script-audit.md) |
| 13 | [HOI IV Dev Corner — Industrial Might & Military Production](https://store.steampowered.com/news/app/394360/view/705530288588980377) | Paradox Development Studio，Zwirbaum；2026-09-08；未发布方案，不算稳定版 | [科技、学说与军备普及：证据备忘](evidence/technology-audit.md) |

## 社区机制页与脚本接口说明

| 编号 | 来源 | 维护方与适用范围 | 本套引用位置 |
| --- | --- | --- | --- |
| 14 | [Logistics](https://hoi4.paradoxwikis.com/Logistics) | Paradox Community Wiki；动态机制页；补给重做始于 1.11 | [设计总纲：从军事组织到可改写的历史](00-design-map.md)、[版本、DLC 与证据边界](01-version-boundaries.md)、[04](modules/04-equipment-and-replenishment.md)、[07](modules/07-hoi4-logistics.md)、[08](modules/08-supply-model.md)、[09](modules/09-campaign-operations.md)、[17](modules/17-worked-campaign.md) |
| 15 | [Land battle](https://hoi4.paradoxwikis.com/Land_battle) | Paradox Community Wiki；动态机制页；本套只引用结构，不照搬全部系数 | [01](modules/01-time-and-scale.md)、[02](modules/02-combat.md)、[09](modules/09-campaign-operations.md) |
| 16 | [Division](https://hoi4.paradoxwikis.com/Division) | Paradox Community Wiki；动态页，部分段落滞后；编制新增以 1.19 官方资料为准 | [03](modules/03-army-templates.md)、[04](modules/04-equipment-and-replenishment.md)、[05](modules/05-personnel-and-training.md) |
| 17 | [Division designer](https://hoi4.paradoxwikis.com/Division_designer) | Paradox Community Wiki；动态机制页 | [03](modules/03-army-templates.md)、[04](modules/04-equipment-and-replenishment.md) |
| 18 | [Battle plan](https://hoi4.paradoxwikis.com/Battle_plan) | Paradox Community Wiki；动态机制页 | [01](modules/01-time-and-scale.md)、[06](modules/06-command-and-recon.md)、[09](modules/09-campaign-operations.md) |
| 19 | [Army](https://hoi4.paradoxwikis.com/Army) | Paradox Community Wiki；动态机制页 | [05](modules/05-personnel-and-training.md) |
| 20 | [Commander](https://hoi4.paradoxwikis.com/Commander) | Paradox Community Wiki；动态机制页 | [06](modules/06-command-and-recon.md) |
| 21 | [Combat tactics](https://hoi4.paradoxwikis.com/Combat_tactics) | Paradox Community Wiki；动态机制页 | [02](modules/02-combat.md)、[06](modules/06-command-and-recon.md) |
| 22 | [Terrain](https://hoi4.paradoxwikis.com/Terrain) | Paradox Community Wiki；动态机制页 | [02](modules/02-combat.md)、[09](modules/09-campaign-operations.md) |
| 23 | [Attrition and accidents](https://hoi4.paradoxwikis.com/Attrition_and_accidents) | Paradox Community Wiki；动态机制页 | [02](modules/02-combat.md)、[05](modules/05-personnel-and-training.md) |
| 24 | [Patch 1.19](https://hoi4.paradoxwikis.com/Patch_1.19) | Paradox Community Wiki；1.19 更新记录 | [科技、学说与军备普及：证据备忘](evidence/technology-audit.md) |
| 25 | [Research](https://hoi4.paradoxwikis.com/Research) | HOI4 Community Wiki；动态机制页，未采用存在冲突的基准天数 | [科技、学说与军备普及：证据备忘](evidence/technology-audit.md)、[10](modules/10-technology.md) |
| 26 | [Production](https://hoi4.paradoxwikis.com/Production) | HOI4 Community Wiki；动态机制页，常规陆军军备生产结构 | [科技、学说与军备普及：证据备忘](evidence/technology-audit.md)、[10](modules/10-technology.md) |
| 27 | [Equipment](https://hoi4.paradoxwikis.com/Equipment) | HOI4 Community Wiki；动态机制页 | [科技、学说与军备普及：证据备忘](evidence/technology-audit.md)、[10](modules/10-technology.md) |
| 28 | [Land doctrine](https://hoi4.paradoxwikis.com/Land_doctrine) | HOI4 Community Wiki；动态页，包含新版 Mastery 与团级支援 | [科技、学说与军备普及：证据备忘](evidence/technology-audit.md)、[11](modules/11-doctrine-and-reform.md) |
| 29 | [AI modding](https://hoi4.paradoxwikis.com/AI_modding#AI_strategy_plans) | HOI4 Community Wiki；社区脚本接口说明 | [历史方向、世界状态与事件脚本：证据核查备忘](evidence/history-script-audit.md)、[12](modules/12-focus-events-and-ai.md) |
| 30 | [National focus modding](https://hoi4.paradoxwikis.com/National_focus_modding) | HOI4 Community Wiki；社区脚本接口说明 | [历史方向、世界状态与事件脚本：证据核查备忘](evidence/history-script-audit.md)、[12](modules/12-focus-events-and-ai.md)、[13](modules/13-poland-counterfactual.md)、[15](modules/15-event-contract.md)、[18](modules/18-architecture-and-validation.md) |
| 31 | [Event modding](https://hoi4.paradoxwikis.com/Event_modding) | HOI4 Community Wiki；社区脚本接口说明 | [历史方向、世界状态与事件脚本：证据核查备忘](evidence/history-script-audit.md)、[12](modules/12-focus-events-and-ai.md)、[13](modules/13-poland-counterfactual.md)、[15](modules/15-event-contract.md)、[18](modules/18-architecture-and-validation.md) |
| 32 | [Decision modding](https://hoi4.paradoxwikis.com/Decision_modding) | HOI4 Community Wiki；社区脚本接口说明 | [历史方向、世界状态与事件脚本：证据核查备忘](evidence/history-script-audit.md)、[12](modules/12-focus-events-and-ai.md)、[15](modules/15-event-contract.md) |
| 33 | [National focus](https://hoi4.paradoxwikis.com/National_focus) | HOI4 Community Wiki；动态机制页 | [科技、学说与军备普及：证据备忘](evidence/technology-audit.md)、[10](modules/10-technology.md) |
| 34 | [German national focus tree: industrial / historical branches](https://hoi4.paradoxwikis.com/German_national_focus_tree:_industrial/_historical_branches#Danzig_or_War) | HOI4 Community Wiki；页面标 1.19；bypass 栏存在待核矛盾 | [版本、DLC 与证据边界](01-version-boundaries.md)、[历史方向、世界状态与事件脚本：证据核查备忘](evidence/history-script-audit.md)、[13](modules/13-poland-counterfactual.md) |
| 35 | [Patch 1.15](https://hoi4.paradoxwikis.com/Patch_1.15) | HOI4 Community Wiki，补丁转录；2024-11-14 | [版本、DLC 与证据边界](01-version-boundaries.md)、[历史方向、世界状态与事件脚本：证据核查备忘](evidence/history-script-audit.md)、[13](modules/13-poland-counterfactual.md) |
| 36 | [Technology modding](https://hoi4.paradoxwikis.com/Technology_modding) | HOI4 Community Wiki；动态接口页；旧学说与基准天数冲突已排除 | [科技、学说与军备普及：证据备忘](evidence/technology-audit.md) |
| 37 | [Army planner](https://hoi4.paradoxwikis.com/Army_planner) | HOI4 Community Wiki；动态机制页；不采用旧补给区域公式 | [科技、学说与军备普及：证据备忘](evidence/technology-audit.md) |
| 38 | [Officer corps](https://hoi4.paradoxwikis.com/Officer_corps) | HOI4 Community Wiki；包含旧学说段落，使用范围受限 | [科技、学说与军备普及：证据备忘](evidence/technology-audit.md) |
| 39 | [Hearts of Iron 4 Wiki](https://hoi4.paradoxwikis.com/Hearts_of_Iron_4_Wiki) | HOI4 Community Wiki；入口页，不能证明每篇子页已同步更新 | [历史方向、世界状态与事件脚本：证据核查备忘](evidence/history-script-audit.md) |
| 40 | [German events](https://hoi4.paradoxwikis.com/German_events) | HOI4 Community Wiki；相关条目标 1.10，非当前脚本 | [历史方向、世界状态与事件脚本：证据核查备忘](evidence/history-script-audit.md) |
| 41 | [Triggers](https://hoi4.paradoxwikis.com/Triggers) | HOI4 Community Wiki；社区脚本接口说明 | [历史方向、世界状态与事件脚本：证据核查备忘](evidence/history-script-audit.md) |

## 明确限定版本的历史脚本镜像

| 编号 | 来源 | 维护方与适用范围 | 本套引用位置 |
| --- | --- | --- | --- |
| 42 | [germany.txt，固定提交 b973b6b](https://github.com/Killeritch/Hearts-of-Iron-IV/blob/b973b6bd327df320fc01a45d0d8bd8d5a24a82a7/common/national_focus/germany.txt#L3207) | Killeritch 第三方历史脚本镜像；2019-04-03；标注 1.6.2，不是现行官方源码 | [历史方向、世界状态与事件脚本：证据核查备忘](evidence/history-script-audit.md)、[13](modules/13-poland-counterfactual.md) |
| 43 | [Germany.txt，固定提交 b973b6b](https://github.com/Killeritch/Hearts-of-Iron-IV/blob/b973b6bd327df320fc01a45d0d8bd8d5a24a82a7/events/Germany.txt#L3805) | Killeritch 第三方历史脚本镜像；2019-04-03；标注 1.6.2 | [历史方向、世界状态与事件脚本：证据核查备忘](evidence/history-script-audit.md)、[13](modules/13-poland-counterfactual.md) |
| 44 | [GER.txt — AI strategy plans，固定提交 b973b6b](https://github.com/Killeritch/Hearts-of-Iron-IV/blob/b973b6bd327df320fc01a45d0d8bd8d5a24a82a7/common/ai_strategy_plans/GER.txt#L1) | Killeritch 第三方历史脚本镜像；2019-04-03；标注 1.6.2 | [历史方向、世界状态与事件脚本：证据核查备忘](evidence/history-script-audit.md) |

## 已知冲突如何处理

| 位置 | 问题 | 本套处理 |
| --- | --- | --- |
| 德国当前国策表 | 正常条件与绕过栏有疑似否定遗漏 | 不据此断言现版一定绕过或卡住 |
| German events | 相关条目仍标旧版本 | 不当作当前运行事件 |
| 军官与部分科技接口页 | 保留旧学说描述 | 用 1.17 官方改制确认新结构 |
| 师编制旧段落 | 尚未完整反映团级支援 | 用 1.19 官方说明补充 |
| 科研基准天数 | 不同 Wiki 页出现冲突数字 | 不复制该精确基准公式 |
| 1.19 日期 | 社区表与官方公告／解锁日期混用 | 分开写公告日与正式解锁日 |
| 工业园与夏季测试服 | 不是研究日稳定版规则 | 单列未来与测试内容 |

## 后续史实研究应单独进行

确定时期与主要地区后，再研究兵源制度、军官与辅助职责、运输组织、粮秣来源、装备与训练。实际考据可以调整配置，不应迫使已经清楚分层的库存、编制和历史事件系统全部重写。

本页不列未阅读资料作为已验证证据，也不把同一官方文章的单篇入口和聚合正文算成两份独立证明。
