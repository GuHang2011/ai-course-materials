# 按问题阅读课程资料

本页于 2026-11-03 根据已上传的六份课程文字稿整理。下面的练习是后续备课建议，没有新增课堂实验结果。

| 材料 | 核心问题 | 建议留下的练习产物 |
| --- | --- | --- |
| [AI 基础课程地图](../materials/06-ai-course-outline.md) | 16 个课次，从学习任务、模型概念到综合实践。 | 选一个课次，写出学习目标与可检查的作业产物。 |
| [AI 应用与人工复核](../materials/02-ai-application.md) | 工具选型、提示词、生图、PPT 与智能体的任务组织。 | 保留生成初稿与人工修订，说明修改原因和信息来源。 |
| [大数据技术概述](../materials/03-big-data-overview.md) | 数据特征、处理层次与计算框架之间的关系。 | 围绕一个任务，画出采集、存储、计算与展示的分工。 |
| [Spark 的设计与运行](../materials/04-spark-architecture.md) | Driver、Executor、RDD、惰性执行与 Shuffle。 | 解释哪个操作触发计算，再用 Spark UI 核对 Stage 划分。 |
| [智能腕表 GUI 设计](../materials/05-watch-gui.md) | 小屏信息层级、触控反馈、消息响应与界面刷新。 | 画一个界面，同时说明空状态、等待状态和失败提示。 |
| [智能制造案例阅读](../materials/01-smart-manufacturing.md) | 通过三类行业案例比较离散制造与流程制造。 | 引用前区分事实与分析，逐项核对企业案例中的效果数字。 |

## 三条阅读路线

1. **AI 应用**：先看课程索引，再选一个办公或设计任务，记录输入、工具与日期、输出、人工修改和事实来源。工具的当前功能应以官方说明为准。
2. **数据计算**：先明确数据从哪里来、需要什么结果，再学习 Spark 的转换与行动操作。运行示例时保留 Spark / Python / Java 版本、输入数据、命令、输出和 Spark UI 的执行信息。
3. **界面开发**：先画小屏线框图，再描述操作触发的消息及状态变化。把“点击后有反馈”和“底层业务完成”分别检查。

## 讲解时容易混淆的点

- Spark 的 `map`、`filter` 等转换通常构建计算依赖，行动操作触发执行；不要把所有 API 调用都描述成立即运行一个新作业。
- 是否发生 Shuffle 还与分区器和具体算子有关，不能只凭 `join` 名称判断每次都需要重新分区。RDD 是核心抽象之一，结构化处理还应查阅对应版本的 DataFrame / SQL 文档。
- 原材料涉及的部署方式和平台功能具有版本背景；选定 Spark 版本后再核对支持的集群管理方式。教材中的历史选项不自动等于当前版本建议。
- GUI 消息处理与刷新是讲解线索，不意味着浏览器或不同嵌入式图形库都使用同一组函数。
- 企业案例的经营数据和效率提升数字应对应到具名来源、日期与统计口径；暂不能核对的数字不放进个人成果介绍。

## 与公开工程项目对照

- [禾镜 FieldLens](https://guhang2011.github.io/fieldlens/)：体验预设标注、记录复核与导出，讨论 AI 输出如何进入人工操作流程；演示不运行真实病害模型。
- [沭阳之家](https://github.com/GuHang2011/shuyang-home)：阅读多端状态和事项汇总实现，讨论界面状态、业务权限与完成状态如何区分。

## 补充阅读

- [Apache Spark RDD Programming Guide](https://spark.apache.org/docs/latest/rdd-programming-guide.html)
- [Apache Spark Cluster Mode Overview](https://spark.apache.org/docs/latest/cluster-overview.html)
- [Apache Spark SQL Guide](https://spark.apache.org/docs/latest/sql-programming-guide.html)

以上为官方文档入口，`latest` 会随版本变化。正式练习应记录实际使用的文档和运行版本。
