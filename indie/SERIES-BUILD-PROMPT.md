# SERIES-BUILD-PROMPT — Claude, For the Indie (bot vs bot, season one)

Builds the seven claude-musinique episodes one at a time, waiting for feedback
between episodes. Narration is authored and gated but NOT yet human-signed:
the first stop of this run is your GATE P sign-off per episode.

Paste into Claude Code from `books/` (typically `claude --dangerously-skip-permissions`):

```
Build the "Claude, For the Indie" season (musinique/youtube/indie/) one episode at a time, waiting for my feedback between episodes. Never build two in one turn.

Ground truth, read all of it before episode one:
1. musinique/youtube/indie/PLAYLIST.md — the slate and order: indie-in-your-corner → indie-on-schedule → indie-sourced → indie-in-your-voice → indie-on-your-catalog → indie-on-the-pitch → indie-in-your-hands.
2. brutalist-art/MUSINIQUE.md — the charter: fights for the indie musician; Baldwin register (no hedges, direct address, name what you see); RECEIPTS LAW (no source, no verdict); NO FAKE NUMBERS; ROLL-YOUR-OWN LAW (every handoff is a deck piece the viewer keeps); the GRADED EXHIBIT move (exhibits keep their own look).
3. musinique/youtube/indie/RECEIPTS.md — the evidence base. Before building episode 3 (indie-sourced) and any beat with a platform-mechanics claim, re-verify the tier-1 anchors (Spotify for Artists docs; Anthropic docs for scheduled-task constraints) and update RECEIPTS.md with what you confirm. If a claim can't be verified at tier 1–2, soften the narration and flag it to me at the gate.
4. brutalist-art/skills/make/claude-explainer/SKILL.md + brutalist-art/CLAUDE-BRAND.md — the laws, INCLUDING the ILLUSTRATE LAW. Channel claude-musinique: chip @Musinique, voice kokoro am_puck (override ELEVENLABS_VOICE_MUSINIQUE), register Baldwin.
5. medhavy_com/youtube/mcp/remotion-src/ (worked example: OverviewV2 + Illustrations + retinted deckPatterns) and skills/animated-deck/ (pattern library + anim.json gate). Each episode's beat_sheet.json carries a per-beat illustration spec in shot props (kind: concept | pattern | code | exhibit) — build those, adapting the worked example. code-kind beats render the REAL skill-file text in an Onda code-block; exhibit-kind beats use the graded-exhibit move.

Per episode, in order:
1. GATE P: show me the NARRATION-GATE-P.md table plus any receipts-verification changes, and STOP for my sign-off. Narration edits I request reopen the gate; apply, re-show, wait.
2. After sign-off: audio via python3 runtime/scripts/generate_audio.py musinique/youtube/indie/<slug>/ from brutalist-art/ — voice kokoro am_puck. ffprobe → actual_duration_s; conform frames = ceil((mp3 + 0.4) * 30).
3. Composition per the illustration specs; composer chips @Musinique; no caption bar. Render --scale=1.5 → musinique/youtube/indie/<slug>/media/final-cut.mp4.
4. QC: ffprobe; stills of B00 (RESULT lines), every inner beat (no two consecutive beats on the same visual scheme — ILLUSTRATE LAW), the verdict, the handoff, the outro. One terracotta accent on UI beats; exhibits keep their own look.
5. Report: durations, QC findings, path, the episode's DESCRIPTION.md — then STOP and wait: "next" / feedback (patch only affected beats) / "skip" / "stop".

Never publish or upload anything. GATE P is per-episode and never bypassed.
```

## Notes

- Season thesis: bot vs bot — teach the indie to aim machines at their grind
  and walk past the promotion scammers. Every handoff paste is a deck piece;
  the finale audits the viewer's own deck.
- Episode 3's exhibit (the "Spotify Andromeda" guide) is the season's graded
  exhibit — build it with the claude-debunked wheel pattern (exhibit assembles,
  then gets graded), sourced per RECEIPTS.md.
- No previz was rendered in the authoring session (the ILLUSTRATE-LAW visuals
  are bespoke per episode and GATE P precedes all spend) — this run is the
  first render pass.
