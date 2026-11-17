### My AI agent setup

I run Claude Code and OpenCode as a small crew of agents across a Mac and a Linux server. These repos are the
whole setup:

| Repo | What it is |
| --- | --- |
| [nc-harness](https://github.com/iAmSerathion/nc-harness) | The harness: one CLI (`nc`) for shared rules, roles and skills, a per-folder model policy, shared memory, delegation to OpenCode workers and a lightweight orchestrator. |
| [nc-infra](https://github.com/iAmSerathion/nc-infra) | `nc-work`: one rootless Docker container per agent task, with an egress allow list and no credentials inside, plus a guide for the VPS and Tailscale behind it. |
| [herdr-nc](https://github.com/iAmSerathion/herdr-nc) | My herdr workspace: layouts, themes and cards that show every agent, worker and orchestrator plan live. |
| [nc-memory-template](https://github.com/iAmSerathion/nc-memory-template) | Template for the shared memory the agents read and write. |

Private rules, client policies and the real memory stay in private repos; the public ones ship generic defaults
and an overlay folder to plug your own in.
