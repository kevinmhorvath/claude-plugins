# kevinmhorvath-hub — Claude Code plugin marketplace

A single hub for [Kevin Horvath's](https://github.com/kevinmhorvath) Claude Code plugins.
Add it once and install any plugin below.

## Add the marketplace

```
/plugin marketplace add kevinmhorvath/claude-plugins
```

## Plugins

| Plugin | What it does | Install | Source |
|---|---|---|---|
| **threat-intel-toolkit** | Defensive IOC + CVE triage on free, key-free open-source intel — a subagent plus two skills (`threat-intel-lookup`, `exploit-availability-check`). No API keys. | `/plugin install threat-intel-toolkit@kevinmhorvath-hub` | [repo](https://github.com/kevinmhorvath/threat-intel-toolkit) |
| **theboardroom** | An AI executive board of directors (CEO, CFO, COO, CLO, CISO personas) that debates a business idea from each role and delivers an integrated Go/No-Go board memo. | `/plugin install theboardroom@kevinmhorvath-hub` | [repo](https://github.com/kevinmhorvath/theboardroom) |

## How it works

This repository is a **catalog** — it holds only `.claude-plugin/marketplace.json`, which points at
each plugin's own repository via a `github` source. The plugin code stays in those repos; this hub
just lists them so they install from one place. Each plugin also remains independently installable
from its own repository, so existing install instructions keep working — this hub is an additional
front door, not a replacement.

Adding a plugin later is a one-entry edit to `marketplace.json`: copy a `github` source block and
change the `repo`. Updates flow automatically — `/plugin marketplace update kevinmhorvath-hub` pulls
the latest catalog, and each plugin tracks its source repo.
