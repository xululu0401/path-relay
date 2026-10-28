# 工期接力图
纯前端CPM小项目排程工具。直接打开index.html或用本地HTTP服务运行；无需安装依赖、账号或模型API。

构建：`node build.cjs`。核心测试：`node --test tests/core.test.cjs`。

输入1–12项、ID A–L、工时0–999 h（0.1 h精度）、前置ID；允许0小时里程碑。目标只作差额对照。Kahn拓扑排序、ES/EF前推、LS/LF后推、TF=LS−ES。整数十分之一小时避免浮点误差。存在多条关键路径时标出所有零时差任务，不声称它们组成一条路径。

假设确定工时、无限并行、完成后开始、不含滞后、不设日历。不是资源优化或现实工期保证。CSV/MD/JSON/PNG导出，JSON备份导入；只处理本地输入；显式保存，不自动覆盖。

默认虚构示例：工时和17 h，总工期13 h；C总时差2 h，增加3 h后总工期14 h。

源码：core.js、ui.js、template.html；index.html为内联构建物。封面是原创SVG+PNG。结果卡长名称缩略，完整名称在CSV。
