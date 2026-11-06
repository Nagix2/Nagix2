<p align="right"><a href="README.md">Português</a> · <b>English</b></p>

<p align="center">
  <img src="assets/banner-en.svg" alt="Hi, I'm Christian, creator of O.R.L.A." width="100%">
</p>

<p align="center">
  <img src="assets/digitando-en.svg" alt="Terminal: christian, software developer, creator of O.R.L.A.; developer tools for people who build software with AI agents" width="100%">
</p>

## About me

Software developer focused on **developer tools** for people who build software with AI agents.
I work with **Electron, Node.js and JavaScript**, and **Claude Code** and **Codex** are part of my daily workflow:
I define the architecture, split the work, review the code and own the final polish.

Right now I'm building **O.R.L.A.**, a Windows desktop app that brings your agents' status, permission requests
and notifications together on an island at the top of your screen.

Follow the development of O.R.L.A. on Instagram: **[@chr.devz](https://www.instagram.com/chr.devz/)**

---

## Featured project · O.R.L.A.

<p align="center">
  <img src="assets/ilha.webp" alt="Recording of the real island: it opens on Agents, Codi asks permission to run npm test, the request is approved with one click, the island closes and shows that Clô is done" width="100%">
</p>

<p align="center"><sub>Recorded from the real app, in test mode with sample data. The app UI is in Portuguese.</sub></p>

<p align="center"><b>Your AI agents on an island at the top of your screen.</b><br>
<sub>O.R.L.A. (<i>Orchestration &amp; Response Layer for Agents</i>) shows Claude Code, Codex and your other agents as <b>Prisms</b>, little glass creatures.
It tells you when they finish or need permission, and you answer right there, without hunting for each agent's window.</sub></p>

<table>
  <tr>
    <td align="center" width="25%"><h3>O</h3><b>Orchestrates</b><br><sub>One request becomes a plan, split across your agents.</sub></td>
    <td align="center" width="25%"><h3>R</h3><b>Responds</b><br><sub>Permissions and questions become buttons. Plus dictation in any app.</sub></td>
    <td align="center" width="25%"><h3>L</h3><b>Logs</b><br><sub>Notes, an automatic journal and a summary of what each agent did.</sub></td>
    <td align="center" width="25%"><h3>A</h3><b>Alerts</b><br><sub>Done, failed or waiting on you: the Prism lets you know right away.</sub></td>
  </tr>
</table>

### The crew

Every agent gets a Prism with its own shape, glass and personality. They breathe, blink, follow your mouse and react to what's going on.

<p align="center">
  <img src="assets/turma-en.svg" alt="The Prism crew: O.R.L.A., Clô, Codi, Groove, Gemi, Copi, Cursi, Opi, Ampi and Agy" width="100%">
</p>

### Inside the app

<table>
  <tr>
    <td width="50%"><img src="assets/orla-agentes.png" alt="Agents tab: who is working right now and what changed"><p align="center"><sub><b>Agents</b> · who is working and what changed</sub></p></td>
    <td width="50%"><img src="assets/orla-fluxo.png" alt="Flow tab: each agent's path, from the conversation to the files"><p align="center"><sub><b>Flow</b> · from the conversation to the files, live</sub></p></td>
  </tr>
  <tr>
    <td width="50%"><img src="assets/orla-app.png" alt="Prism library with 44 glass models"><p align="center"><sub><b>Prism library</b> · 44 glass models</sub></p></td>
    <td width="50%"><img src="assets/orla-ilha.png" alt="The island open, with Clô and Codi working"><p align="center"><sub><b>The island</b> · open at the top of the screen</sub></p></td>
  </tr>
</table>

<p align="center"><sub>Demo-mode screenshots. Everything runs on your PC, with no telemetry. The source is private and the download is coming soon.</sub></p>

### By the numbers

<p align="center">
  <img src="assets/numeros-en.svg" alt="18.7k lines of code, 78 integrations, 8 agents supported, 44 Prism models, 100% local with no telemetry" width="100%">
</p>

### How it was built

<p align="center">
  <img src="assets/linha-do-tempo-en.svg" alt="O.R.L.A. timeline, from the first release to 78 integrations" width="100%">
</p>

<details>
<summary><b>Architecture</b></summary>
<br>

```mermaid
flowchart LR
  subgraph AG["AI agents"]
    A1["Claude Code"]
    A2["Codex"]
    A3["Copilot CLI · Cursor<br/>OpenCode · Amp"]
  end
  A1 -- "hooks" --> M
  A2 -- "session logs" --> M
  A3 --> M
  C["Integrations<br/>GitHub · Vercel · Gmail · stores"] --> M
  V["Voice and dictation"] --> M
  M["Main process<br/>Electron · Node.js"]
  M --> I["Island at the top of the screen"]
  M --> J["App window"]
  M --> P["Desktop Prism"]
  M --> T["ESP32 desk display"]
  M <--> N["Notes vault<br/>Markdown"]
  classDef orla fill:#8a78ff,stroke:#b3a5f6,color:#fff
  class M orla
```

- **Local-first:** agents are read from the logs and hooks they already write on your machine. Nothing leaves your PC unless you turn it on.
- **Prisms rendered in SVG** by a custom engine: glass, caustics, particles, eyes that follow the mouse and 14 outfits.
- **Nothing runs without your OK:** every permission needs your click or your key.
- **Tested:** unit tests and end-to-end tests of the running app, with reference screenshots.

</details>

---

## Stack

| Area | Technologies |
|---|---|
| Desktop | Electron · Node.js · JavaScript · HTML · CSS |
| Graphics | SVG, with a custom character and animation engine |
| Windows | PowerShell · C# (.NET) |
| Hardware | ESP32 |
| AI | Claude Code · Codex · MCP · OpenRouter · Ollama · LM Studio |
| Build | electron-builder · esbuild · Git |

---

<p align="center">
  <img src="assets/prism-orla.svg" alt="O.R.L.A., happy" width="72"><br>
  <b>On the edge of your screen.</b><br>
  <sub><a href="https://www.instagram.com/chr.devz/">Instagram @chr.devz</a></sub>
</p>
