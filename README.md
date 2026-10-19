<div align="center">

# Subodh Bansode
### Open-Source Systems & ML Infrastructure Engineer

**Systems and machine learning engineer focused on analytical query engines, ML inference runtimes, browser protocols, and geospatial intelligence.**

<br>

<a href="https://github.com/Subodh-17">
  <img src="https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white" alt="GitHub Profile" />
</a>
&nbsp;
<a href="mailto:subodh171011@gmail.com">
  <img src="https://img.shields.io/badge/Email-D14836?style=flat-square&logo=gmail&logoColor=white" alt="Email Contact" />
</a>
&nbsp;
<a href="https://www.instagram.com/subodh17_">
  <img src="https://img.shields.io/badge/Instagram-E4405F?style=flat-square&logo=instagram&logoColor=white" alt="Instagram Profile" />
</a>

</div>

<br>

---

## Technical Summary

Engineering focus centered on analytical query execution, compiler and runtime stability, and production data infrastructure. Upstream open-source contributor across foundational ecosystems, with active work in **Apache DataFusion** (Rust query engine), **SafeTensors**, and **PyTorch Lightning**, alongside merged contributions to **Hugging Face** (`diffusers`). Committed to evidence-backed engineering: isolating defects, writing deterministic regression tests, and collaborating with upstream maintainers through code review.

---

## Technical Skills

- **Languages:** Rust, Python, TypeScript, JavaScript, SQL (PostgreSQL / PLpgSQL), Scilab
- **Machine Learning & Systems:** PyTorch, Hugging Face (`diffusers`), SafeTensors, PyTorch Lightning, Scikit-Learn, NumPy, SciPy
- **Query Engines & Data Systems:** Apache DataFusion, Apache Arrow, PostgreSQL / PostGIS, SQLAlchemy, FastAPI
- **Developer Infrastructure & Protocols:** Git, GitHub Actions (Multi-OS CI Matrices), Docker & Docker Compose, Chrome DevTools Protocol (CDP), Model Context Protocol (MCP), Linux
- **Web & Geospatial:** React, Vite, Leaflet, GeoTIFF Radar Processing

---

## Open-Source Engineering & Upstream Contributions

### Merged Upstream Contributions (8 PRs across 6 Ecosystems)

