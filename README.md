<p align="right"><b>Português</b> · <a href="README.en.md">English</a></p>

<p align="center">
  <img src="assets/banner.svg" alt="Oi, eu sou o Christian, criador da O.R.L.A." width="100%">
</p>

<p align="center">
  <img src="assets/digitando.svg" alt="Terminal: christian, desenvolvedor, criador da O.R.L.A.; ferramentas de desenvolvimento para quem programa com agentes de IA" width="100%">
</p>

## Sobre mim

Desenvolvedor focado em **ferramentas de desenvolvimento** para quem programa com agentes de IA.
Trabalho com **Electron, Node.js e JavaScript**, e uso o **Claude Code** e o **Codex** no dia a dia:
eu defino a arquitetura, divido as tarefas, reviso o código e cuido do acabamento.

Hoje estou construindo a **O.R.L.A.**, um app desktop para Windows que reúne o status, as permissões e os avisos
dos seus agentes numa ilha no topo da tela.

Acompanhe o desenvolvimento da O.R.L.A. no Instagram: **[@chr.devz](https://www.instagram.com/chr.devz/)**

---

## Projeto em destaque · O.R.L.A.

<p align="center">
  <img src="assets/ilha.webp" alt="Gravação da ilha de verdade: ela abre em Agentes, o Codi pede permissão para rodar npm test, o pedido é aprovado com um clique, a ilha fecha e avisa que o Clô terminou" width="100%">
</p>

<p align="center"><sub>Gravação da O.R.L.A. de verdade, em modo de teste com dados de exemplo.</sub></p>

<p align="center"><b>Seus agentes de IA numa ilha no topo da tela.</b><br>
<sub>A O.R.L.A. mostra o Claude Code, o Codex e os seus outros agentes como <b>Prisms</b>, bichinhos de vidro.
Ela avisa quando eles terminam ou pedem permissão, e você responde dali, sem caçar a janela de cada um.</sub></p>

<table>
  <tr>
    <td align="center" width="25%"><h3>O</h3><b>Orquestra</b><br><sub>Um pedido seu vira um plano, dividido entre os seus agentes.</sub></td>
    <td align="center" width="25%"><h3>R</h3><b>Responde</b><br><sub>Permissões e perguntas viram botões. E você dita em qualquer programa.</sub></td>
    <td align="center" width="25%"><h3>L</h3><b>Lembra</b><br><sub>Notas, diário automático e o resumo do que cada agente fez.</sub></td>
    <td align="center" width="25%"><h3>A</h3><b>Avisa</b><br><sub>Terminou, deu erro ou precisa de você: o Prism avisa na hora.</sub></td>
  </tr>
</table>

### A turma

Cada agente ganha um Prism com formato, vidro e jeito próprios. Eles respiram, piscam, olham para o mouse e reagem ao que acontece.

<p align="center">
  <img src="assets/turma.svg" alt="A turma de Prisms: O.R.L.A., Clô, Codi, Groove, Gemi, Copi, Cursi, Opi, Ampi e Agy" width="100%">
</p>

### Por dentro do app

<table>
  <tr>
    <td width="50%"><img src="assets/orla-agentes.png" alt="Aba Agentes: quem está trabalhando agora e o que mudou"><p align="center"><sub><b>Agentes</b> · quem está trabalhando e o que mudou</sub></p></td>
    <td width="50%"><img src="assets/orla-fluxo.png" alt="Aba Fluxo: o caminho de cada agente, da conversa aos arquivos"><p align="center"><sub><b>Fluxo</b> · da conversa aos arquivos, ao vivo</sub></p></td>
  </tr>
  <tr>
    <td width="50%"><img src="assets/orla-app.png" alt="Biblioteca de Prisms com 44 modelos de vidro"><p align="center"><sub><b>Biblioteca de Prisms</b> · 44 modelos de vidro</sub></p></td>
    <td width="50%"><img src="assets/orla-ilha.png" alt="A ilha aberta com o Clô e o Codi trabalhando"><p align="center"><sub><b>A ilha</b> · aberta no topo da tela</sub></p></td>
  </tr>
</table>

<p align="center"><sub>Fotos do modo demonstração. Tudo roda no seu PC, sem telemetria. O código é privado e o download sai em breve.</sub></p>

### Em números

<p align="center">
  <img src="assets/numeros.svg" alt="18,7 mil linhas de código, 78 integrações, 8 agentes suportados, 44 modelos de Prisms, 100% local e sem telemetria" width="100%">
</p>

### Como foi feita

<p align="center">
  <img src="assets/linha-do-tempo.svg" alt="Linha do tempo da O.R.L.A., da primeira versão às 78 integrações" width="100%">
</p>

<details>
<summary><b>Arquitetura</b></summary>
<br>

```mermaid
flowchart LR
  subgraph AG["Agentes de IA"]
    A1["Claude Code"]
    A2["Codex"]
    A3["Copilot CLI · Cursor<br/>OpenCode · Amp"]
  end
  A1 -- "avisos (hooks)" --> M
  A2 -- "registros das sessões" --> M
  A3 --> M
  C["Conexões<br/>GitHub · Vercel · Gmail · lojas"] --> M
  V["Voz e ditado"] --> M
  M["Processo principal<br/>Electron · Node.js"]
  M --> I["Ilha no topo da tela"]
  M --> J["Janela do app"]
  M --> P["Prism solto na área de trabalho"]
  M --> T["Telinha de mesa ESP32"]
  M <--> N["Cofre de notas<br/>Markdown"]
  classDef orla fill:#8a78ff,stroke:#b3a5f6,color:#fff
  class M orla
```

- **Tudo local:** os agentes são lidos pelos registros e avisos que eles mesmos já gravam no PC. Nada sai do computador sem você ligar.
- **Prisms desenhados em SVG** por um motor próprio: vidro, cáusticas, partículas, olhos que seguem o mouse e 14 roupas.
- **Nada roda sem o seu OK:** toda permissão depende do seu clique ou da sua tecla.
- **Testado:** testes automáticos de unidade e do app aberto, com fotos de referência das telas.

</details>

---

## Stack

| Área | Tecnologias |
|---|---|
| Desktop | Electron · Node.js · JavaScript · HTML · CSS |
| Gráficos | SVG, com motor próprio de personagens e animação |
| Windows | PowerShell · C# (.NET) |
| Hardware | ESP32 |
| IA | Claude Code · Codex · MCP · OpenRouter · Ollama · LM Studio |
| Build | electron-builder · esbuild · Git |

---

<p align="center">
  <img src="assets/prism-orla.svg" alt="A O.R.L.A. feliz" width="72"><br>
  <b>Na orla da sua tela.</b><br>
  <sub><a href="https://www.instagram.com/chr.devz/">Instagram @chr.devz</a></sub>
</p>
