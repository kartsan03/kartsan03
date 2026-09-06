## whoami

Most of what I build never shows up here. The public stuff is whatever stayed useful more than once. That usually means pipelines that don't wake me at 3am, plus checks that catch bullshit before a person has to. Sometimes I end up on Solana, when money has to settle on-chain and I refuse to babysit it.

I care about systems that stay honest under load. Wrong assumptions should fail loud. Scrapers and ETL leave an audit trail. I judge LLM output offline instead of by vibes. Agent side-effects wait for a human. If a tool only works in a demo gif, it isn't finished.

UA / RU / EN.

### Currently

- Offline gates for LLM output (schema, snapshots, CI exit codes — no model call at gate time)
- Human-in-the-loop for agent tool side-effects
- Messy public-data pipelines that still leave an audit trail
- Solana tooling when something actually has to settle on-chain

### Stack

![Python](https://img.shields.io/badge/Python-1a1a1a?style=for-the-badge&logo=python&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-1a1a1a?style=for-the-badge&logo=typescript&logoColor=white)
![Rust](https://img.shields.io/badge/Rust-1a1a1a?style=for-the-badge&logo=rust&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-1a1a1a?style=for-the-badge&logo=javascript&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-1a1a1a?style=for-the-badge&logo=postgresql&logoColor=white)
![Solana](https://img.shields.io/badge/Solana-1a1a1a?style=for-the-badge&logo=solana&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-1a1a1a?style=for-the-badge&logo=nodedotjs&logoColor=white)
![Anchor](https://img.shields.io/badge/Anchor-1a1a1a?style=for-the-badge&logoColor=white)

<p>
  <a href="https://pypi.org/project/aiqg/"><img alt="aiqg on PyPI" src="https://img.shields.io/pypi/v/aiqg?style=for-the-badge&label=aiqg&color=111111" /></a>
  <a href="https://pypi.org/project/actgate/"><img alt="actgate on PyPI" src="https://img.shields.io/pypi/v/actgate?style=for-the-badge&label=actgate&color=111111" /></a>
</p>
<p>
  <a href="https://github.com/michaelhly/solana-py/pull/701"><img alt="solana-py #701 merged" src="https://img.shields.io/badge/solana--py-%23701_merged-2ea44f?style=for-the-badge" /></a>
</p>

---

### On the shelf

- **[ai-quality-gate](https://github.com/kartsan03/ai-quality-gate)** / [`aiqg`](https://pypi.org/project/aiqg/): offline gate for model output; no model call at gate time
- **[actgate](https://github.com/kartsan03/actgate)** / [`actgate`](https://pypi.org/project/actgate/): local intent ledger for agent tool actions; human approve before side effects
- **[djinni-market-etl](https://github.com/kartsan03/djinni-market-etl)**: personal read of the UA job market from public data
- **[rook](https://github.com/kartsan03/rook)**: turn a creator's recent content into something you can decide from
- **[StableInvoice](https://github.com/kartsan03/StableInvoice)**: small Solana escrow invoice flow I built when I needed the chain in the loop

---

### Contributed to

- [michaelhly/solana-py](https://github.com/michaelhly/solana-py) — [#701](https://github.com/michaelhly/solana-py/pull/701) merged (websocket unsubscribe helpers)
- [kevinheavey/solders](https://github.com/kevinheavey/solders)
