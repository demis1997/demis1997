# Hey, I'm Dimitris 

<p align="center">
  <img src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExOGk3MTBkbnIwcmo2dGFtdDgzcWYwcHE2Y2Y2YnBpcm11M3Vlb25udiZlcD12MV9naWZzX3NlYXJjaCZjdD1n/11KzOet1ElBDz2/giphy.gif" alt="Spike Spiegel — Cowboy Bebop" width="450" />
</p>

I build things that are supposed to be difficult to break. And occasionally things that break in very interesting ways.

My focus is **blockchain security architecture and institutional digital asset custody**: MPC and threshold cryptography, Solidity and smart contract security, post quantum cryptography, and secure infrastructure and cloud architecture. I study how key protection, transaction authority, and recovery hold up under compromise.

I build with **Rust, Python, TypeScript, and Solidity**, use **static analysis, fuzzing, and security testing** to challenge the happy path, and work across distributed systems and AI infrastructure.

When I'm not staring at a terminal, you'll probably find me boxing, riding, or doing random sidequests.

**[Security Research Index](https://github.com/demis1997/institutional-custody-security-research/blob/main/RESEARCH_INDEX.md)**

[Security research](#featured-security-research) · [Current work](#currently-working-on) · [Open source](#open-source-security-contributions) · [Projects](#other-engineering-projects)

## Featured Security Research

### [Securing Institutional Digital Asset Custody](https://github.com/demis1997/institutional-custody-security-research)

*Private Keys, Distributed Trust, and the Uncomfortable Arrival of Quantum Computing*

Research examining how MPC signing, authorization policies, distributed state, and recovery mechanisms interact under adversarial conditions. Includes reproducible application experiments, Ethereum transaction authorization analysis, verification microbenchmarks, and a proposed post quantum migration architecture.

The evidence distinguishes executed tests and a synthetic local-chain transfer from declared models and unexecuted native MPC scenarios. This is independent research, not a production custody certification.

**[Read Paper](https://github.com/demis1997/institutional-custody-security-research/blob/main/paper/custody-security-research.pdf)** · [Research Repository](https://github.com/demis1997/institutional-custody-security-research) · [Quorum Custody Implementation](https://github.com/demis1997/quorum-custody)

## Currently Working On

### [Securing Institutional Digital Asset Custody on AWS](https://github.com/demis1997/aws-custody-security-lab)

Building a custody security lab around independently administered AWS trust domains. Implemented so far: modular Terraform, IAM/KMS/S3 policy definitions, private network infrastructure, a fourteen-scenario threat model, and reproducible compromise and recovery tests.

The tests distinguish one compromised signer from a signing quorum, shared deployment authority from independent accounts, and encrypted backups from trustworthy recovery history. Terraform is validated with mocked AWS providers; no cloud infrastructure or native MPC integration has been deployed.

[Explore the lab](https://github.com/demis1997/aws-custody-security-lab) · [Validation evidence](https://github.com/demis1997/aws-custody-security-lab/blob/main/VALIDATION_REPORT.md) · [Quorum Custody](https://github.com/demis1997/quorum-custody)

Ongoing post quantum custody research examines hybrid authorization and migration paths that preserve spending and recovery boundaries.

##  Custody Engineering

###  [Quorum Custody](https://github.com/demis1997/quorum-custody)

A local Ethereum custody demo built around **2-of-3 threshold ECDSA** and Coinbase's cb-mpc, with separate signer processes.

Independent transaction approvals, signer-side policy checks, mutual TLS, and durable recovery paths make the trust boundaries concrete. Even with one signer offline, the remaining two can still get the job done.

Turns out keeping private keys out of the wrong hands is a pretty interesting engineering problem.

##  Open Source Security Contributions

### [Semgrep](https://github.com/semgrep/semgrep)

- **Open · [#11999](https://github.com/semgrep/semgrep/pull/11999)** — fix Go static-analysis false negatives involving calls in conditional initializers; improve statement-sequence matching, preserve scope and shadowing, and add regression coverage.

### [Slither](https://github.com/crytic/slither)

Solidity static-analysis contributions focused on gas efficiency, conservative detection, and regression tests:

- **Open · [#3119](https://github.com/crytic/slither/pull/3119)** — detect literal revert strings eligible for custom errors, with error-ABI caveats.
- **Open · [#3120](https://github.com/crytic/slither/pull/3120)** — identify fixed-size storage layouts that can use fewer slots; restrict suggestions to fresh layouts.
- **Open · [#3121](https://github.com/crytic/slither/pull/3121)** — detect read-only external memory parameters that could use calldata, accounting for writes and aliases.
- **Open · [#3122](https://github.com/crytic/slither/pull/3122)** — detect invariant scalar storage reads in isolated loops using control-flow and read/write analysis.
- **Open · [#3123](https://github.com/crytic/slither/pull/3123)** — add conservative cacheable-accumulator metadata to existing `costly-loop` findings.
- **Closed, unmerged · [#1707](https://github.com/crytic/slither/pull/1707)** — earlier gas-optimization detector proposal.

*PR statuses checked 21 October 2026; open proposals are not merged features.*

##  Other Engineering Projects

###  [IronLedger](https://github.com/demis1997/IronLedger)

A Rust double-entry ledger with per-asset balancing, atomic PostgreSQL writes, idempotency, replay and reconciliation, backed by unit and property tests. Making sure money doesn't magically appear or disappear because two requests arrived at the same time.

###  [SiteProof](https://github.com/demis1997/siteproof)

An AI website auditor with tenant boundaries, SSRF protection, isolated browser capture and checked redesigns. Because "the AI said it looks better" is not a testing strategy.

###  [cryptoanalyzer](https://github.com/demis1997/cryptoanalyzer)

A DeFi research workbench combining protocol adapters, document ingestion, graph data and source-aware scoring. Research with inspectable sources and explicit gaps, not a crystal ball for predicting financial risk.

###  [Iris Sales Coach](https://github.com/demis1997/iris-sales-coach)

An AI sales-coaching prototype with versioned prompts, typed interfaces, permission checks and repeatable mock-provider tests. Helping salespeople improve without another three-hour training presentation.

###  [Canopy AI](https://github.com/demis1997/canopy-AI)

An AI reply and sales copilot with organization-scoped data, encrypted provider credentials, deterministic checks and human review. A mix of AI orchestration, business logic and trying to make software sound less like software.

##  Security Research & Engineering Interests

Current questions I'm exploring, usually with a threat model or a test harness nearby:

- **Digital asset custody threat modeling:** signer trust boundaries, recovery, and MPC/HSM security.
- **Application security:** static analysis, vulnerability detection, fuzzing, and useful regression tests.
- **Cryptographic protocol security:** hybrid authorization, post quantum custody migration, and the limits of current EVM account models.
- **Secure infrastructure:** independent signer administration, cloud identity, protected recovery, and observable failure handling.

##  Things I work with

### Languages

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Rust](https://img.shields.io/badge/Rust-000000?style=for-the-badge&logo=rust&logoColor=white)
![Solidity](https://img.shields.io/badge/Solidity-363636?style=for-the-badge&logo=solidity&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![C++](https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=cplusplus&logoColor=white)

### Security & Blockchain

![Ethereum](https://img.shields.io/badge/Ethereum-3C3C3D?style=for-the-badge&logo=ethereum&logoColor=white)
![Foundry](https://img.shields.io/badge/Foundry-222222?style=for-the-badge)
![Hardhat](https://img.shields.io/badge/Hardhat-FFF100?style=for-the-badge&logoColor=black)
![MPC](https://img.shields.io/badge/Threshold_Cryptography-593D88?style=for-the-badge)
![Slither](https://img.shields.io/badge/Slither-8B0000?style=for-the-badge)
![Hyperledger](https://img.shields.io/badge/Hyperledger-2F3134?style=for-the-badge&logo=hyperledger&logoColor=white)
![OpenZeppelin](https://img.shields.io/badge/OpenZeppelin-4E5EE4?style=for-the-badge&logo=openzeppelin&logoColor=white)

### Backend & Infrastructure

![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=for-the-badge)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white)

### AI & Frontend

![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=for-the-badge&logo=openai&logoColor=white)
![Anthropic](https://img.shields.io/badge/Anthropic-191919?style=for-the-badge&logo=anthropic&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white)
![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?style=for-the-badge)
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white)
![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=for-the-badge&logo=playwright&logoColor=white)

## ☕ Say hello

Always happy to talk about cryptography, security, distributed systems, AI, or an interesting problem worth solving.

[LinkedIn](https://www.linkedin.com/in/demisk/)

---

*Whatever happens, happens.*

**See you, space cowboy…** 🚀