- **[huggingface/diffusers#14961](https://github.com/huggingface/diffusers/pull/14961)** — Corrected active PEFT LoRA adapter tracking across text encoders during multi-adapter inference pipelines. *(Approved by PEFT maintainer `@BenjaminBossan` and reviewed by Diffusers lead `@sayakpaul`)*
- **[existence-master/Sentient#295](https://github.com/existence-master/Sentient/pull/295)** — Implemented target-scoped CDP download isolation to preserve user browser download integrity during automation sessions. *(Tested and approved by maintainer `@itsskofficial`)*
- **[existence-master/Sentient#326](https://github.com/existence-master/Sentient/pull/326)** — Isolated Model Context Protocol (MCP) OAuth credentials by server URL to prevent cross-server credential collisions and leakage. *(Tested and approved by maintainer `@itsskofficial`)*
- **[ThreeMoonsLab/agents-shipgate#1007](https://github.com/ThreeMoonsLab/agents-shipgate/pull/1007)** — Resolved PEP 508 extras-qualified pin parsing failures during deterministic dependency lockfile verification. *(Approved by `@pengfei-threemoonslab`)*
- **[knight22-21/CodePrism#72](https://github.com/knight22-21/CodePrism/pull/72)** — Enforced strict schema validation to reject unknown configuration keys and prevent silent runtime fallbacks. *(Approved by `@knight22-21`)*
- **[knight22-21/CodePrism#70](https://github.com/knight22-21/CodePrism/pull/70)** — Corrected complex PEP 440 version specifier parsing for dependency constraint boundaries. *(Approved by `@knight22-21`)*
- **[batrapulkit/squidbrake#51](https://github.com/batrapulkit/squidbrake/pull/51)** — Established cross-platform GitHub Actions CI test matrices across Linux, Windows, macOS, and Python 3.13.
- **[corsairdev/corsair#1398](https://github.com/corsairdev/corsair/pull/1398)** — Integrated Dynapictures dynamic image generation plugin into the Corsair TypeScript framework. *(Approved by `@devjain32`, `@Dhirenderchoudhary`)*

*(Note on Closed Contributions: PR [mloda-ai/mloda#1938](https://github.com/mloda-ai/mloda/pull/1938) was closed unmerged on GitHub, with the concurrent join race condition fix reportedly incorporated into a larger merged PR on Oct 11, 2026, per maintainer `@TomKaltofen`)*

---

### Active Upstream Contributions & Research RFCs (In Review / Prototype)

- **[apache/datafusion#26465](https://github.com/apache/datafusion/pull/26465)** — `fix(functions): pass correct number_rows in gcd benchmarks`. Propagated CLI row count argument through benchmark execution harness. *(**Approved** by DataFusion committer `@kumarUjjawal`, 28 checks passed; 2 checks were skipped, awaiting committer merge; not yet merged)*
- **[apache/datafusion#26376](https://github.com/apache/datafusion/pull/26376)** — `fix(expr): differentiate aggregate functions with and without explicit cast in output schema (#26221)`. Resolved schema name collisions across 33 files with full sqllogictest suite. *(In review; not yet merged)*
- **[apache/datafusion Discussions #26425](https://github.com/apache/datafusion/discussions/26425)** — `[RFC] Partition-at-a-Time Streaming Evaluation in WindowAggExec`. Architecture and working prototype evaluating sorted partitions sequentially when `PARTITION BY` ordering matches input stream order (falling back to standard batch accumulation otherwise; retains parent Arrow buffers across partition slice boundaries). Prototype tracks memory via `MemoryPool` and passes 2,578 `datafusion-physical-plan` crate unit tests; broader SQL integration and workspace verification remain outstanding.
- **[safetensors/safetensors#873](https://github.com/safetensors/safetensors/pull/873)** — `fix: allow slicing zero-length dimensions`. Supported zero-length slice operations in Rust tensor core without panics. *(In review; not yet merged)*
- **[Lightning-AI/pytorch-lightning#22006](https://github.com/Lightning-AI/pytorch-lightning/pull/22006)** — `fix: set sampler epoch before creating resumed iterator`. Synchronized sampler epoch state prior to iterator initialization for deterministic distributed training restarts. *(In review; not yet merged)*
- **[Lightning-AI/pytorch-lightning#22017](https://github.com/Lightning-AI/pytorch-lightning/pull/22017)** — `Improve error message for mixed strategy namespaces`. Validated distributed strategy configuration combinations and error diagnostics. *(In review; not yet merged)*

---

## Featured Engineering Projects

### [Marine Pollution Intelligence](https://github.com/Subodh-17/Marine-Pollution-Intelligence-SIH)
*End-to-end Sentinel-1 SAR satellite oil spill detection and vessel attribution platform (Smart India Hackathon 2026).*
- Ingests real and synthetic Sentinel-1 SAR Level-1 GRD imagery, applies Lee speckle filtering and adaptive Otsu thresholding for oil slick candidate segmentation.
- Simulates oceanographic leeway drift hindcasting and correlates spatial vectors against historical AIS vessel trajectories to generate explainable candidate vessel attribution scores.
- **Stack:** Python, FastAPI, React, Leaflet, GeoTIFF Radar Ingestion, Lee Speckle Filter, Drift Hindcast Modeling, AIS Trajectory Correlation.

### [Predictive Logistics](https://github.com/Subodh-17/Predictive_Logistics_SIH_26251)
*Forward supply chain forecasting and terrain-aware route optimization platform (SIH 2026 Problem Statement 26251).*
- Generates weather-aware statistical demand forecasts (7/14/30-day horizons) with Random Forest cross-validation, shortage classification, and priority queue dispatch scoring.
- Optimizes vehicle dispatch routes under terrain penalties and road weather hazards; integrates simulated ESP32/RFID sensor inventory telemetry.
- **Stack:** Python, FastAPI, PostgreSQL / PostGIS, SQLAlchemy, React, Vite, TypeScript, Docker Compose, Leaflet.

### [StockVision](https://github.com/Subodh-17/stockvision-scilab-gui)
*Interactive numerical desktop studio for time-series forecasting, comparative evaluation, and backtesting.*
- Evaluates Linear Regression, Autoregressive (AR), and Holt exponential smoothing against naive last-value baselines on synchronized chronological test windows.
- Executes expanding-window walk-forward validation and backtests long-only trading signals under explicit transaction costs, slippage, and execution lag.
- **Stack:** Scilab (Core Numerics, Least Squares Solver, Embedded GUI Controls, Plotting).

---

## Current Technical Interests

- **Analytical Query Engines (Rust):** Vectorized execution kernels, partition-at-a-time streaming operators, and schema inference in Apache DataFusion & Arrow.
- **ML Runtime Systems & Attention:** Memory-efficient attention mechanisms, KV cache lifecycle management, and zero-copy tensor serialization (`safetensors`).
- **Geospatial & Spatial Systems:** High-throughput spatial indexing, PostGIS partitioning strategies, and satellite SAR radar processing pipelines.

---

<div align="center">

[GitHub](https://github.com/Subodh-17) &nbsp;&bull;&nbsp; [Email](mailto:subodh171011@gmail.com) &nbsp;&bull;&nbsp; [Instagram](https://www.instagram.com/subodh17_)

</div>
