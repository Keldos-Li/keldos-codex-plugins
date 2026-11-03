*该插件为技术演示。*

# 麦当劳助手

在 Codex 的**交互面板/工作台**中，**实时**调用麦当劳的 MCP tools：
- 查看活动、查询优惠券、计算营养、选择餐厅餐品、点单下单；
- 调用会话中的模型，让 AI 根据要求**帮你点单**。

## 使用截图

**AI 推荐点餐**
![按预算和偏好推荐餐品](https://github.com/user-attachments/assets/cb53fcb4-f752-4fc3-b2d9-acafc24e5886)

**浏览活动**
![浏览麦当劳活动](https://github.com/user-attachments/assets/2cf0dee7-302d-4438-ae17-b05917f7a543)

**营养计算器**
![计算餐品组合的营养](https://github.com/user-attachments/assets/71fe9402-0afe-4c10-9c66-75aec03aa3cb)

## 安装与授权

1. 添加插件市场：

   ```sh
   codex plugin marketplace add Keldos-Li/keldos-codex-plugins
   ```
   
2. 安装麦当劳助手：

   ```sh
   codex plugin add mcdonalds-assistant@keldos-codex-plugins
   ```

3. 浏览器自动打开授权页。按提示连接，填写自己的麦当劳 MCP Token。可从[麦当劳 MCP 平台](https://open.mcd.cn/mcp)获取 Token。

## 功能

- 浏览活动：查看麦当劳近期营销活动与优惠信息。
- 优惠券：查看可领取优惠券和个人卡包，在面板确认后领取优惠券。
- 营养计算器：选择餐品与份数，计算能量、蛋白质、脂肪、碳水化合物和钠，并分析营养组合。
- 点餐：搜索餐厅、浏览真实菜单、选择餐品、计算价格，根据预算和偏好推荐搭配。
- 我的积分：查看积分余额、到期信息与积分商城商品。

## 账户连接

服务加密保存使用者授权的麦当劳 MCP Token。可在[连接管理](https://mcd-mcp.keldos.chatgpt.site/oauth/connections)中解除授权并删除保存的 Token。

目前，为了避免 AI 可能出现的问题，关停了真正的下单、支付和积分兑换功能（实际支持）。
