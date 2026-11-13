# Tymur

I fix bugs in LLM libraries, inference servers and agent frameworks. Most of them turn out to be the same bug: a layer reports something other than what the layer under it did. I also build data pipelines, mostly for job-market data.

Building: [wiretruth](https://github.com/kartsan03/wiretruth). Does your LLM SDK tell you the truth? It replays real provider responses through any-llm, LiteLLM, pydantic-ai, the Vercel AI SDK and TanStack AI, and checks what each one reports against what the provider sent. [Results matrix](https://kartsan03.github.io/wiretruth/).

## Merged upstream work

98 merged PRs in 17 projects, counted on 13 November 2026. The bigger ones:

- [Semantica](https://github.com/semantica-agi/semantica/pulls?q=is%3Apr+author%3Akartsan03+is%3Amerged) (19 merged): export, vector-store and triple-store fixes, e.g. [ranking Euclidean results by distance in Qdrant and Pinecone](https://github.com/semantica-agi/semantica/pull/2116).
- [Xinference](https://github.com/xorbitsai/inference/pulls?q=is%3Apr+author%3Akartsan03+is%3Amerged) (19 merged): chat rendering, stop strings, streaming, request aborts and replica failover, e.g. [using greedy decoding at temperature 0 for Gemma 3, Gemma 4, GLM-4V and MiniCPM-V 4.6](https://github.com/xorbitsai/inference/pull/5727).
- [Spec Kit](https://github.com/github/spec-kit/pulls?q=is%3Apr+author%3Akartsan03+is%3Amerged) (19 merged): integration manifests, extension catalogs, presets, bundle pins and workflows, e.g. [skipping the right side of `and`/`or` when the left side decides](https://github.com/github/spec-kit/pull/4923).
- [FastMCP for TypeScript](https://github.com/punkpeye/fastmcp/pulls?q=is%3Apr+author%3Akartsan03+is%3Amerged) (15 merged): MCP protocol, OAuth proxy and edge runtime fixes, e.g. [stopping tool notifications and timers after a call is aborted](https://github.com/punkpeye/fastmcp/pull/484).
- [txtai](https://github.com/neuml/txtai/pulls?q=is%3Apr+author%3Akartsan03+is%3Amerged) (5 merged): index and graph fixes, e.g. [deleting the requested rows when ANN ids are a NumPy array](https://github.com/neuml/txtai/pull/1303).
- [muse-gadget-sdk](https://github.com/facebookincubator/muse-gadget-sdk/pulls?q=is%3Apr+author%3Akartsan03+is%3Amerged) (4 merged): Linux runtime fixes, e.g. [making `system.run` return when the shell exits, not when its pipes close](https://github.com/facebookincubator/muse-gadget-sdk/pull/26).

Also embabel-agent (3), ollaya (3), any-llm (2), solana-py (2), and TanStack AI, Docling and five more projects with one each. [All of them](https://github.com/search?q=author%3Akartsan03+is%3Apr+is%3Amerged+-user%3Akartsan03&type=pullrequests).

## Projects

- [ai-quality-gate](https://github.com/kartsan03/ai-quality-gate): offline checks for recorded LLM output (schema, grounding, snapshots) that fail CI with an exit code and never call a model. On PyPI as [`aiqg`](https://pypi.org/project/aiqg/).
- [actgate](https://github.com/kartsan03/actgate): an MCP proxy that holds an agent's tool calls until a person approves them and writes each decision to a hash-chained ledger. On PyPI as [`actgate`](https://pypi.org/project/actgate/).
- [djinni-market-etl](https://github.com/kartsan03/djinni-market-etl): Djinni job postings in PostgreSQL, with one observation per posting per run, so time to close and reopens can be counted. [Analysis recipes](https://github.com/kartsan03/djinni-market-etl/blob/main/docs/analysis.md).
- [solana-sort-key-and-clock](https://github.com/kartsan03/solana-sort-key-and-clock): which rule 16 Solana mainnet validators use to order transactions in a block, measured with my own probe transactions. The raw data and a one-command reproduction are in the repo.
- [StableInvoice](https://github.com/kartsan03/StableInvoice): USDC escrow invoices on Solana. The client funds a vault up front, and the payment goes out in one sum once every milestone is accepted.

## What I'm working out

How do you test code that sits between your program and a model provider, when the provider's answer changes from run to run? My current answer is to record real responses once and check everything against the recording. wiretruth does that for SDKs, ai-quality-gate for an app's own LLM output.
