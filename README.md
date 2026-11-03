# 麦当劳助手（分发版）

在 Codex 桌面端使用麦当劳活动、优惠券、营养、餐厅餐品、推荐和积分功能。

添加插件市场：

```sh
codex plugin marketplace add Keldos-Li/mcdonalds-plugins
```

重新启动桌面应用，在插件目录选择“麦当劳插件”，安装“麦当劳助手（分发版）”，按提示完成 OAuth 授权。授权页面需要填写使用者自己的麦当劳 MCP Token，可从 https://open.mcd.cn/mcp 获取。

新建聊天，输入“打开麦当劳面板”。连接管理与解除授权：https://mcd-mcp.keldos.chatgpt.site/oauth/connections 。

服务加密保存每个用户授权的麦当劳 Token。授权范围包含查询与领取优惠券；领取操作需要面板明确确认。服务不支持下单、支付和积分兑换。
