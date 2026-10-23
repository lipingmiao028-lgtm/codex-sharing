先读 output/test-project/AGENTS.md、知识索引及已完成的产品、系统、测试设计，保存本阶段输入到 output/docs-project/06_UI测试/阶段输入.md。

在 output/test-project 使用 UI 测试 SKILL；尚未创建时按“UI 测试 SKILL 创建”输入在当前用户主目录下的全局技能目录建立 .agents/skills/ui-test/SKILL.md，再读取并遵循它。

以 output/docs-project/03_测试设计/测试设计.md（包含页面 URL）作为输入，先检查已有脚本；回归时直接复用有效脚本，不重复生成。按用例 URL 遍历相关页面并确认测试点，仅对未覆盖或变化的用例新增或更新 Playwright 页面操作脚本，再实际执行。测试启动 Vue 3 前端和 Spring Boot 后端；正常换算验证真实接口。SQLite 核验以系统设计为准，Mock 与异常注入单列。用 expect 等待，检查页面和控制台异常，主页面与关键状态截图放 output/docs-project/06_UI测试/assets/。

本次允许修复案例内代码或测试缺陷；分析原因后修复并复测，不删除或放宽断言掩盖失败。只停止本轮启动的服务。

执行报告写 output/docs-project/06_UI测试/执行报告.md，记录实际命令、平台、通过/失败/未执行、证据相对链接及剩余问题；更新索引。没有 Windows 真机时不宣称 Windows 已验证。

Playwright 测试代码、运行产物和失败 trace 均保存到 output/test-project/ 内。
