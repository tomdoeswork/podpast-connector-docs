# PodPast

PodPast is a hosted connector for Claude and Claude Code. Add the podcasts and YouTube channels you follow, and Claude can answer a question across all of them at once. Each claim in the answer points to the episode and timestamp it came from. There is nothing to install.

**Homepage:** https://podpast.ai
**Examples:** https://podpast.ai/examples
**Live demo (no signup):** https://podpast.ai/demo
**Works with:** Claude (web, desktop, mobile) and Claude Code
**Transport:** Streamable HTTP (remote, hosted)
**Connector URL:** `https://api.podpast.ai/mcp`
**Auth:** OAuth (sign in with your PodPast account)
**MCP registry name:** `io.github.tomdoeswork/podpast`

## What it does

- Add a podcast or YouTube channel by name or URL.
- Ask one question and search every episode in your library, across several shows at once.
- Get an answer with numbered sources that link to the episode and timestamp.
- New episodes of the shows you follow are checked every hour.

## Install

**Claude**

1. Create a free account at https://podpast.ai/login.
2. In Claude, open Settings, then Connectors, then Add custom connector.
3. Paste `https://api.podpast.ai/mcp` and sign in with your PodPast account.

**Claude Code**

```
claude mcp add --transport http podpast https://api.podpast.ai/mcp
```

Then run `/mcp` in Claude Code and sign in.

## Tools

- `search_podcasts` - Find a podcast by name.
- `analyze_podcast` - Check how many episodes are available for a show before adding it.
- `add_to_pod` - Add a show to your Pod.
- `ask_pod` - Ask a question across the shows you follow and get a cited answer.
- `search_pod` - Search your Pod and get ranked transcript passages with timestamps.
- `get_pod_info` - See what is in your Pod.
- `get_episode_transcript` - Get a single episode's transcript.
- `refresh_pod` - Pull the latest episodes for a show.
- `remove_episode` - Remove an episode from your Pod.
- `retry_podcast` - Retry a show that failed to process.
- `check_pod_credits` - Check your transcription-minute balance.
- `buy_credits` - Buy more transcription minutes.

## Pricing

- **Free, $0, no card:** 2 podcasts, the last 25 episodes of each, 30 questions a month, up to 50 YouTube videos.
- **Pro, $12 a month or $108 a year:** 25 podcasts, the last 200 episodes of each, 1,500 questions a month, 100 transcription minutes a month.
- **Transcription packs:** 1,000 minutes for $10 or 3,000 minutes for $30, for episodes with no published transcript. Minutes do not expire.

Paid checkout is United States only. Details: https://podpast.ai/pricing

## Support

support@podpast.ai
