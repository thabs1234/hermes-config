# hermes-config

## Overview

Repository for Hermes Agent configuration using 9router local AI proxy.

### What this configures

- **API endpoint**: `http://127.0.0.1:20128/v1` (9router local proxy)
- **Default model**: `openai/gpt-4o-mini`
- **Streaming**: WebSocket enabled for real-time chat

### Changes made

Switched from OpenRouter direct API to 9router local proxy bridge for:
- No external API key required
- Unified OpenAI-compatible endpoint
- WebSocket streaming support

### Verification

```bash
curl -X POST http://127.0.0.1:20128/v1/chat/completions \
  -H 'Content-Type: application/json' \
  -d '{"model":"openai/gpt-4o-mini","messages":[{"role":"user","content":"Hello"}]}'
```