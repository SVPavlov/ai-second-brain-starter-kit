# WhatsApp module (opt-in, Mac first)

Your brain reads your WhatsApp: digests of what came in, and chats filed as client context. **Read-first by design**: sending ships disabled, and the guide explains the risks (unofficial client, personal number) before you decide anything.

This module lives in its own repository (it contains a Go bridge, which does not belong inside a vault):

**Install guide + everything else: https://github.com/SVPavlov/ai-second-brain-module-whatsapp**

Short version: clone, apply two patches (send guard + send-off default), build, pair with your phone, connect the MCP server, copy the two skills (whatsapp-digest, whatsapp-to-brain) into `.claude/skills/`. 30-45 minutes, private machine, Mac first.
