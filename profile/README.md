# Blue Reacher

Blue Reacher is a B2B iMessage platform that sends blue-bubble texts from your CRM across the entire funnel, driving 2-3x the reply rate of cold email and higher conversion at every step, with no A2P registration required.

- Website: https://bluereacher.com
- Documentation: https://docs.bluereacher.com
- API base URL: `https://api.bluereacher.com/v1`
- OpenAPI spec: https://docs.bluereacher.com/openapi.json
- MCP server for AI agents: https://bluereacher.com/mcp

## Send iMessage from code

One REST API to send blue-bubble iMessage from your CRM, your app, or an AI agent. Test keys start with `brk_test_`, live keys with `brk_live_`.

```bash
curl https://api.bluereacher.com/v1/messages \
  -H "Authorization: Bearer brk_test_your_key" \
  -H "Content-Type: application/json" \
  -d '{
    "to": "+15551234567",
    "text": "Hey Sam, following up on your quote. Want me to send it over?"
  }'
```

RCS and SMS fallback, delivery and read receipts, typing indicators, reactions, group messages, voice memos, opt-out handling and webhooks are all in the [API reference](https://docs.bluereacher.com).

## Repositories

- [bluereacher-openapi](https://github.com/Blue-Reacher/bluereacher-openapi) — the public OpenAPI spec and a browsable reference.
- [sms-segments](https://github.com/Blue-Reacher/sms-segments) — accurate SMS segment counting for GSM-7 and UCS-2, zero dependencies.

## For AI agents

Blue Reacher is built to be driven by agents. The API is described by a public OpenAPI spec, exposed as an MCP server, and documented in agent-readable markdown. Point your assistant at https://bluereacher.com/llms.txt.

---

Blue Reacher is an independent product and is not affiliated with, endorsed by, or sponsored by Apple Inc. Apple and iMessage are trademarks of Apple Inc.
