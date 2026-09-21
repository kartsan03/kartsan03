<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/header-dark.svg">
  <img alt="Tymur. Data pipelines and LLM tooling." src="assets/header-light.svg" width="100%">
</picture>

I build data pipelines and the tooling around LLMs. Most of what I build never shows up here; the public stuff is whatever stayed useful more than once.

Lately that means bug fixes in LLM and agent libraries. The bugs tend to be the same kind: a layer that reports something other than what the layer under it did.

### Upstream

- <a href="https://github.com/github/spec-kit/pulls?q=is%3Apr+author%3Akartsan03+is%3Amerged"><img src="https://github.com/github.png?size=40" width="20" height="20" align="top" alt=""></a> [github/spec-kit](https://github.com/github/spec-kit/pulls?q=is%3Apr+author%3Akartsan03+is%3Amerged): 5 merged PRs on agent dispatch, bundle pins, catalogs, JSON settings
- <a href="https://github.com/facebookincubator/muse-gadget-sdk/pulls?q=is%3Apr+author%3Akartsan03+is%3Amerged"><img src="https://github.com/facebookincubator.png?size=40" width="20" height="20" align="top" alt=""></a> [facebookincubator/muse-gadget-sdk](https://github.com/facebookincubator/muse-gadget-sdk/pulls?q=is%3Apr+author%3Akartsan03+is%3Amerged): 2 merged PRs on `system.run` exits and `file.write` modes

[Everything else I've had merged](https://github.com/search?q=author%3Akartsan03+is%3Apr+is%3Amerged+-user%3Akartsan03&type=pullrequests)

### Projects

- [ai-quality-gate](https://github.com/kartsan03/ai-quality-gate): offline checks for recorded LLM output (schema, grounding, snapshots) that fail CI with an exit code and never call a model. On PyPI as [`aiqg`](https://pypi.org/project/aiqg/).
- [actgate](https://github.com/kartsan03/actgate): an MCP proxy that holds an agent's tool calls until a person approves them, and records each decision in a hash-chained ledger. On PyPI as [`actgate`](https://pypi.org/project/actgate/).
- [djinni-market-etl](https://github.com/kartsan03/djinni-market-etl): Djinni jobs and candidate profiles in Postgres, with each vacancy tracked until it closes.
- [StableInvoice](https://github.com/kartsan03/StableInvoice): USDC escrow invoices on Solana. The client funds a vault up front, and payment goes out in one lump sum once every milestone is accepted.
