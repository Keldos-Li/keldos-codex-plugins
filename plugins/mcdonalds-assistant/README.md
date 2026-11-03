# 麦当劳助手

在 Codex 桌面端使用麦当劳中国的查询工具和交互面板，浏览活动、查询优惠券、计算营养、选择餐厅餐品，并让 AI 根据预算和偏好推荐搭配。

## 安装与授权

1. [添加 Keldos Codex Plugins 插件市场](../../README.md#添加插件市场)。
2. 安装麦当劳助手：

   ```sh
   codex plugin add mcdonalds-assistant@keldos-codex-plugins
   ```

3. 在桌面端按提示连接麦当劳 MCP 服务，在授权页面填写自己的麦当劳 MCP Token。可从[麦当劳 MCP 平台](https://open.mcd.cn/mcp)获取 Token。
4. 新建聊天，输入“打开麦当劳面板”。

## 功能

- 浏览活动：查看麦当劳近期营销活动与优惠信息。
- 优惠券：查看可领取优惠券和个人卡包，在面板确认后领取优惠券。
- 营养计算器：选择餐品与份数，计算能量、蛋白质、脂肪、碳水化合物和钠，并分析营养组合。
- 点餐：搜索餐厅、浏览真实菜单、选择餐品、计算价格，根据预算和偏好推荐搭配。
- 我的积分：查看积分余额、到期信息与积分商城商品。

## 使用截图

### 浏览活动

![浏览麦当劳活动](https://github.com/user-attachments/assets/2cf0dee7-302d-4438-ae17-b05917f7a543)

### 营养计算器

![计算餐品组合的营养](https://github.com/user-attachments/assets/71fe9402-0afe-4c10-9c66-75aec03aa3cb)

### AI 推荐点餐

![按预算和偏好推荐餐品](https://github.com/user-attachments/assets/cb53fcb4-f752-4fc3-b2d9-acafc24e5886)

## 账户连接

服务加密保存使用者授权的麦当劳 MCP Token。可在[连接管理](https://mcd-mcp.keldos.chatgpt.site/oauth/connections)中解除授权并删除保存的 Token。

点餐面板用于餐品选择、推荐和计价。服务不支持下单、支付和积分兑换。

[反馈问题](https://github.com/Keldos-Li/keldos-codex-plugins/issues) · [返回插件市场](../../README.md)
