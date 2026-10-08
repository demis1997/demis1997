# Dimitris Konstantinou
<p align="center">
<img src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExOGk3MTBkbnIwcmo2dGFtdDgzcWYwcHE2Y2Y2YnBpcm11M3Vlb25udiZlcD12MV9naWZzX3NlYXJjaCZjdD1n/11KzOet1ElBDz2/giphy.gif" alt="Spike Spiegel — Cowboy Bebop" width="450" />
</p>
**Software engineer building applied AI systems, with a background in backend systems, blockchain security and cryptographic infrastructure.**

I focus on systems whose outputs can be inspected and tested: grounded AI workflows, durable backend state, and explicit security boundaries. My current flagship project is SiteProof, where a generated redesign must pass executable checks before a reviewer can accept it.

## Selected work

- **[SiteProof](https://github.com/demis1997/siteproof)** — Evidence-backed homepage auditing and private redesign verification. Typed findings, fact provenance, hybrid-retrieval infrastructure and checkpointed workflows connect observation to bounded repair and acceptance. Real Docker/browser/DB/storage fixture checks cover regression rejection and restart recovery; live model quality, semantic retrieval and inference costs remain blocked, and human review is pending.
- **[IronLedger](https://github.com/demis1997/IronLedger)** — Rust double-entry ledger with atomic PostgreSQL writes, transactional outbox, idempotency, replay and reconciliation. Fifty-nine local workspace tests and strict Clippy checks passed during maintenance; full-stack validation is incomplete and the inspected main CI run failed. The focused maintenance fix is under review.
- **[Quorum Custody](https://github.com/demis1997/quorum-custody)** — A policy-controlled MPC custody for local Ethereum ETH transfers. Three separate signer processes create a real 2-of-3 secp256k1 wallet with Coinbase cb-mpc. Two distinct people approve the exact unsigned transaction; two available signers independently verify that evidence, produce a threshold ECDSA signature, and the custody worker verifies and broadcasts it to Anvil. A third signer can be offline during signing.
- **[cryptoanalyzer](https://github.com/demis1997/cryptoanalyzer)** — DeFi research workbench combining protocol adapters, document ingestion, graph persistence and source-aware heuristic scoring. Fixture scoring checks are reproducible; live data adapters and optional models need broader validation. Scores are not validated predictions of financial risk.
- **[Iris Sales Coach](https://github.com/demis1997/iris-sales-coach)** — Sales-coaching prototype with 13 versioned prompts, structured schemas and a typed provider interface. Ten mock-provider AI tests, the permission test and the build passed, including offline CI; existing lint issues remain. Live inference and telephony quality are not established by these checks. Built with Lovable; no customer outcomes are claimed.
- **[Canopy AI](https://github.com/demis1997/canopy-AI)** — Canopy is an AI reply and sales copilot for adult-content creators and agencies. It keeps creator personas, fan conversations, approved training, and product catalogs within organizations. Operators can review, edit, reject, or insert suggestions. Model responses are checked against deterministic safety, product, price, and conversation rules.
## Tools demonstrated in these projects

Python, TypeScript/JavaScript and Rust · FastAPI, React/Next.js and Express · PostgreSQL/pgvector, Redis and object storage · LangGraph, structured outputs and evaluation harnesses · Playwright, axe and Lighthouse · Solidity/EVM property testing · Docker and GitHub Actions.

[LinkedIn](https://www.linkedin.com/in/demisk/) 
