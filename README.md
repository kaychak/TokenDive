# 🌊 TokenDive

**Every token takes you deeper.**

TokenDive turns the coding-agent usage already sitting on your disk into an
ocean expedition. You keep coding; a submarine keeps descending. Somewhere
around 1,000 m the water goes black and things start to glow.

It lives in your macOS menu bar. It never interrupts you. Once in a while it
tells you something surfaced.

---

## Not released yet

There is nothing to download here today. This page exists so there is somewhere
to ask questions and report problems before there is.

**Watch this repository** to hear when there is a build.

## What it does

**Depth instead of numbers.** `1,519 m · Midnight Zone` means more than
`412,883,109 tokens`, which is the point. Depth accumulates day by day and never
goes backwards.

**A daily cap, so burning tokens is pointless.** Past a per-day ceiling, extra
tokens buy zero depth. The real axis of progression is *days you showed up*, not
tokens spent.

**Species you find, not levels you grind.** 100 marine species across nine
zones, each at roughly its real depth, each with one fact worth reading. Every
scientific name is checked against [WoRMS](https://marinespecies.org) and every
depth against [OBIS](https://obis.org). You cannot meet an anglerfish in a coral
reef.

**And it ends.** There is a bottom, about a year of real use away. What happens
when you get there is deliberately not written down here.

## What it reads

Four locations, all on your own machine:

| Agent | Where |
|---|---|
| Claude Code | `~/.claude/projects` |
| Codex CLI | `~/.codex/sessions` |
| Cursor | `~/Library/Application Support/Cursor` |
| Pi agent | `~/.pi/agent` |

From those files it takes **token counts and timestamps, and nothing else**.
Prompts and code are dropped where the file is parsed: the internal record has
no field that can hold text.

macOS will not ask you to approve any of this, because those paths are not the
kind the system protects. That is worth knowing rather than being reassured by —
**any app you run outside the App Store can read them without asking.** So the
claims here are built to be checked instead.

## What it sends

Nothing. The app contains no HTTP client at all — no `urllib.request`, no
`http`, no TLS library — which you will be able to confirm on a copy you have
downloaded, without trusting anybody:

```
unzip -l /Applications/TokenDive.app/Contents/Resources/lib/python311.zip \
  | grep -cE 'urllib/request|http/|ssl'
```

That prints `0`. A firewall such as [LuLu](https://objective-see.org/products/lulu.html)
will tell you the same thing from outside: no outbound connections, ever.

The app says all of this about itself too, under **What TokenDive reads…** in
its own menu — generated from the code that does the reading, rather than typed
out beside it.

Everything it writes lives in `~/.tokendive`.

## Something wrong, or something to say

[Open an issue](../../issues). If a number looks wrong, the menu has
**Diagnostics…**, which copies a short report — version, what logs it found,
what it computed. No prompts, no file names, no paths beyond the four above. It
is meant to be pasted in public.

## Terms

Free to use, and not open source. Copyright © 2026 kaychak. All rights
reserved.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED. IN NO EVENT SHALL THE AUTHOR BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY ARISING FROM THE SOFTWARE OR THE USE OF IT.

The full terms ship with the app.
