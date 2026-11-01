# Subodh

[![GitHub](https://img.shields.io/badge/GitHub-Subodh--17-0f172a?style=flat-square&logo=github&logoColor=white)](https://github.com/Subodh-17)
[![Merged Upstream](https://img.shields.io/badge/Merged_PRs-18_Upstream-10b981?style=flat-square&logo=git&logoColor=white)](https://github.com/Subodh-17)
[![Under Review](https://img.shields.io/badge/Open_PRs-7_Active-2563eb?style=flat-square&logo=github&logoColor=white)](https://github.com/Subodh-17)
[![Rust](https://img.shields.io/badge/Rust-DataFusion-0f172a?style=flat-square&logo=rust&logoColor=white)](https://www.rust-lang.org)
[![Python](https://img.shields.io/badge/Python-3.10_--_3.13-0f172a?style=flat-square&logo=python&logoColor=white)](https://python.org)
[![PyTorch](https://img.shields.io/badge/PyTorch-Distributed_&_LoRA-0f172a?style=flat-square&logo=pytorch&logoColor=white)](https://pytorch.org)

Systems and open-source engineer focused on **AI agent runtimes, machine learning infrastructure, privacy engineering, and high-performance data query engines**. Contributor to open-source ecosystems including Apache DataFusion, Hugging Face, Lightning AI, and AI agent infrastructure projects.

---

## 1. Verified Contribution Scorecard

| Category | Verified Count | Scope & Verification Source |
|---|:---:|---|
| **Merged Upstream Pull Requests** | **18** | Merged into upstream repositories (Apache DataFusion, Hugging Face Diffusers, AgentWatch, Sentient, etc.) |
| **Active Open Pull Requests** | **7** | Live upstream PRs undergoing maintainer review (PyTorch Lightning, Shipgate, PatchPilot, SafeTensors, MS-Swift) |
| **Blocked Open Pull Requests** | **8** | Open on GitHub; currently unable to progress upstream due to contributor organization restriction (1 Transformers, 7 Diffusers) |
| **Closed / Unmerged PRs (Cataloged)** | **22** | Documented in master ledger (10 substantive examples detailed below; 12 iterative/bot-closed in ledger) |
| **Upstream Repositories Contributed To** | **12+** | Query engines, distributed ML runtimes, agent frameworks, developer tooling |
| **Independent Flagship Projects** | **4** | Original systems spanning satellite radar segmentation, freight optimization, quantitative trading, and Web3 MRV |

---

## 2. High-Leverage Open-Source Case Studies

### A. High-Performance Query Engines (Rust)

* **[apache/datafusion#26465](https://github.com/apache/datafusion/pull/26465)** — `fix(functions): pass correct number_rows in gcd benchmarks` (**MERGED**)
  * *Problem:* In the Apache DataFusion scalar SIMD mathematical benchmark harness (`datafusion/functions/benches/gcd.rs`), array fixture construction passed mismatched row count arguments, corrupting greatest common divisor throughput measurements.
  * *Implementation:* Corrected parameter plumbing in the criterion benchmark harness to propagate exact configured row counts across all benchmark matrices. Merged upstream by PMC Chair Andrew Lamb on 2026-10-19.

---

### B. AI Agent Runtimes, Formal Verification & Observability

* **[Shinraya-Tech-Labs/AgentWatch#753](https://github.com/Shinraya-Tech-Labs/AgentWatch/pull/753)** — `feat(contracts): implement sequence-gap detection and dynamic capture profile introspection` (**MERGED**)
  * *Problem:* Telemetry contract evaluation misclassified network transport drops as contract violations (`REFUTED`) due to static counter heuristics.
  * *Implementation:* Built `SequenceGap` and `SequenceContinuityTracker` in `agentwatch/contracts/coverage.py`. Dynamically introspected telemetry sequence streams (`sensor_id:seq`), downgrading false refutations to `INCONCLUSIVE` during detected drop windows. Verified across 1,256 unit tests with 1%, 5%, and 20% simulated packet drop rates.
* **[Shinraya-Tech-Labs/AgentWatch#754](https://github.com/Shinraya-Tech-Labs/AgentWatch/pull/754)** — `feat(contracts): implement interval temporal logic and happens-before ordering` (**MERGED**)
  * *Problem:* Telemetry evaluator lacked support for multi-agent concurrency and partial-order causal reasoning.
  * *Implementation:* Built a partial-order causal DAG engine and implemented Allen's Interval Algebra operators (`meets`, `overlaps`, `during`, `starts`, `finishes`) in `agentwatch/contracts/temporal.py` to formally verify concurrent multi-agent executions.
* **[Shinraya-Tech-Labs/AgentWatch#757](https://github.com/Shinraya-Tech-Labs/AgentWatch/pull/757)** — `feat(normalizers): implement OTel GenAI v2 and MCP protocol normalizers` (**MERGED**)
  * *Problem:* Ingestion schema validation failed on emerging telemetry from OpenTelemetry GenAI semantic conventions v2 and Model Context Protocol (MCP / JSON-RPC 2.0) clients.
  * *Implementation:* Developed zero-dependency protocol normalizers in `agentwatch/normalizers/` mapping OTel GenAI spans, token usage, tool invocations, and MCP JSON-RPC payloads into standard internal events.
* **[existence-master/Sentient#326](https://github.com/existence-master/Sentient/pull/326)** — `fix(mcp): isolate OAuth credentials by server URL` (**MERGED**)
  * *Problem:* Multi-server MCP configurations shared OAuth credentials across server instances due to a unified credential lookup key.
  * *Implementation:* Scoped OAuth token storage and refresh routines by normalized MCP server endpoint URL, preventing credentials from being inadvertently shared across server configurations.
* **[DivyashreeR008/Open-Agents#406](https://github.com/DivyashreeR008/Open-Agents/pull/406)** — `test(recommendation): add automated scoring tests` (**MERGED**)
  * *Problem:* Recommendation and task routing algorithms lacked regression test suites, risking silent ranking regressions during weight adjustments.
  * *Implementation:* Authored a 58-test regression harness (+799 LOC) testing mathematical properties: monotonic weight scaling, deterministic tie-breaking, empty pools, and boundary value inputs (0.0, 1.0).

---

### C. Machine Learning Infrastructure & Diffusion Tooling

* **[huggingface/diffusers#14961](https://github.com/huggingface/diffusers/pull/14961)** — `Fix active adapter detection for text encoders` (**MERGED**)
  * *Problem:* Querying `pipe.get_active_adapters()` failed to detect active LoRA adapters when applied specifically to secondary text encoders (`text_encoder_2`) in SDXL and Flux pipelines.
  * *Implementation:* Extended adapter introspection across all registered text encoder submodules, aggregating active adapter names while gracefully bypassing non-PEFT modules.
* **[Lightning-AI/pytorch-lightning#22006](https://github.com/Lightning-AI/pytorch-lightning/pull/22006)** — `fix: set sampler epoch before creating resumed iterator` (**OPEN — COMMUNITY VERIFIED**)
  * *Problem:* In `FitLoop`, resumed training iterators were instantiated before the sampler epoch was updated, causing non-deterministic data sampling upon checkpoint resumption.
  * *Implementation:* Corrected execution order to update sampler epoch prior to creating the resumed data iterator. Verified across 12 worker-prefetch traces by community reviewer `anishpentyala`.
* **[Lightning-AI/pytorch-lightning#22017](https://github.com/Lightning-AI/pytorch-lightning/pull/22017)** — `Improve error message for mixed strategy namespaces` (**OPEN — 11/11 CI GREEN**)
  * *Problem:* Conflicting strategy configuration flags produced ambiguous exceptions during accelerator initialization.
  * *Implementation:* Enhanced diagnostic messaging in `AcceleratorConnector` to provide explicit namespace disambiguation and actionable resolution steps. Verified with 165 test cases passing.

---

### D. Systems Security, Privacy & Secret Redaction

* **[ThreeMoonsLab/agents-shipgate#1106](https://github.com/ThreeMoonsLab/agents-shipgate/pull/1106)** — `fix(privacy): redact AWS path keys and URL-safe Basic credentials` (**OPEN — 13 PASSING, 1 SKIPPED**)
  * *Problem:* AWS secret access keys inside URL/filesystem paths (`path/<key>`, `s3://.../<key>`) bypassed redaction due to `/` exclusion in regex lookarounds. Basic credentials using URL-safe Base64 (`-`, `_`) or unpadded strings caused false negatives or decoding crashes.
  * *Implementation:* Hardened regex lookarounds in `src/agents_shipgate/core/privacy.py` to permit path separators while preserving token entropy checks. Added RFC 4648 Base64 character normalization, safe repadding, and `len % 4 == 1` rejection. Verified across 32 targeted regression tests; CI reports 13 passing jobs and 1 expected skipped job.
* **[ThreeMoonsLab/agents-shipgate#1105](https://github.com/ThreeMoonsLab/agents-shipgate/pull/1105)** — `fix(host-grants): handle YAML timestamps in config hashing` (**OPEN — 13 PASSING, 1 SKIPPED**)
  * *Problem:* Host grant configurations containing date or timestamp scalars crashed cryptographic hashing with `TypeError: Object of type date is not JSON serializable`.
  * *Implementation:* Implemented deterministic ISO 8601 formatting for `date` and `datetime` scalars in `_canonical()` within `src/agents_shipgate/core/host_grants.py` while strictly preserving secret redaction precedence. Balanced test partition runtime weights in `tests/shard_seconds.json`. Verified across 9 targeted regression tests; CI reports 13 passing jobs and 1 expected skipped job.
* **[ionfwsrijan/PatchPilot#354](https://github.com/ionfwsrijan/PatchPilot/pull/354)** — `fix(findings): persist triaged status across page reloads` (**OPEN — CI GREEN**)
  * *Problem:* Security findings triaged as accepted or ignored silently reset to open upon browser reload due to client-side hydration dropping backend state.
  * *Implementation:* Synchronized TypeScript contracts in `api.ts` and updated hydration mapping in `frontend/src/app/lib/mappers.ts` to preserve database status with `"open"` fallback. Added 217 LOC backend test suite and frontend unit tests.

---

## 3. Upstream Contribution Inventories

### A. Merged Upstream Pull Requests (18 PRs)

<details>
<summary><b>View Verified Merged Upstream Pull Requests (18)</b></summary>

| Repository | PR | Title | Merge Date | Merge SHA |
|---|:---:|---|:---:|:---:|
| `apache/datafusion` | [#26465](https://github.com/apache/datafusion/pull/26465) | fix(functions): pass correct number_rows in gcd benchmarks | 2026-10-19 | `384d6464` |
| `huggingface/diffusers` | [#14961](https://github.com/huggingface/diffusers/pull/14961) | Fix active adapter detection for text encoders | 2026-10-08 | `e0415c41` |
| `Shinraya-Tech-Labs/AgentWatch` | [#753](https://github.com/Shinraya-Tech-Labs/AgentWatch/pull/753) | feat(contracts): sequence-gap detection & dynamic capture profile | 2026-10-19 | `c2f55ba1` |
| `Shinraya-Tech-Labs/AgentWatch` | [#754](https://github.com/Shinraya-Tech-Labs/AgentWatch/pull/754) | feat(contracts): interval temporal logic and happens-before ordering | 2026-10-20 | `4ea16af8` |
| `Shinraya-Tech-Labs/AgentWatch` | [#757](https://github.com/Shinraya-Tech-Labs/AgentWatch/pull/757) | feat(normalizers): implement OTel GenAI v2 and MCP normalizers | 2026-10-20 | `625c3da9` |
| `Shinraya-Tech-Labs/AgentWatch` | [#784](https://github.com/Shinraya-Tech-Labs/AgentWatch/pull/784) | feat(mcp): add MCP error normalizer and code classifier | 2026-10-26 | `416444a7` |
| `ThreeMoonsLab/agents-shipgate` | [#1007](https://github.com/ThreeMoonsLab/agents-shipgate/pull/1007) | fix: support PEP 508 extras-qualified pins in lock verification | 2026-10-09 | `600dc8b3` |
| `Karan-Raj-KR/crewai-recipes` | [#229](https://github.com/Karan-Raj-KR/crewai-recipes/pull/229) | feat(playground): basic in-memory rate limiting to prevent loops | 2026-10-24 | `fece08a3` |
| `Karan-Raj-KR/crewai-recipes` | [#242](https://github.com/Karan-Raj-KR/crewai-recipes/pull/242) | feat(customer-onboarding): add --json output flag | 2026-10-28 | `c279a9d7` |
| `ionfwsrijan/PatchPilot` | [#350](https://github.com/ionfwsrijan/PatchPilot/pull/350) | feat(security): prioritize findings by normalized severity | 2026-10-23 | `94950e40` |
| `DivyashreeR008/Open-Agents` | [#406](https://github.com/DivyashreeR008/Open-Agents/pull/406) | test(recommendation): add automated scoring tests | 2026-10-20 | `a0d1ff8e` |
| `batrapulkit/squidbrake` | [#51](https://github.com/batrapulkit/squidbrake/pull/51) | ci: test on Windows, macOS, and Python 3.13 | 2026-10-02 | `335260a9` |
| `existence-master/Sentient` | [#326](https://github.com/existence-master/Sentient/pull/326) | fix(mcp): isolate OAuth credentials by server URL | 2026-10-13 | `011d4650` |
| `existence-master/Sentient` | [#295](https://github.com/existence-master/Sentient/pull/295) | fix(browser): preserve user downloads when attached | 2026-10-12 | `0d7c8742` |
| `knight22-21/CodePrism` | [#72](https://github.com/knight22-21/CodePrism/pull/72) | fix: reject unknown configuration keys | 2026-10-03 | `8b9c46eb` |
| `knight22-21/CodePrism` | [#70](https://github.com/knight22-21/CodePrism/pull/70) | fix: parse requirement specifications correctly | 2026-10-03 | `656d2de8` |
| `aeshef/obsidian-agent` | [#68](https://github.com/aeshef/obsidian-agent/pull/68) | feat: add per-chart reset control | 2026-10-30 | `d84b7db5` |
| `corsairdev/corsair` | [#1398](https://github.com/corsairdev/corsair/pull/1398) | feat: add Dynapictures plugin | 2026-09-02 | `8b55578b` |

</details>

---

### B. Active Open Pull Requests (7 PRs)

<details>
<summary><b>View Active Open Pull Requests Awaiting Review (7)</b></summary>

| Repository | PR | Title | Status | Verification & Review Evidence |
|---|:---:|---|:---:|---|
| `ThreeMoonsLab/agents-shipgate` | [#1105](https://github.com/ThreeMoonsLab/agents-shipgate/pull/1105) | fix(host-grants): handle YAML timestamps in config hashing | OPEN | 13 passing jobs, 1 expected skipped job; 9 targeted regression tests |
| `ThreeMoonsLab/agents-shipgate` | [#1106](https://github.com/ThreeMoonsLab/agents-shipgate/pull/1106) | fix(privacy): redact AWS path keys and URL-safe Basic credentials | OPEN | 13 passing jobs, 1 expected skipped job; 32 targeted regression tests |
| `ionfwsrijan/PatchPilot` | [#354](https://github.com/ionfwsrijan/PatchPilot/pull/354) | fix(findings): persist triaged status across page reloads | OPEN | Functional CI green (backend & frontend suites passing; 217 LOC test harness) |
| `Lightning-AI/pytorch-lightning` | [#22006](https://github.com/Lightning-AI/pytorch-lightning/pull/22006) | fix: set sampler epoch before creating resumed iterator | OPEN | Community-verified through 12 worker-prefetch traces (@anishpentyala) |
| `Lightning-AI/pytorch-lightning` | [#22017](https://github.com/Lightning-AI/pytorch-lightning/pull/22017) | Improve error message for mixed strategy namespaces | OPEN | 11/11 CI jobs passed; verified with 165 tests (@anishpentyala) |
| `safetensors/safetensors` | [#873](https://github.com/safetensors/safetensors/pull/873) | fix: allow slicing zero-length dimensions | OPEN | Automated CI checks passing on PR branch |
| `modelscope/ms-swift` | [#10289](https://github.com/modelscope/ms-swift/pull/10289) | fix: handle cli help command | OPEN | Automated CI checks passing on PR branch |

</details>

---

### C. Blocked Open Pull Requests (8 PRs)

<details>
<summary><b>View Blocked Open Pull Requests (8)</b></summary>

*These pull requests remain open on GitHub but are currently unable to progress upstream due to an organization-level contributor account restriction instituted in October 2026:*

| Repository | PR | Title | Status | Scope / Verification |
|---|:---:|---|:---:|---|
| `huggingface/transformers` | [#49192](https://github.com/huggingface/transformers/pull/49192) | AutoTokenizer backend selection for tiny-aya | OPEN (BLOCKED) | Rust tokenizer mapping; 119k CI tests green |
| `huggingface/diffusers` | [#14990](https://github.com/huggingface/diffusers/pull/14990) | torch compile for Qwen Image 2.1 | OPEN (BLOCKED) | Pipeline torch.compile compatibility |
| `huggingface/diffusers` | [#14989](https://github.com/huggingface/diffusers/pull/14989) | prevent cross-variant shard deletion | OPEN (BLOCKED) | Checkpoint pruning shard preservation |
| `huggingface/diffusers` | [#14984](https://github.com/huggingface/diffusers/pull/14984) | preserve singleton dimensions in numpy_to_pil | OPEN (BLOCKED) | Array dimension handling |
| `huggingface/diffusers` | [#14983](https://github.com/huggingface/diffusers/pull/14983) | correct text_ids shape in Flux DreamBooth | OPEN (BLOCKED) | LoRA training tensor shapes |
| `huggingface/diffusers` | [#14982](https://github.com/huggingface/diffusers/pull/14982) | prior preservation weighting in DreamBooth | OPEN (BLOCKED) | Prior loss scaling |
| `huggingface/diffusers` | [#14971](https://github.com/huggingface/diffusers/pull/14971) | offline loading of sharded checkpoints | OPEN (BLOCKED) | Hub offline checkpoint loading |
| `huggingface/diffusers` | [#14963](https://github.com/huggingface/diffusers/pull/14963) | correct PNDM scheduler inference step count | OPEN (BLOCKED) | Step count validation on odd intervals |

</details>

---

### D. Selected Closed / Unmerged Engineering Work (10 Substantive Examples)

<details>
<summary><b>View Selected Closed / Unmerged Contributions (10 Substantive Examples)</b></summary>

*These 10 contributions represent selected substantive engineering investigations, root-cause analyses, and implementations that were closed due to upstream policy shifts, maintainer reassignments, or bot auto-closures. They are explicitly marked **CLOSED / UNMERGED** and are not presented as accepted upstream code. An additional 12 iterative, exploratory, or bot-closed pull requests (across MLflow, mloda, and SafeTensors) are cataloged in the local master ledger and are not individually reproduced in this summary table:*

| Repository | PR | Title & Engineering Scope | Status | Outcome / Notes |
|---|:---:|---|:---:|---|
| `apache/datafusion` | [#26376](https://github.com/apache/datafusion/pull/26376) | Differentiate aggregate function schemas (#26221) | CLOSED / UNMERGED | 1,200 lines across 36 files; closed under AI Dump policy on 2026-10-29 |
| `mlflow/mlflow` | [#26432](https://github.com/mlflow/mlflow/pull/26432) | Token-level lexer for MCP server version filter normalization | CLOSED / UNMERGED | Auto-closed by bot upon maintainer issue assignment |
| `mloda-ai/mloda` | [#1791](https://github.com/mloda-ai/mloda/pull/1791) | Scrub exception messages from error logs to prevent PII leakage | CLOSED / UNMERGED | Privacy regex filtering in exception formatters |
| `mloda-ai/mloda` | [#1938](https://github.com/mloda-ai/mloda/pull/1938) | Resolve race condition in concurrent dataset joins | CLOSED / UNMERGED | Recognized on XERJ Corpus Hub contributor profile |
| `huggingface/transformers` | [#49298](https://github.com/huggingface/transformers/pull/49298) | Skip redundant CPU materialization for FSDP2 in from_pretrained | CLOSED / UNMERGED | Memory-efficient streaming initialization |
| `safetensors/safetensors` | [#869](https://github.com/safetensors/safetensors/pull/869) | Allow empty slices on zero-sized dimensions | CLOSED / UNMERGED | Superseded by active PR #873 |
| `huggingface/transformers` | [#49712](https://github.com/huggingface/transformers/pull/49712) | Grouped RMSNorm in Mamba2 non-fused path | CLOSED / UNMERGED | Closed upstream; triggered contributor block |
| `existence-master/Sentient` | [#274](https://github.com/existence-master/Sentient/pull/274) | Preserve Hermes delivery in skipped job previews | CLOSED / UNMERGED | Superseded |
| `knight22-21/CodePrism` | [#66](https://github.com/knight22-21/CodePrism/pull/66) | Validate search kind | CLOSED / UNMERGED | Superseded by merged PR #70 |
| `airbytehq/airbyte` | [#87507](https://github.com/airbytehq/airbyte/pull/87507) | HubSpot configurable property history | CLOSED / UNMERGED | Bot auto-closed |

*Note: The remaining 12 iterative, superseded, or bot-closed pull requests (across MLflow, mloda, and SafeTensors) are cataloged in the local master ledger and are not individually reproduced in this summary table.*

</details>

---

## 4. Flagship Original Engineering Projects

### Marine Pollution Intelligence
**Repository:** [`Subodh-17/marine-pollution-intelligence`](https://github.com/Subodh-17/marine-pollution-intelligence)  
*Autonomous satellite radar (SAR) oil spill segmentation, hydrodynamic drift hindcasting, and vessel attribution.*

- **SAR Oil Slick Segmentation:** Implemented adaptive local Gaussian thresholding (`detection.py:287`) preceded by 7x7 Lee speckle filtering to suppress radar sea clutter while preserving dark slick boundaries.
- **Hydrodynamic Drift Hindcasting:** 2D Euler trajectory hindcasting model integrating surface wind shear (3% rule) and NOAA/HYCOM ocean current vectors (`drift/model.py`).
- **AIS Vessel Attribution:** Multi-factor attribution engine (`scoring/attribution.py`) computing spatial-temporal proximity, vessel type weights, speed anomalies, and draft variances.
- **Inference Runtime:** ONNX Runtime for optimized local model inference with SQLite/PostgreSQL metadata persistence.

```
SAR Imagery (Sentinel-1) ──> Lee Speckle Filter (7x7) ──> Adaptive Local Gaussian ──> Slick Polygons
                                                                                            │
AIS Vessel Feeds         ──> Speed / Proximity Anomaly ──> 2D Euler Drift Hindcast <────────┘
                                                                   │
                                                      Attribution Probability Score
```

---

### Predictive Logistics SIH 26251
**Repository:** [`Subodh-17/Predictive_Logistics_SIH_26251`](https://github.com/Subodh-17/Predictive_Logistics_SIH_26251)  
*Terrain- and weather-aware dynamic multi-modal freight routing and priority dispatching system.*

- **Dynamic Multi-Modal Routing:** Terrain- and weather-aware graph traversal engine incorporating elevation gradients and severe weather penalties with an enforced 8 km/h speed floor (`terrain.py`).
- **7-Factor Priority Dispatching:** Algorithmic queue weighting perishability, medical criticality, contract SLAs, transport costs, and route reliability (`priority.py`).
- **Geospatial Storage:** PostgreSQL with PostGIS extension and GeoAlchemy2 spatial queries (`models.py`). 483 automated unit/integration tests passing.

```
Consignment Orders ──> 7-Factor Priority Engine ──> Ranked Dispatch Queue
                             │
Weather / DEM Feeds ──> Elevation & Storm Penalties ──> Dynamic Graph Routing (A*)
                                                              │
                                                Constrained Path (>= 8 km/h Floor)
```

---

### StockVision Scilab GUI
**Repository:** [`Subodh-17/stockvision-scilab-gui`](https://github.com/Subodh-17/stockvision-scilab-gui)  
*Quantitative time-series modeling and walk-forward algorithmic trading backtester in pure Scilab.*

- **Algorithmic Quantitative Engine:** Implemented in pure native Scilab (`model_engine.sce`).
- **Time-Series Models:** Ordinary Least Squares (OLS) polynomial trend fitting, Autoregressive AR(p) modeling, and Holt double exponential smoothing.
- **Execution Simulation:** Walk-forward backtesting engine incorporating realistic bid-ask slippage and transaction cost modeling.

```
Price & Volume Data ──> OLS Polynomial Trend ──> Residual Detrending
                                                        │
Execution Engine    <── Walk-Forward Backtester <── AR(p) + Holt Smoothing
(Slippage + Costs)
```

---

### Blueledger
**Repository:** [`Subodh-17/Blueledger`](https://github.com/Subodh-17/Blueledger)  
*Decentralized MRV (Measurement, Reporting, and Verification) registry for blue carbon credits.*

- **Smart Contract Layer:** Solidity 0.8.20 credit registry contract (`BlueCarbonRegistry.sol`) with role-based access control (verifier, admin, registrar) and permanent certificate retirement mechanics.
- **Web3 Integration:** Ethers.js v6 for transactional signing, event listener subscriptions, and gas estimation.
- **Decentralized Storage:** IPFS integration (Kubo RPC & Pinata) for immutable audit evidence and satellite MRV proof pinning (`storage.js`).

```
Satellite / In-Situ MRV ──> IPFS Evidence Ingestion ──> Cryptographic Hash CID
                                                               │
Independent Verifier    ──> Role-Based Auditor Verification ──> Traceable Credit Issuance
                                                               │
                                                   On-Chain Retirement Event
```

---

## 5. Technical Capabilities Matrix

| Domain | Core Technologies & Systems |
|---|---|
| **Languages** | Python (3.10–3.13), Rust, TypeScript, JavaScript (Node.js), SQL, Solidity (0.8.20), Scilab, Bash |
| **ML & Diffusion Infrastructure** | PyTorch, Hugging Face Diffusers, PyTorch Lightning, SafeTensors, ONNX Runtime, PEFT / LoRA |
| **Agent Runtimes & Observability** | OpenTelemetry GenAI v2, Model Context Protocol (MCP / JSON-RPC 2.0), LangChain, CrewAI, AgentWatch |
| **Data & Storage Systems** | Apache DataFusion (SIMD/Arrow), PostgreSQL / PostGIS, SQLite, SQLAlchemy, GeoAlchemy2, Redis, IPFS |
| **Verification & CI/CD** | Pytest, Cargo Bench/Test, GitHub Actions Matrix CI, Ruff, Bandit, Semgrep, Shard Balancing |
| **Standards & Protocols** | RFC 4648 (Base64), PEP 508, ISO 8601, JSON-RPC 2.0, REST, Docker Sandboxing |

---

## 6. Public Verification Statement

- **GitHub Profile:** [`@Subodh-17`](https://github.com/Subodh-17)
- **Primary Contact:** `subodh171011@gmail.com`
- **Verification Statement:** Linked upstream pull requests and cited merge commits can be independently verified through their respective repositories.
