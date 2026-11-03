---
name: mcdonalds-workspace
description: Use for McDonald’s China activities, coupons, food calories and nutrition, restaurant menus, meal selection, price checks, points, and the conversation side panel.
---

# McDonald’s workspace

Use this plugin’s registered OAuth connection for its interface and McDonald’s business tools. Users enter their McDonald’s MCP Token on the service’s authorization page at https://mcd-mcp.keldos.chatgpt.site. The backend encrypts the provider credential and issues separate OAuth access credentials to the host. Users can revoke the connection and delete the stored provider credential at https://mcd-mcp.keldos.chatgpt.site/oauth/connections. Never request credentials in chat, read local credential files, or put credentials in source, logs, browser storage, or tool results.

Open `open_mcd_workspace` when the user requests the panel. It advertises a thread entrypoint. Activity, coupon, restaurant, menu, price and points queries run directly through the panel’s tools. Their actual business results are in `structuredContent.data`.

## Recommendations and nutrition analysis

When a panel request arrives in the conversation:

1. Read `read_mcd_order_state` with its `sessionId`. Check the exact pending request ID and arguments. Keep this existing session.
2. For `recommend`, query the selected restaurant’s actual menu and full details of the proposed meals using this plugin’s McDonald’s tools. Respect the requested budget, preferences and required combo choices. Call `complete_mcd_order_action` with the matching `sessionId`, `requestId` and `data: {explanation, details: [originalMealDetails], items: [{productCode, quantity, modification?, roundList?}]}`. The server rechecks meal details with McDonald’s before saving the basket.
3. For `analyze`, explain the real item quantities and nutrition totals in the pending arguments. Return `data: {text}` through `complete_mcd_order_action`. Do not invent nutrient values or make unsupported medical claims.
4. If a request cannot be completed, report the actual business error through `error` with the same session and request IDs. Keep conversation replies brief because the panel displays the returned result.

Business query completion is handled by the service. Do not fabricate business results or complete a pending provider query yourself. Coupon claims require the panel’s explicit confirmation. Never automatically replay an uncertain write. Panel requests prepare meal selections and prices; do not create orders, make payments or redeem points from those requests.

Keep the interface focused on business information and preserve its five sections: activities, coupons, nutrition, ordering and points.
