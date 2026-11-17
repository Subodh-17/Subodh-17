# Subodh

[![GitHub](https://img.shields.io/badge/GitHub-Subodh--17-0f172a?style=flat-square&logo=github&logoColor=white)](https://github.com/Subodh-17)
[![Verified PR Census](https://img.shields.io/badge/Authored_PRs-94_Lifetime_(50_Merged)-10b981?style=flat-square&logo=git&logoColor=white)](https://github.com/Subodh-17)
[![Open Contributions](https://img.shields.io/badge/Open_PRs-16_Open-2563eb?style=flat-square&logo=github&logoColor=white)](https://github.com/Subodh-17)
[![Formal Peer Reviews](https://img.shields.io/badge/Peer_Reviews-6_Submitted_(3_Approved)-8b5cf6?style=flat-square&logo=github&logoColor=white)](https://github.com/Subodh-17)
[![Rust Systems](https://img.shields.io/badge/Rust-Arrow_|_DataFusion-dea584?style=flat-square&logo=rust&logoColor=black)](https://www.rust-lang.org)
[![Python ML](https://img.shields.io/badge/Python-PyTorch_|_Diffusers-3776ab?style=flat-square&logo=python&logoColor=white)](https://python.org)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Subodh-0a66c2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/subodh-b-b705b5403)
[![Email](https://img.shields.io/badge/Email-subodh171011%40gmail.com-ea4335?style=flat-square&logo=gmail&logoColor=white)](mailto:subodh171011@gmail.com)

---

### Systems & AI Infrastructure Engineer | Rust, Distributed Systems, ML Infrastructure

I am an engineer focused on **high-performance columnar query systems (Rust / Apache Arrow), causal contract verification in AI agent runtimes, deterministic ML training execution, and resilient backend architectures**. My work emphasizes systems correctness, edge-case reproduction, zero-copy data paths, and defensive state management.

I actively contribute to open-source ecosystems including **Apache Arrow-rs, Apache DataFusion & DataFusion-Spark, Hugging Face Diffusers, PyTorch Lightning, SafeTensors, and ThreeMoonsLab Shipgate**. Across the **National Summer of Code (NSoC 2026)** program, contributions were merged across all eight targeted repositories (17 merged pull requests in total). I also submit thorough formal code reviews to Tier-1 repositories, with multiple review findings adopted by authors into subsequent patch revisions.

---

## 1. Selected Engineering Strengths

- **High-Performance Columnar Systems (Rust):** Implementing vectorized execution kernels, canonical error formatting, and zero-copy deserialization in Apache Arrow-rs and DataFusion; Parquet Variant type handling and error diagnostics.
- **Runtime Verification & Agent Telemetry:** Developing mathematical runtime monitors for multi-agent systems, including causal DAG happens-before relation checking, Allen's 13 interval temporal algebra relations, sequence-gap network drop analyzers, and zero-dependency normalizers for OpenTelemetry GenAI v2 and MCP (JSON-RPC 2.0).
- **ML Infrastructure & Training Determinism:** Debugging and resolving distributed training race conditions in PyTorch Lightning's `FitLoop`, implementing multi-text-encoder PEFT LoRA adapter routing in Hugging Face Diffusers, and evaluating strided tensor memory deduplication in SafeTensors.
- **Resilient Distributed Backends & GIS:** Engineering terrain/weather-constrained A* multi-modal routing algorithms with physical speed floors in PostGIS, and satellite radar (Sentinel-1 SAR) oil slick segmentation and hydrodynamic drift hindcasting pipelines.

---

## 2. Contribution Scorecard

*Census independently verified against live GitHub API state as of November 16, 2026.*

| Metric Category | Verified Count | Verification Scope & Authority |
|---|:---:|---|
| **Total Lifetime Authored Pull Requests** | **94** | GitHub Search API (`gh search prs --author=Subodh-17`) |
| **Merged Pull Requests (Total)** | **50** | Formally merged into primary or target branches |
| ↳ *External Upstream Open Source* | *32* | Merged into DataFusion, DataFusion-Spark, Diffusers, DevTrack, Shipgate, AgentWatch, etc. |
| ↳ *Personal Production & Research Codebases* | *18* | Merged feature branches in Marine Pollution (8), Subodh-17 (9), Logistics (1) |
| **Currently Open Contributions** | **16** | Open PRs across upstream, mentored, and personal repositories, regardless of current review activity. |
| ↳ *Tier-1 Broader Open Source* | *12* | Arrow-rs, Lightning (2), Diffusers (6), SafeTensors, MS-Swift, TENET-AI |
| ↳ *Mentored / Personal Codebases* | *4* | Shipgate (`#1141`), Observability Platform (`#37`), PatchPilot (`#354`), Marine Pollution (`#9`) |
| **Closed / Unmerged Pull Requests** | **28** | Documented exploratory investigations, superseded revisions, and policy closures |
| ↳ *Mentored Superseded Pull Requests* | *2* | `CodePrism#66` (superseded by merged `#70`), `Sentient#274` |
| ↳ *Broader Open Source Closed PRs* | *26* | Documented investigations across Arrow-rs, DataFusion, Transformers, MLflow, mloda, SafeTensors, Airbyte |
| **Formal Peer Code Reviews** | **6** | Submitted across PyTorch Lightning (2), SafeTensors (3), and MLflow (1) |
| ↳ *Approved Reviews* | *3* | `safetensors#900`, `safetensors#898`, `pytorch-lightning#22182` |
| ↳ *Changes Requested Reviews* | *2* | `safetensors#913`, `pytorch-lightning#22142` |
| ↳ *Commented Reviews* | *1* | `mlflow#27631` |
| **Mathematical Identity** | **94 = 50 + 16 + 28** | **Strict mathematical reconciliation: zero uncataloged entries** |
| **NSoC 2026 Repository Coverage** | **8 / 8** | **17 merged pull requests across all 8 targeted NSoC repositories (>=1 merged PR in each)** |
| **ECSoC 2026 Mentored Contributions** | **2** | 2 merged pull requests in `Karan-Raj-KR/crewai-recipes` (#229, #242) |

---

## 3. Selected Upstream Contributions

### High-Performance Query Systems (Rust)

* **[apache/datafusion#26465](https://github.com/apache/datafusion/pull/26465)** — `fix(functions): pass correct number_rows in gcd benchmarks` (**MERGED**)
  [![Rust](https://img.shields.io/badge/Rust-DEA584?style=flat-square&logo=rust&logoColor=black)](https://www.rust-lang.org) [![Apache Arrow](https://img.shields.io/badge/Apache_Arrow-E10079?style=flat-square&logo=apachearrow&logoColor=white)](https://arrow.apache.org)
  * *Problem:* In Apache DataFusion's scalar mathematical benchmark suite (`datafusion/functions/benches/gcd.rs`), array fixture generators passed mismatched row parameters across Criterion execution matrices, corrupting throughput measurements for SIMD greatest-common-divisor routines.
  * *Change:* Corrected configuration plumbing to propagate user-configured row counts systematically across all benchmark iteration loops.
  * *Evidence:* Merged upstream by DataFusion PMC Chair Andrew Lamb on 2026-10-19 (Merge SHA: `384d6464`).
* **[apache/datafusion-spark#116](https://github.com/apache/datafusion-spark/pull/116)** — `fix(string): match Spark 4 encode charset and error behavior (#46)` (**MERGED**)
  [![Rust](https://img.shields.io/badge/Rust-DEA584?style=flat-square&logo=rust&logoColor=black)](https://www.rust-lang.org) [![Apache Arrow](https://img.shields.io/badge/Apache_Arrow-E10079?style=flat-square&logo=apachearrow&logoColor=white)](https://arrow.apache.org)
  * *Problem:* In Apache DataFusion-Spark's string expression kernel, string encoding routines failed to adhere to Spark 4 charset mapping and error behavior on invalid input byte sequences (`#46`).
  * *Change:* Implemented compliant charset encoding logic, handling replacement characters and error modes matching Spark 4 specifications.
  * *Evidence:* Merged upstream into `apache/datafusion-spark:main` on 2026-11-16 (Merge SHA: `359ca1c2`).

### Machine Learning Infrastructure & Training Determinism

* **[huggingface/diffusers#14961](https://github.com/huggingface/diffusers/pull/14961)** — `Fix active adapter detection for text encoders` (**MERGED**)
  [![Hugging Face](https://img.shields.io/badge/Hugging_Face-Diffusers-FFD21E?style=flat-square&logo=huggingface&logoColor=black)](https://huggingface.co/docs/diffusers) [![PyTorch](https://img.shields.io/badge/PyTorch-PEFT_LoRA-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)](https://pytorch.org)
  * *Problem:* `pipeline.get_active_adapters()` failed to detect active PEFT LoRA adapters attached to secondary text encoders (`text_encoder_2`) in dual-encoder diffusion architectures such as SDXL and Flux.
  * *Change:* Extended adapter introspection across all registered encoder submodules, aggregating active adapter names while gracefully bypassing non-PEFT modules.
  * *Evidence:* Merged upstream on 2026-10-08 (Merge SHA: `e0415c41`).
* **[Lightning-AI/pytorch-lightning#22006](https://github.com/Lightning-AI/pytorch-lightning/pull/22006)** — `fix: set sampler epoch before creating resumed iterator` (**OPEN — COMMUNITY REVIEWED**)
  [![PyTorch Lightning](https://img.shields.io/badge/PyTorch_Lightning-792EE5?style=flat-square&logo=lightning&logoColor=white)](https://lightning.ai) [![PyTorch](https://img.shields.io/badge/PyTorch-Distributed_ML-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)](https://pytorch.org)
  * *Problem:* In PyTorch Lightning's distributed `FitLoop`, resumed data iterators were instantiated before updating the sampler epoch, causing distributed workers to resume training with an incorrect epoch seed and corrupting data shuffling determinism.
  * *Change:* Reordered loop initialization to set the sampler epoch prior to iterator creation.
  * *Evidence:* Validated across 12 distributed worker prefetch traces; positive community review by `@anishpentyala`.

### Security, Policy Gates & Verification

* **[VarshithReddy2006/DevTrack#171](https://github.com/VarshithReddy2006/DevTrack/pull/171)** — `fix(auth): harden ClerkUserSyncService against account takeover, username collisions, and invalid inputs (#115)` (**MERGED**)
  [![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)](https://www.typescriptlang.org) [![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)](https://mongodb.com)
  * *Problem:* In Clerk OAuth authentication sync, unverified email linking permitted cross-identity account hijacking. Furthermore, username derivation lacked schema constraint bounds, and concurrent webhook invocations triggered unhandled MongoDB `E11000` duplicate key crashes.
  * *Change:* Enforced strict verification checks (`verification.status === 'verified'`), safe base username derivation bounded to [3, 30] characters, bounded random/numeric collision retries (max 12), and self-healing for supporting profiles (`UserProfile`, `UserSettings`).
  * *Evidence:* Resolves Issue #115. Verified across 22 new unit and integration tests; merged upstream on 2026-11-11 (Merge SHA: `438c472`).
* **[Shinraya-Tech-Labs/AgentWatch#754](https://github.com/Shinraya-Tech-Labs/AgentWatch/pull/754)** — `feat(contracts): implement interval temporal logic and happens-before ordering` (**MERGED**)
  [![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)](https://python.org) [![OpenTelemetry](https://img.shields.io/badge/OpenTelemetry-GenAI_v2-000000?style=flat-square&logo=opentelemetry&logoColor=white)](https://opentelemetry.io)
  * *Problem:* Agent runtime verification lacked formal operators to reason about concurrency, race conditions, and temporal relationships across asynchronous multi-agent tool invocations.
  * *Change:* Built a directed acyclic graph (DAG) causal happens-before relation evaluator and implemented Allen's 13 interval temporal algebra relations (`meets`, `overlaps`, `during`, `starts`, `finishes`, and inverses) in `agentwatch/contracts/temporal.py`.
  * *Evidence:* Verified multi-agent concurrency determinism; merged upstream on 2026-10-20 (Merge SHA: `2cf6ed3b`).
* **[ThreeMoonsLab/agents-shipgate#1106](https://github.com/ThreeMoonsLab/agents-shipgate/pull/1106)** — `fix(privacy): redact AWS path keys and URL-safe Basic credentials` (**MERGED**)
  [![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)](https://python.org) [![Security](https://img.shields.io/badge/Security-Lookaround_Redaction-critical?style=flat-square)](https://github.com/ThreeMoonsLab/agents-shipgate)
  * *Problem:* AWS secret access keys embedded inside file paths (`path/<key>`, `s3://.../<key>`) escaped redaction regexes due to forward-slash delimiter handling, and URL-safe Base64 strings (RFC 4648) triggered false negatives in privacy audit logs.
  * *Change:* Hardened lookaround assertion boundaries to handle directory separators without compromising entropy heuristics, and implemented RFC 4648 character normalization and padding validation.
  * *Evidence:* Verified across 32 regression tests; merged upstream on 2026-11-06 (Merge SHA: `1e3e372`).

---

## 4. Formal Code Review Work

*Subodh conducts independent technical peer reviews on upstream repositories, combining formal defect reproduction, test coverage analysis, and cross-platform compilation:*

| Target Pull Request | Decision | Submission Date | Technical Finding & Author Interaction |
|---|:---:|:---:|---|
| [`safetensors/safetensors#900`](https://github.com/safetensors/safetensors/pull/900) | **`APPROVED`** | 2026-11-06 | Empirically verified CPU allocation of empty PyTorch tensors across 96 parameter combinations under Meta and CUDA ambient contexts on an RTX 5070 GPU. PR author `@DiadkoShmek` thanked Subodh for the WSL2/CUDA validation. |
| [`safetensors/safetensors#898`](https://github.com/safetensors/safetensors/pull/898) | **`APPROVED`** | 2026-11-15 | Validated rejection of tensors named `__metadata__` to prevent silent custom header erasure during serialization. Proved zero runtime performance overhead and confirmed SemVer compatibility. |
| [`Lightning-AI/pytorch-lightning#22182`](https://github.com/Lightning-AI/pytorch-lightning/pull/22182) | **`APPROVED`** | 2026-11-15 | Validated `WeightAveraging` checkpoint resume double-updating fix and bit-for-bit parity (`torch.allclose`). PR author `@deep1blue` publicly commented: *"Thank you @Subodh-17 for reviewing and approving this PR!"* |
| [`safetensors/safetensors#913`](https://github.com/safetensors/safetensors/pull/913) | **`CHANGES_REQUESTED`** | 2026-11-12 | Identified interval shrinking bug, test artifact leakage, and zero-stride view gaps. **PR author Davis Rens adopted Finding 1 (`last_stop = max(...)`) and Finding 3 (test cleanup) in commit `859baa3cde`, and resolved zero-stride view checks in commit `5c284e3918`.** Remaining interleaved view cases were separated into Issue #926, which Subodh implemented in PR #927. |
| [`Lightning-AI/pytorch-lightning#22142`](https://github.com/Lightning-AI/pytorch-lightning/pull/22142) | **`CHANGES_REQUESTED`** | 2026-11-12 | Evaluated lazy-loading shared tensor and untyped storage preservation to prevent memory duplication during model materialization. PR author `@deep1blue` addressed both points in commit `b01e67335`. |
| [`mlflow/mlflow#27631`](https://github.com/mlflow/mlflow/pull/27631) | **`COMMENTED`** | 2026-11-12 | Identified edge cases in empty DataFrame evaluation and per-scorer evidence tracking. PR author `@harshal-paltse` adopted all three review findings in commit `6791bb59a`. |

*Note: Author branch adoption or acknowledgment is an indicator of technical quality in peer review; it is distinct from repository maintainer endorsement or merge.*

---

## 5. Original Engineering Projects

### Marine Pollution Intelligence
**Repository:** [`Subodh-17/marine-pollution-intelligence`](https://github.com/Subodh-17/marine-pollution-intelligence) *(Public)*
*Autonomous satellite radar (SAR) oil spill segmentation, hydrodynamic drift hindcasting, and vessel attribution platform.*

[![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=flat-square&logo=python&logoColor=white)](https://python.org)
[![FastAPI](https://img.shields.io/badge/FastAPI-0.110+-009688?style=flat-square&logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com)
[![React](https://img.shields.io/badge/React_19-20232A?style=flat-square&logo=react&logoColor=61DAFB)](https://react.dev)
[![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white)](https://vitejs.dev)
[![ONNX Runtime](https://img.shields.io/badge/ONNX_Runtime-005CED?style=flat-square&logo=onnx&logoColor=white)](https://onnxruntime.ai)
[![Leaflet](https://img.shields.io/badge/Leaflet-199900?style=flat-square&logo=leaflet&logoColor=white)](https://leafletjs.com)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=flat-square&logo=postgresql&logoColor=white)](https://postgresql.org)
[![SQLite](https://img.shields.io/badge/SQLite-07405E?style=flat-square&logo=sqlite&logoColor=white)](https://sqlite.org)

- **Copernicus Sentinel-1 SAR Processing:** Implemented adaptive local Gaussian thresholding preceded by a 7x7 Lee speckle filter window convolution to suppress radar sea clutter while preserving dark slick contours.
- **Embedded Edge Inference:** Deployed dual ONNX Runtime CPU models (`SpillUNet` [54 KB] + `SceneClassifier` [50 KB]) with a lightweight ~105 KB total model payload requiring zero GPU runtime dependencies.
- **2D Euler Hydrodynamic Drift Hindcasting:** Numerical trajectory model combining surface wind shear (empirical 3% rule) and Open-Meteo CMEMS/MET Norway ocean current vectors with circuit-breaker backoffs.
- **Spatio-Temporal AIS Attribution:** Multi-factor vessel scoring algorithm combining positional proximity, speed anomalies, and draft metrics to assign probabilistic culpability.
- **Status:** Full-stack architecture (FastAPI, React 19, Leaflet GIS, SQLite); 8 merged PRs, 1 open PR (#9).

### Predictive Logistics & Forward Supply Chain — SIH PS 26251
**Repository:** [`Subodh-17/Predictive_Logistics_SIH_26251`](https://github.com/Subodh-17/Predictive_Logistics_SIH_26251) *(Public)*
*Terrain- and weather-aware dynamic multi-modal freight routing and forward supply chain decision support.*

[![Python](https://img.shields.io/badge/Python-3.12-3776AB?style=flat-square&logo=python&logoColor=white)](https://python.org)
[![FastAPI](https://img.shields.io/badge/FastAPI-0.143-009688?style=flat-square&logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com)
[![React](https://img.shields.io/badge/React_18-20232A?style=flat-square&logo=react&logoColor=61DAFB)](https://react.dev)
[![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)](https://www.typescriptlang.org)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=flat-square&logo=postgresql&logoColor=white)](https://postgresql.org)
[![PostGIS](https://img.shields.io/badge/PostGIS-336791?style=flat-square&logo=postgresql&logoColor=white)](https://postgis.net)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=flat-square&logo=tailwind-css&logoColor=white)](https://tailwindcss.com)
[![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)](https://docker.com)

- **Dynamic Multi-Modal Routing:** Terrain- and weather-aware graph traversal engine (A* search) incorporating Digital Elevation Model (DEM) slope penalties and an enforced 8 km/h physical speed floor (`terrain.py`).
- **7-Factor Priority Dispatching:** Algorithmic queue weighting perishability, medical criticality, contract SLAs, transport costs, and route reliability (`priority.py`).
- **PostGIS Spatial Persistence:** PostgreSQL 16 + PostGIS backend executing spatial geography queries (`ST_DWithin`, `ST_LineInterpolatePoint`) for waypoint tracking.
- **Test Suite:** 280 automated unit, integration, and geospatial routing tests across 21 test files passing in CI.

### StockVision V3 — Quantitative Research Terminal
**Repository:** [`Subodh-17/stockvision-scilab-gui`](https://github.com/Subodh-17/stockvision-scilab-gui) *(Public)*
*Quantitative time-series forecasting terminal and backtester built in pure Scilab for the Scilab GUIVerse Hackathon.*

[![Scilab](https://img.shields.io/badge/Scilab-Native_Engine-002B49?style=flat-square&logo=scilab&logoColor=white)](https://www.scilab.org)
[![Time Series](https://img.shields.io/badge/Time_Series-OLS_|_AR(p)_|_Holt-0f172a?style=flat-square)](https://www.scilab.org)
[![Backtesting](https://img.shields.io/badge/Simulation-Walk--Forward-10b981?style=flat-square)](https://www.scilab.org)

- **Pure Scilab Numerical Engine:** Implemented entirely in native Scilab script (`model_engine.sce` / `gui_layout.sci`) without external binary dependencies.
- **Statistical Forecasting Models:** Ordinary Least Squares (OLS) polynomial trend fitting with exact 95% prediction intervals, Autoregressive AR(p) modeling, and Holt double exponential smoothing.
- **Multi-Fold Walk-Forward Validation:** Validates forecasting accuracy chronologically across market regimes against a naive persistence baseline.

### Blueledger — Blockchain Blue Carbon MRV Registry
**Repository:** [`Subodh-17/Blueledger`](https://github.com/Subodh-17/Blueledger) *(Public)*
*Decentralized Measurement, Reporting, and Verification (MRV) registry for blue carbon restoration credits (SIH PS 25038).*

[![Solidity](https://img.shields.io/badge/Solidity-0.8.20-363636?style=flat-square&logo=solidity&logoColor=white)](https://soliditylang.org)
[![Hardhat](https://img.shields.io/badge/Hardhat-Ethereum-FFF100?style=flat-square&logo=hardhat&logoColor=black)](https://hardhat.org)
[![Ethers.js](https://img.shields.io/badge/Ethers.js-v6-2535a0?style=flat-square&logo=ethereum&logoColor=white)](https://docs.ethers.org)
[![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=node.js&logoColor=white)](https://nodejs.org)
[![Express](https://img.shields.io/badge/Express-000000?style=flat-square&logo=express&logoColor=white)](https://expressjs.com)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=flat-square&logo=postgresql&logoColor=white)](https://postgresql.org)
[![IPFS](https://img.shields.io/badge/IPFS-Kubo_&_Pinata-65C2CB?style=flat-square&logo=ipfs&logoColor=white)](https://ipfs.tech)

- **Smart Contract Layer:** Solidity 0.8.20 batch-tracked ecological credit registry contract (`BlueCarbonRegistry.sol`) with role-based access control.
- **Separation of Duties:** Enforces programmatic constraints ensuring independent field verifiers cannot issue credits for their own verifications.
- **Decentralized Storage:** IPFS integration (Kubo RPC & Pinata) for immutable content-addressed pinning of remote-sensing evidence and field survey proofs (`storage.js`).

### Multi-AI Stock Prediction & Trading Ensemble
**Repository:** [`Subodh-17/stock_prediction_python`](https://github.com/Subodh-17/stock_prediction_python) *(Public)*
*Quantitative next-day price forecasting ensemble blending deep learning and statistical regression.*

[![Python](https://img.shields.io/badge/Python-3.11-3776AB?style=flat-square&logo=python&logoColor=white)](https://python.org)
[![PyTorch](https://img.shields.io/badge/PyTorch-LSTM-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)](https://pytorch.org)
[![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-F7931E?style=flat-square&logo=scikit-learn&logoColor=white)](https://scikit-learn.org)

- **Model Pipeline:** Implemented stacked PyTorch LSTM (30-day sliding history windows) alongside an interpretable Linear Regression baseline with technical lag indicators (`ensemble.py`).
- **Execution Guardrails:** Simulated paper-trading broker execution hooks with portfolio risk thresholds and volatility stop-losses. *(Note: Multi-LLM consensus features are simulated and dependent on external API credentials).*

### PROTEA-X-AI *(Private Hackathon Repository)*
- Fine-tuned PyTorch ResNet-18 computer vision system built for the HACKBLOX AI Hackathon 2026, featuring custom data transforms and edge evaluation harnesses. Maintained as a private repository.

---

## 6. Pull Request Contributions & Engineering Investigations

### A. Merged Upstream Pull Requests (32 PRs)

<details open>
<summary><b>View All 32 Formally Merged Upstream Pull Requests</b></summary>

| # | Repository | PR | Functional Scope | Merge Date | Merge Commit |
|:---:|---|:---:|---|:---:|:---:|
| 1 | `apache/datafusion-spark` | [#116](https://github.com/apache/datafusion-spark/pull/116) | `fix(string): match Spark 4 encode charset and error behavior (#46)` | 2026-11-16 | `359ca1c` |
| 2 | `apache/datafusion-spark` | [#118](https://github.com/apache/datafusion-spark/pull/118) | `fix(datetime): respect ANSI mode in next_day (#113)` | 2026-11-16 | `5d56182` |
| 3 | `apache/datafusion-spark` | [#119](https://github.com/apache/datafusion-spark/pull/119) | `fix(datetime): avoid premature overflow in make_dt_interval (#109)` | 2026-11-16 | `7a17ed5` |
| 4 | `deepikagandla74/ai-campus-placement-agent` | [#423](https://github.com/deepikagandla74/ai-campus-placement-agent/pull/423) | `feat: add user-controlled leaderboard opt-out` | 2026-11-15 | `4631fbe` |
| 5 | `adityalenova/cyrus` | [#151](https://github.com/adityalenova/cyrus/pull/151) | `test(api): add saved tracking authorization integration coverage` | 2026-11-14 | `7ed16f0` |
| 6 | `VarshithReddy2006/DevTrack` | [#171](https://github.com/VarshithReddy2006/DevTrack/pull/171) | `fix(auth): harden ClerkUserSyncService against account takeover (#115)` | 2026-11-11 | `438c472` |
| 7 | `Muskankr/OpenSourceMate` | [#245](https://github.com/Muskankr/OpenSourceMate/pull/245) | `test: add shared sanitized GitHub API fixtures` | 2026-11-10 | `84f9b01` |
| 8 | `WhatBreaks/WhatBreaks` | [#27](https://github.com/WhatBreaks/WhatBreaks/pull/27) | `feat(core-engine): add version transition modeling (#18)` | 2026-11-10 | `7f66ed6` |
| 9 | `adityalenova/cyrus` | [#119](https://github.com/adityalenova/cyrus/pull/119) | `fix(sitemap): correct hub frequencies and derived lastmod` | 2026-11-08 | `aa99bfd` |
| 10 | `ThreeMoonsLab/agents-shipgate` | [#1106](https://github.com/ThreeMoonsLab/agents-shipgate/pull/1106) | `fix(privacy): redact AWS path keys and URL-safe Basic credentials` | 2026-11-06 | `1e3e372` |
| 11 | `ThreeMoonsLab/agents-shipgate` | [#1105](https://github.com/ThreeMoonsLab/agents-shipgate/pull/1105) | `fix(host-grants): handle YAML timestamps in config hashing` | 2026-11-06 | `eebcb51` |
| 12 | `adityalenova/cyrus` | [#113](https://github.com/adityalenova/cyrus/pull/113) | `fix(catalog): return total and pages pagination metadata for /api/catalog/repos` | 2026-11-05 | `86d72f4` |
| 13 | `knight22-21/CodePrism` | [#79](https://github.com/knight22-21/CodePrism/pull/79) | `fix(security): include pinned versions in OSV vulnerability queries` | 2026-11-05 | `27f9f4a` |
| 14 | `sanjaysaini383/observability-platform` | [#35](https://github.com/sanjaysaini383/observability-platform/pull/35) | `feat(ci): add automated checks for project services` | 2026-11-03 | `036e6b97` |
| 15 | `aeshef/obsidian-agent` | [#68](https://github.com/aeshef/obsidian-agent/pull/68) | `feat: add per-chart reset control` | 2026-10-30 | `d84b7db5` |
| 16 | `Karan-Raj-KR/crewai-recipes` | [#242](https://github.com/Karan-Raj-KR/crewai-recipes/pull/242) | `feat(customer-onboarding): add --json output flag (#169)` | 2026-10-28 | `c279a9d7` |
| 17 | `Shinraya-Tech-Labs/AgentWatch` | [#784](https://github.com/Shinraya-Tech-Labs/AgentWatch/pull/784) | `feat(mcp): add MCP error normalizer and code classifier (fixes #745)` | 2026-10-26 | `416444a7` |
| 18 | `Karan-Raj-KR/crewai-recipes` | [#229](https://github.com/Karan-Raj-KR/crewai-recipes/pull/229) | `feat(playground): basic in-memory rate limiting to prevent runaway loops (#181)` | 2026-10-24 | `fece08a3` |
| 19 | `ionfwsrijan/PatchPilot` | [#350](https://github.com/ionfwsrijan/PatchPilot/pull/350) | `feat(security): prioritize findings by normalized severity` | 2026-10-23 | `94950e40` |
| 20 | `DivyashreeR008/Open-Agents` | [#406](https://github.com/DivyashreeR008/Open-Agents/pull/406) | `test(recommendation): add automated scoring tests` | 2026-10-20 | `a0d1ff84` |
| 21 | `Shinraya-Tech-Labs/AgentWatch` | [#757](https://github.com/Shinraya-Tech-Labs/AgentWatch/pull/757) | `feat(normalizers): implement OTel GenAI v2 and MCP protocol normalizers (#732)` | 2026-10-20 | `d6cda134` |
| 22 | `Shinraya-Tech-Labs/AgentWatch` | [#754](https://github.com/Shinraya-Tech-Labs/AgentWatch/pull/754) | `feat(contracts): implement interval temporal logic and happens-before ordering (#729)` | 2026-10-20 | `2cf6ed3b` |
| 23 | `Shinraya-Tech-Labs/AgentWatch` | [#753](https://github.com/Shinraya-Tech-Labs/AgentWatch/pull/753) | `feat(contracts): implement sequence-gap detection and dynamic capture profile (#730)` | 2026-10-19 | `e0b1ae07` |
| 24 | `apache/datafusion` | [#26465](https://github.com/apache/datafusion/pull/26465) | `fix(functions): pass correct number_rows in gcd benchmarks` | 2026-10-19 | `384d6464` |
| 25 | `existence-master/Sentient` | [#326](https://github.com/existence-master/Sentient/pull/326) | `fix(mcp): isolate OAuth credentials by server URL` | 2026-10-13 | `011d4650` |
| 26 | `existence-master/Sentient` | [#295](https://github.com/existence-master/Sentient/pull/295) | `fix(browser): preserve user downloads when attached` | 2026-10-12 | `0d7c8742` |
| 27 | `ThreeMoonsLab/agents-shipgate` | [#1007](https://github.com/ThreeMoonsLab/agents-shipgate/pull/1007) | `fix: support PEP 508 extras-qualified pins in dependency lock verification` | 2026-10-09 | `600dc8b3` |
| 28 | `huggingface/diffusers` | [#14961](https://github.com/huggingface/diffusers/pull/14961) | `Fix active adapter detection for text encoders` | 2026-10-08 | `e0415c41` |
| 29 | `knight22-21/CodePrism` | [#72](https://github.com/knight22-21/CodePrism/pull/72) | `fix: reject unknown configuration keys` | 2026-10-03 | `8b9c46eb` |
| 30 | `knight22-21/CodePrism` | [#70](https://github.com/knight22-21/CodePrism/pull/70) | `fix: parse requirement specifications correctly` | 2026-10-03 | `656d2de8` |
| 31 | `batrapulkit/squidbrake` | [#51](https://github.com/batrapulkit/squidbrake/pull/51) | `ci: test on Windows, macOS, and Python 3.13` | 2026-10-02 | `335260a9` |
| 32 | `corsairdev/corsair` | [#1398](https://github.com/corsairdev/corsair/pull/1398) | `feat: add Dynapictures plugin` | 2026-09-02 | `8b55578b` |

</details>

---

### B. Currently Open Contributions (16 PRs)

<details>
<summary><b>View All 16 Open Pull Requests and Current Status</b></summary>

| # | Repository | PR | Title / Engineering Scope | Category | Live Workflow / Review Status |
|:---:|---|:---:|---|:---:|---|
| 1 | `ThreeMoonsLab/agents-shipgate` | [#1141](https://github.com/ThreeMoonsLab/agents-shipgate/pull/1141) | `fix(privacy): include source-omission redactions in final privacy audit snapshot (#586)` | Mentored / Security | 15/15 CI checks passing; under maintainer review |
| 2 | `safetensors/safetensors` | [#927](https://github.com/safetensors/safetensors/pull/927) | `fix(torch): handle disjoint interleaved shared tensor views` | ML / SafeTensors | CI passing (DCO); storage deduplication fix for #926; awaiting maintainer review |
| 3 | `Lightning-AI/pytorch-lightning` | [#22006](https://github.com/Lightning-AI/pytorch-lightning/pull/22006) | `fix: set sampler epoch before creating resumed iterator` | Distributed ML | Community reviewed (@anishpentyala); core tests passing; awaiting maintainer review |
| 4 | `ionfwsrijan/PatchPilot` | [#354](https://github.com/ionfwsrijan/PatchPilot/pull/354) | `fix(findings): persist triaged status across page reloads` | Mentored / Security | Assigned by maintainer (Issue #320); backend tests passing; awaiting maintainer review |
| 5 | `Subodh-17/marine-pollution-intelligence` | [#9](https://github.com/Subodh-17/marine-pollution-intelligence/pull/9) | `fix(routing): calculate exact route-to-polygon distance with penetration` | Personal / GIS | Personal feature branch open; local test suite passing |
| 6 | `Lightning-AI/pytorch-lightning` | [#22017](https://github.com/Lightning-AI/pytorch-lightning/pull/22017) | `Improve error message for mixed strategy namespaces` | Distributed ML | 11/11 CI jobs passing; community reviewed (@anishpentyala); awaiting maintainer review |
| 7 | `huggingface/diffusers` | [#14990](https://github.com/huggingface/diffusers/pull/14990) | `fix: support torch compile for Qwen Image 2.1` | ML / Diffusers | 4/4 CI checks passing; awaiting maintainer triage |
| 8 | `huggingface/diffusers` | [#14971](https://github.com/huggingface/diffusers/pull/14971) | `Fix offline loading of sharded checkpoints` | ML / Diffusers | 4/4 CI checks passing; secret scan false-positive documented; awaiting maintainer triage |
| 9 | `huggingface/diffusers` | [#14983](https://github.com/huggingface/diffusers/pull/14983) | `fix: remove incorrect text_ids concatenation in Flux DreamBooth LoRA training` | ML / Diffusers | 4/4 CI checks passing; awaiting maintainer triage |
| 10 | `huggingface/diffusers` | [#14982](https://github.com/huggingface/diffusers/pull/14982) | `Fix prior preservation weighting in advanced DreamBooth LoRA` | ML / Diffusers | 4/4 CI checks passing; awaiting maintainer triage |
| 11 | `apache/arrow-rs` | [#12135](https://github.com/apache/arrow-rs/pull/12135) | `fix(variant): reject duplicate object keys in strict casts` | Core Rust / Arrow | Fork CI passing; strict policy freeze; awaiting maintainer evaluation |
| 12 | `huggingface/diffusers` | [#14984](https://github.com/huggingface/diffusers/pull/14984) | `fix: preserve singleton dimensions in numpy_to_pil` | ML / Diffusers | 4/4 CI checks passing; awaiting maintainer triage |
| 13 | `huggingface/diffusers` | [#14963](https://github.com/huggingface/diffusers/pull/14963) | `Validate PNDM inference step count` | ML / Diffusers | 4/4 CI checks passing; awaiting maintainer triage |
| 14 | `sanjaysaini383/observability-platform` | [#37](https://github.com/sanjaysaini383/observability-platform/pull/37) | `chore(dashboard): remove stray UI components directory` | Mentored / Infra | 7/7 CI checks passing; awaiting maintainer review |
| 15 | `modelscope/ms-swift` | [#10289](https://github.com/modelscope/ms-swift/pull/10289) | `fix: handle cli help command` | ML / LLM | Awaiting maintainer review |
| 16 | `TENET-DEV-AI/TENET-AI` | [#335](https://github.com/TENET-DEV-AI/TENET-AI/pull/335) | `feat(security): add agent action interposition layer` | AI Security | Automated bot review comments posted; CI security scan failing |

</details>

---

### C. Selected Closed Contributions & Engineering Investigations

<details>
<summary><b>View Selected Closed Investigations (11 Examples from 28 Closed Records)</b></summary>

*These records reflect substantive technical investigations, root-cause analyses, and implementations that were closed due to upstream organization AI policies, maintainer reassignments, or alternative architectural directions:*

| Repository | PR | Architectural Scope & Implementation | Context / Disposition |
|---|:---:|---|---|
| `apache/arrow-rs` | [#12280](https://github.com/apache/arrow-rs/pull/12280) | Display canonical Arrow type names in string/binary cast errors (#12214) | Closed — account-level AI-policy concern regarding excessive open PRs across unrelated repositories; no technical defect was stated in the closure comment. |
| `apache/datafusion` | [#27260](https://github.com/apache/datafusion/pull/27260) | Match Spark 4 encode charset behavior | Superseded by DataFusion-Spark subproject migration |
| `apache/datafusion` | [#26376](https://github.com/apache/datafusion/pull/26376) | Differentiate aggregate function schemas (#26221) | 1,200 LOC across 36 files; closed under organization AI policy on 2026-10-29 |
| `apache/datafusion` | [#26993](https://github.com/apache/datafusion/pull/26993) | Preserve min/max when merging all-null statistics | Closed following alternative statistics merge strategy |
| `mlflow/mlflow` | [#26432](https://github.com/mlflow/mlflow/pull/26432) | Token-level lexer for MCP server version filter normalization | Auto-closed by bot upon maintainer issue assignment |
| `mloda-ai/mloda` | [#1791](https://github.com/mloda-ai/mloda/pull/1791) | Scrub exception messages from error logs to prevent PII leakage | Privacy regex filtering in exception formatters |
| `mloda-ai/mloda` | [#1938](https://github.com/mloda-ai/mloda/pull/1938) | Resolve race condition in concurrent dataset joins | Concurrency barrier synchronization |
| `huggingface/transformers` | [#49298](https://github.com/huggingface/transformers/pull/49298) | Skip redundant CPU materialization for FSDP2 in from_pretrained | Memory-efficient streaming initialization |
| `huggingface/transformers` | [#49712](https://github.com/huggingface/transformers/pull/49712) | Grouped RMSNorm in Mamba2 non-fused path | Closed upstream during kernel refactoring |
| `safetensors/safetensors` | [#873](https://github.com/safetensors/safetensors/pull/873) | Allow slicing zero-length dimensions | Empty tensor slice boundary validation |
| `airbytehq/airbyte` | [#87507](https://github.com/airbytehq/airbyte/pull/87507) | HubSpot configurable property history | Bot auto-closed |

*Note: An additional 17 closed records across MLflow, mloda, Hugging Face, and SafeTensors are cataloged in the canonical audit ledger.*

</details>

---

## 7. Comprehensive Technology Stack & Implementation Scope

*Every technology, programming language, and framework listed below is verified by direct commits, PR diffs, or architecture implementations across my original systems and open-source work.*

### A. Programming Languages
<a href="#"><img src="https://skillicons.dev/icons?i=python,rust,ts,js,solidity,bash,html,css" alt="Python, Rust, TypeScript, JavaScript, Solidity, Bash, HTML5, CSS3" /></a>

| Language | Verified Version / Scope | Primary Implementation Context |
|---|---|---|
| **Python** | 3.10 – 3.13 | Core ML/agent infrastructure (PyTorch, Diffusers, AgentWatch, Shipgate, Marine Pollution, Logistics) |
| **Rust** | 2021 Edition / Cargo | DataFusion SIMD benchmarks (`#26465`), DataFusion-Spark (`#116`, `#118`, `#119`), Arrow-rs (`#12135`), WhatBreaks (`#27`) |
| **TypeScript** | 5.x / Strict Mode | DevTrack Clerk sync hardening (`#171`), PatchPilot triage persistence (`#350`, `#354`), Corsair SDK (`#1398`) |
| **JavaScript** | ES2022+ / Node.js 20+ | OpenSourceMate metric sync (`#245`), Blueledger REST API, Marine Pollution interactive SPA |
| **Solidity** | 0.8.20 / Hardhat | Batch-tracked ecological carbon credit registry smart contract (`BlueCarbonRegistry.sol`) |
| **SQL** | PostgreSQL 16+ / SQLite | Relational schema modeling, PostGIS spatial geography queries, ACID transaction isolation |
| **Scilab** | Native Numerical Engine | StockVision time-series forecasting, OLS polynomial fitting, walk-forward validation |
| **Bash** | Linux / macOS / WSL | GitHub Actions matrix automation, local container bootstrapping, environment orchestration |
| **HTML5 & CSS3** | Modern Standards | Responsive web application design, Leaflet GIS dashboards, theme-adaptive UI layouts |

---

### B. Frontend & User Interface Engineering
<a href="#"><img src="https://skillicons.dev/icons?i=react,vite,tailwind,html,css,ts,js" alt="React, Vite, Tailwind CSS, HTML5, CSS3, TypeScript, JavaScript" /></a>

| Technology | Ecosystem Role | Verified Project Implementation |
|---|---|---|
| **React** | 18.x & 19.x SPAs | Dynamic geospatial dashboards in Marine Pollution Intelligence and Predictive Logistics SIH 26251 |
| **Vite** | Build Tooling & HMR | Asset compilation and optimized static production builds for web applications |
| **Tailwind CSS** | Design System | Utility-first responsive styling and typography for freight dispatch and security triage interfaces |
| **Leaflet & React-Leaflet** | Interactive GIS Mapping | Vector geospatial overlays, radar oil-slick contours, vessel tracking, and terrain route paths |
| **Recharts** | Data Visualization | Real-time sensor telemetry, demand forecasting horizons, and stock equity curve visualization |

---

### C. Backend Architecture & High-Throughput APIs
<a href="#"><img src="https://skillicons.dev/icons?i=fastapi,nodejs,express" alt="FastAPI, Node.js, Express" /></a>

| Technology | Framework / Component | Verified Architecture Context |
|---|---|---|
| **FastAPI** | ASGI / Python 3.12+ | Asynchronous REST microservices in Marine Pollution Intelligence and Predictive Logistics |
| **Node.js & Express** | Event-Driven Runtime | REST API services, role middleware, and event dispatcher in Blueledger backend |
| **Pydantic** | Schema Validation (v2) | Type-safe data validation, request parsing, and environment configuration management |
| **Prisma & SQLAlchemy** | ORMs & Spatial Queries | Prisma interactive transactions in DevTrack (`#171`), PostGIS spatial geography in Logistics |
| **REST & JSON-RPC 2.0** | Protocols | OpenTelemetry span ingestion, MCP client/server handshakes, and public registry API endpoints |

---

### D. AI, Machine Learning & Systems Performance
<a href="#"><img src="https://skillicons.dev/icons?i=pytorch,tensorflow,sklearn,opencv,numpy,pandas" alt="PyTorch, TensorFlow, Scikit-Learn, OpenCV, NumPy, Pandas" /></a>

| Technology | Framework / Engine | Contribution & Application Highlights |
|---|---|---|
| **PyTorch** | Deep Learning Core | PEFT LoRA adapter routing in Diffusers (`#14961`), distributed iterator mechanics in Lightning AI (`#22006`) |
| **Hugging Face Diffusers** | Diffusion Infrastructure | Text encoder adapter introspection (`#14961`), Qwen Image compile (`#14990`), DreamBooth LoRA |
| **PyTorch Lightning** | Distributed Training | Resumed dataset checkpoint ordering in `FitLoop` (`#22006`), accelerator connector diagnostics (`#22017`) |
| **ONNX Runtime** | Production Inference | CPU-optimized embedded satellite oil slick segmentation models (`SpillUNet` + `SceneClassifier`) |
| **Scikit-Learn & LightGBM** | Statistical ML | 7/14/30-day cross-validated forward demand forecasting and shortage classification in logistics |
| **NumPy & SciPy** | Scientific Computing | 7x7 Lee speckle filter window convolutions, 2D Euler hydrodynamic drift hindcast integration |
| **SAR Remote Sensing** | Sentinel-1 Radar | Copernicus Sentinel-1 radar imagery processing, radar sea clutter attenuation, dark slick extraction |

---

### E. Storage, Web3 & Cloud Infrastructure
<a href="#"><img src="https://skillicons.dev/icons?i=postgres,sqlite,ipfs,docker,githubactions,git,github,linux,windows" alt="PostgreSQL, SQLite, IPFS, Docker, GitHub Actions, Git, GitHub, Linux, Windows" /></a>

| Technology | Platform / Component | Implementation Scope |
|---|---|---|
| **PostgreSQL & PostGIS** | Geospatial Database | Production persistence for logistics routing orders and PostGIS spatial geography queries |
| **SQLite** | Embedded Datastore | High-performance, zero-dependency local metadata cache in Marine Pollution Intelligence |
| **IPFS (Kubo & Pinata)** | Decentralized Storage | Content-addressed immutable storage and pinning of ecological audit evidence files |
| **Solidity & Hardhat** | Smart Contracts | Batch credit registry contract with verified state transition rules and access control |
| **Docker & Docker Compose** | Containerization | Multi-container microservice definitions (API, PostGIS, frontend, mock telemetry feeds) |
| **GitHub Actions** | CI/CD Pipelines | Cross-platform multi-OS test matrix orchestration across Ubuntu Linux, Windows, and macOS (`#51`) |

---

### F. Agent Runtimes, Observability & Protocols

| Technology | Protocol / Standard | Production Contribution Context |
|---|---|---|
| **OpenTelemetry (OTel)** | GenAI v2 Conventions | Zero-dependency protocol normalizer mapping spans, tokens, and tool calls in AgentWatch (`#757`) |
| **Model Context Protocol (MCP)**| JSON-RPC 2.0 Clients | Scoped OAuth credentials by server URL (`Sentient#326`), MCP error normalizers (`AgentWatch#784`) |
| **Allen's Interval Algebra** | Formal Verification | Causal DAG validation engine verifying multi-agent temporal execution (`AgentWatch#754`) |
| **RFC 4648 & Base64** | Data Normalization | Hardened lookaround secret redaction handling URL-safe Base64 and unpadded keys (`#1106`) |
| **PEP 508 & PEP 440** | Python Packaging | Extras-qualified lock verification (`#1007`) and complex version specifier parsing (`#70`) |
| **ISO 8601** | Temporal Formatting | Deterministic scalar canonicalization during configuration hashing (`#1105`) |

---

## 8. Open-Source Ecosystem Focus & Strategic Alignment

I actively focus my open-source contributions, design studies, and engineering depth across ecosystems where systems performance, correctness, and data engineering intersect:

1. **The Apache Software Foundation (ASF):**
   - *Target Ecosystems:* **Apache DataFusion** and **Apache Arrow-rs**.
   - *Demonstrated Alignment:* Merged Rust code in DataFusion Criterion benchmark harnesses (`#26465`), merged Rust contributions to Apache DataFusion-Spark 4 expression compatibility (`#116`, `#118`, `#119`), and Parquet Variant duplicate key validation in Arrow-rs (`#12135`).
   - *Focus Areas:* Columnar memory representations, vectorized SIMD execution kernels, logical/physical query optimization, and memory-safe zero-copy IPC.
2. **PyTorch / The Linux Foundation / Lightning AI:**
   - *Target Ecosystems:* Distributed training infrastructure, executor determinism, and dynamic compilation.
   - *Demonstrated Alignment:* Root-cause fixes in `pytorch-lightning` `FitLoop` dataset sampler order (`#22006`), accelerator connector diagnostics (`#22017`), and formal review approval of checkpoint resumption fixes (`#22182`).
3. **Hugging Face Ecosystem:**
   - *Target Ecosystems:* **Diffusers**, **PEFT**, and **SafeTensors**.
   - *Demonstrated Alignment:* Merged adapter introspection across multi-text-encoder pipelines (`#14961`), 6 active PRs spanning `torch.compile` compatibility, sharded checkpoint resolution, and prior-preservation loss scaling; SafeTensors strided tensor deduplication (`#927`).

---

## 9. Verification & Professional Contact

All public pull requests, merge commits, formal code reviews, unit tests, and open-source project codebases cited in this profile can be independently inspected and verified through public upstream GitHub repositories. Project code developed within private hackathon environments (`PROTEA-X-AI`) is private and may not be publicly accessible.

<div align="center">

[![GitHub](https://img.shields.io/badge/GitHub-Subodh--17-0f172a?style=flat-square&logo=github&logoColor=white)](https://github.com/Subodh-17)
&nbsp;
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Subodh-0a66c2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/subodh-b-b705b5403)
&nbsp;
[![Email](https://img.shields.io/badge/Email-subodh171011%40gmail.com-ea4335?style=flat-square&logo=gmail&logoColor=white)](mailto:subodh171011@gmail.com)

</div>

- **GitHub Profile:** [`@Subodh-17`](https://github.com/Subodh-17)
- **LinkedIn Profile:** [`Subodh`](https://www.linkedin.com/in/subodh-b-b705b5403)
- **Primary Email:** `subodh171011@gmail.com`
- **Location:** Maharashtra, India
- **Availability:** Open for systems engineering roles, open-source collaborations, and technical project discussions.
