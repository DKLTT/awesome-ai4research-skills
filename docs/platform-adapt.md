# OpenAIR 平台Skill改造接入完整流程
## 完整步骤
1. 克隆开源Skill源码，修复依赖版本冲突
2. 开发适配器Wrapper：统一平台标准出入参JSON
3. CLI脚本改造为FastAPI HTTP微服务
4. 安全沙箱加固：目录隔离、资源限制、输入注入过滤
5. 编写Dockerfile打包镜像，推送内部镜像仓库
6. 基于skill-meta.json模板生成注册配置，上传平台Skill管理中心
7. 在线调试 + Agent全链路测试，灰度放量上线

## 平台标准入参 Request
```json
{
  "request_id": "全局追踪ID",
  "user_id": "平台用户ID",
  "skill_params": {},
  "meta": {"auth_token": "内部鉴权凭证", "timeout": 30}
}

{
  "code": 0,
  "msg": "success",
  "data": {},
  "trace_id": "链路ID",
  "cost_ms": 执行耗时
}