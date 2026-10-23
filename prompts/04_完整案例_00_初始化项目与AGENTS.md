在 output/ 下初始化温度换算案例，只有五个同级项目：output/docs-project、output/mock-project、output/frontend-project、output/backend-project、output/test-project。

初始化时立即创建 output/AGENTS.md 和每个项目的 AGENTS.md，写清职责、知识入口、相对路径约定、技术栈、验证要求与跨项目同步规则。不要将 SQLite 建为项目；它是未来后端项目中的一个数据库文件。

生成的所有 AGENTS.md（父级及五个项目）均使用英文撰写标题、说明和规则；引用已有中文文件名时保留实际路径，不为语言要求重命名文件。产品页面与业务文档仍使用中文。

技术要求：Mock 与正式前端用 Vue 3；后端用 Spring Boot；数据库文件用 SQLite；独立测试项目用 Playwright。依赖版本在实现阶段核对并锁定，命令和脚本兼容 Windows、macOS、Linux。

output/docs-project 本身就是知识库根目录，不再增加 knowledge/ 层。根目录维护 README.md、AGENTS.md 和 00_索引.md；按参考采集、产品设计、系统设计、测试设计和实施验证分阶段保存结构化 Markdown，保存确认需求、各阶段输入 prompt、设计产物、部署记录和测试证据；建索引，附件归阶段同级 assets/。不保存用户原话。

目标：参考公开网页的一个单一功能，完成华氏转摄氏的 B/S 示例。正式前端必须调用真实后端计算，Mock 只提供原型交互。下一步先采集参考，再根据参考和目标确定产品与系统设计。

本阶段只初始化项目与工作约定，不提前设计数据库表、不实现业务代码、不提交 Git。
