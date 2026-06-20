# PodPast

Hosted Claude connector. Turns the podcasts and YouTube shows you already follow into a searchable, askable knowledge source inside Claude. Ask what a guest said and get the answer back with the exact quote and the timestamp it came from.

**Homepage:** https://podpast.ai
**Status:** New, solo-built, Claude-native. Runs in Claude.ai today.
**Transport:** Streamable HTTP (remote / hosted)
**Auth:** OAuth (sign in with your PodPast account)

## What it does

- Add a podcast or YouTube show by name or URL.
- Ask Claude what a guest said, what an episode covered, or where a specific claim came from.
- Get the answer back with the exact quote and the timestamp it came from.

## Install

1. Create an account at https://podpast.ai and copy your personal PodPast connector URL from your account.
2. In Claude.ai, open Settings - Connectors - Add custom connector.
3. Paste your connector URL and sign in with your PodPast account.

> Each PodPast account gets its own connector URL tied to your Pod - paste the one shown in your account, not a shared link.

## Tools

- `add_to_pod` - Add a show to your Pod.
- `search_podcasts` - Find a podcast by name.
- `analyze_podcast` - Check how many episodes are available for a show before adding.
- `ask_pod` - Ask a question across the podcasts you follow.
- `search_pod` - Keyword-search across your Pod.
- `get_pod_info` - Get the current state of your Pod.
- `get_episode_transcript` - Get a single episode's transcript.
- `refresh_pod` - Refresh a show with the latest episodes.
- `remove_episode` - Remove an episode from your Pod.
- `retry_podcast` - Retry a failed transcription.
- `check_pod_credits` - Check your transcription-minute credit balance.
- `buy_credits` - Buy more transcription-minute credits.

## Wedge

NotebookLM, but for the podcasts you follow, inside Claude.
