# CMS 工作流执行器

[English](README.md)

私有 cms-frontend 工作流通过 `changelog-summary` 事件发送按 UTC+8 包含首尾两天的
日期范围，以及可选的 `backend,aiTutor,cmsBackend` 子库键。主库始终参与。
`include_think_and_speak` 默认关闭，默认排除 Think & Speak／AI English Gym
产品线及其 CMS 管理工具；开启后才包含，其他 CMS 模块仍保留。校验后按布尔值转发。
共用执行器默认仍运行原单版本 changelog；summary 模式发现全部标准文件前缀并读取已有 Markdown 附件，按内容筛选 CMS
相关内容，并仅把三个报告文件写入 cms-frontend 私有 Release。保持 `quiet` 开启，
不能在此公开发布报告 artifacts 或正文。复用原 ACCESS_TOKEN、AWS 和 SSM 配置。
先部署 api-meter 的 CMS 汇总种子迁移并发布 repo-toolkit main，再使用此流程。
输入与输出规则见 [CMS 指南](https://github.com/Seechange-edu/cms-frontend/blob/HEAD/docs/changelog-summary.zh-CN.md)。
