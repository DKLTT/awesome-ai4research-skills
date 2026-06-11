# Contribution Guide 贡献规范
## 1. 新增Skill强制规则
1. 必须使用 templates/skill-entry.md.tpl 统一模板，禁止自定义格式
2. 完整填写 Cover Tags，标记该Skill覆盖的所有科研流程
3. 一体化多能力套件必须填写 Source Suite 字段溯源
4. GPL强传染协议项目不推荐接入内部OpenAIR平台
5. 完整填写 OpenAIR Adapt Info，提供平台改造参考

## 2. 文件存放规则
一个覆盖多流程的Skill，需要复制条目粘贴到**所有对应**skills/分类md文件中

## 3. 提交备注规范
feat: add [Skill名称] to Hypothesis Generation
docs: 更新OpenAIR接入教程