---
name: podcast-research
description: Use when the user asks what a podcast, YouTube channel, host or guest said about a topic, wants a quote or timestamp from a show, or wants to add a show or video to their PodPast library.
---

# Podcast research with PodPast

PodPast is the user's library of podcast and YouTube transcripts (their "Pod"). The `podpast` MCP server in this plugin reaches it. The first call asks the user to sign in; if a tool reports the server is not authenticated, tell them to run `/mcp` and sign in to PodPast.

## Picking a tool

- A question about what the shows said: `ask_pod`. It returns a cited answer. Keep the citations and links when you show it.
- An exact quote or passage: `search_pod`. It returns ranked passages with timestamps.
- What is in the library, or whether a show finished processing: `get_pod_info`.
- The full text of one episode, for summarizing or quoting at length: `get_episode_transcript`.

## Adding a show

1. Podcast by name: `search_podcasts`, and let the user pick if there are several matches.
2. `analyze_podcast` on the chosen feed. It reports how many episodes have a free transcript and how many transcription minutes the rest would use. It spends nothing.
3. Give the user the choice it implies (free episodes only, or all episodes using minutes), then `add_to_pod`.

A YouTube channel or video link goes straight to `add_to_pod`.

## Costs

Adding episodes that already have a transcript is free. Paid transcription uses the user's transcription minutes; confirm with the user before choosing it. `buy_credits` only returns a checkout link; the user pays on podpast.ai.
