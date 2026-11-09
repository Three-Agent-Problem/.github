<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="assets/mark-dark.svg">
    <img src="assets/mark-light.svg" width="96" height="96" alt="">
  </picture>
</p>

<h1 align="center">Three Agent Problem</h1>

<p align="center">Three bodies, one figure eight: agents that keep handing work to each other without colliding.</p>

## Production infrastructure for A2A agents

[A2A](https://a2a-protocol.org) lets agents from different vendors and frameworks call each other. We build what you need once those agents run for real: durable tasks, a human inbox for approvals, credentials for `AUTH_REQUIRED`, traces across hops, and a registry that only lists cards clients can actually use.

| Repository | What it is |
|---|---|
| [**Lagrange**](https://github.com/three-agent-problem/lagrange) | Operator console with a task tree across agents and time in state. An inbox that renders structured-input requests as forms and resumes the task. A credential broker for `AUTH_REQUIRED` (with a [Nango](https://nango.dev) adapter). A push observer for any [a2a-go](https://github.com/a2aproject/a2a-go) agent. |
| [**registry**](https://github.com/three-agent-problem/registry) | `card-lint`, which grades an agent card against A2A 1.0, and a registry that indexes conformant agents by skill and checks they are alive. |
| [**Halo**](https://github.com/three-agent-problem/halo) | A team of Claude Code agents that work together over A2A: an opus lead, haiku, sonnet and opus workers in their own git worktrees, and a reviewer, each with its own address on Lagrange. A lazygit-style TUI shows every message live. `brew install three-agent-problem/tap/halo` |
| [**examples**](https://github.com/three-agent-problem/examples) | Runnable multi-agent apps. Start with **procurement**: quotes, approval, order with push, calendar connection, purchase order. |

Everything is Apache-2.0 and written in Go on the official A2A SDK. Early days, so expect things to change.
