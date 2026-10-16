<div align="center">

# Subodh Bansode
### Open Source Contributor & AI/ML Engineer

**AI/ML and open-source contributor focused on predictive modeling, geospatial intelligence, backend systems, and data-intensive applications.**

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

## Technical Introduction

Building reliable machine learning pipelines, geospatial decision-support architectures, and database-backed services. Focused on model evaluation, reproducible ML workflows, and improving production software through upstream open-source contributions to foundational ecosystems (Hugging Face, PyTorch Lightning, Apache DataFusion).

---

## Technical Stack

#### Languages
<a href="https://skillicons.dev">
  <img src="https://skillicons.dev/icons?i=python,rust,ts,js,solidity" alt="Python, Rust, TypeScript, JavaScript, Solidity" />
</a>

*Python, Rust, TypeScript, JavaScript, SQL, Solidity, Scilab*

#### Machine Learning & Data Science
<a href="https://skillicons.dev">
  <img src="https://skillicons.dev/icons?i=pytorch,tensorflow,sklearn" alt="PyTorch, TensorFlow, Scikit-Learn" />
</a>

*PyTorch, Hugging Face (Diffusers, Transformers, SafeTensors), PyTorch Lightning, Scikit-Learn, TensorFlow, NumPy, SciPy, Pandas*

#### Backend & Data Infrastructure
<a href="https://skillicons.dev">
  <img src="https://skillicons.dev/icons?i=fastapi,postgres,nodejs,express" alt="FastAPI, PostgreSQL, Node.js, Express" />
</a>

*FastAPI, PostgreSQL / PostGIS, SQLAlchemy, Node.js, Express, REST APIs*

#### Developer Infrastructure & CI/CD
<a href="https://skillicons.dev">
  <img src="https://skillicons.dev/icons?i=git,githubactions,docker,linux" alt="Git, GitHub Actions, Docker, Linux" />
</a>

*Git, GitHub Actions (Multi-OS CI Matrices), Docker & Docker Compose, Linux*

#### Frontend & Interfaces
<a href="https://skillicons.dev">
  <img src="https://skillicons.dev/icons?i=react,vite,html,css" alt="React, Vite, HTML5, CSS3" />
</a>

*React, Vite, Leaflet / React-Leaflet, GeoTIFF Ingestion, HTML5, CSS3*

---

## Featured Engineering Projects

### [Marine Pollution Intelligence](https://github.com/Subodh-17/Marine-Pollution-Intelligence-SIH)
*End-to-end Sentinel-1 SAR oil spill detection and vessel attribution decision-support prototype.*
- Ingests synthetic and real Sentinel-1 SAR GeoTIFF imagery, applies Lee speckle filtering, extracts geometric dark-spot characterizations, and simulates oceanographic leeway drift hindcasting.
- Correlates historical AIS vessel trajectories within the spatio-temporal drift window to generate explainable candidate vessel attribution scores.
- **Stack:** Python, FastAPI, React, Leaflet, GeoTIFF Processing, Lee Speckle Filter, Drift Hindcast Modeling, AIS Trajectory Correlation.

### [Predictive Logistics](https://github.com/Subodh-17/Predictive_Logistics_SIH_26251)
*Decision-support simulation platform for forward supply chain forecasting and route optimization.*
- Generates weather-aware statistical demand forecasts (7/14/30-day horizons) with Random Forest cross-validation, shortage classification, and multi-criteria priority queue scoring.
- Optimizes delivery routes under terrain penalties and road weather constraints while ingesting simulated ESP32/RFID sensor inventory telemetry.
- **Stack:** Python, FastAPI, PostgreSQL / PostGIS, SQLAlchemy, React, Vite, TypeScript, Docker Compose, Leaflet.

### [StockVision](https://github.com/Subodh-17/stockvision-scilab-gui)
*Interactive desktop studio for time-series forecasting, comparative evaluation, and backtesting.*
- Compares Linear Regression, Autoregressive (AR), and Holt exponential smoothing against a naive last-value baseline on a synchronized chronological test window.
- Executes expanding-window walk-forward validation and backtests long-only trading signals under explicit transaction costs, slippage, and execution lag.
- **Stack:** Scilab (Core Numerics, Least Squares Solver, Embedded GUI Controls, Plotting).

### [Blue Carbon MRV](https://github.com/Subodh-17/WCEHackathon2026_Proteas)
*Hackathon prototype for coastal blue carbon restoration monitoring, reporting, and verification.*
- Provides web and mobile interfaces for ecological field data submission, coupled with a Node.js/PostgreSQL backend for project registry management.
- Implements an ERC-20 carbon credit smart contract on Hardhat/Solidity to enforce transparent, audit-ready credit issuance and transfers.
- **Stack:** Solidity, Hardhat, Node.js, Express, PostgreSQL, JavaScript, HTML5/CSS3.

---

## Open Source Contributions

A commitment to practical systems engineering through reproducible bug isolation, root-cause analysis, and upstream fixes:

### Merged Upstream Contributions

- **[huggingface/diffusers#14961](https://github.com/huggingface/diffusers/pull/14961)** — Corrected active PEFT LoRA adapter tracking across text encoders during multi-adapter inference pipelines.
- **[existence-master/Sentient#295](https://github.com/existence-master/Sentient/pull/295)** — Implemented session isolation to preserve user download behavior during attached Chrome DevTools Protocol (CDP) browser automation.
- **[existence-master/Sentient#326](https://github.com/existence-master/Sentient/pull/326)** — Segregated Model Context Protocol (MCP) OAuth credentials by server URL to prevent cross-server credential leakage.
- **[ThreeMoonsLab/agents-shipgate#1007](https://github.com/ThreeMoonsLab/agents-shipgate/pull/1007)** — Resolved PEP 508 extras-qualified pin parsing failures during deterministic dependency lock verification.
- **[knight22-21/CodePrism#72](https://github.com/knight22-21/CodePrism/pull/72)** — Enforced strict schema validation to reject unknown configuration keys and avoid silent fallbacks.
- **[knight22-21/CodePrism#70](https://github.com/knight22-21/CodePrism/pull/70)** — Fixed PEP 440 version specifier parsing for complex constraint boundaries.
- **[batrapulkit/squidbrake#51](https://github.com/batrapulkit/squidbrake/pull/51)** — Established cross-platform GitHub Actions CI test matrices across Linux, Windows, macOS, and Python 3.13.
- **[corsairdev/corsair#1398](https://github.com/corsairdev/corsair/pull/1398)** — Integrated dynamic image generation capabilities into the Corsair TypeScript plugin framework.

### Active Upstream Work & Proposals (In Review)

- **[apache/datafusion#26376](https://github.com/apache/datafusion/pull/26376)** — Differentiated aggregate function output schemas with and without explicit cast in Rust logical plan consumer.
- **[safetensors/safetensors#873](https://github.com/safetensors/safetensors/pull/873)** — Added support for slicing zero-length dimensions without panicking in Rust tensor core and Python bindings.
- **[Lightning-AI/pytorch-lightning#22006](https://github.com/Lightning-AI/pytorch-lightning/pull/22006)** — Ensured sampler epoch is set prior to creating resumed iterators for deterministic distributed training restarts.
- **[Lightning-AI/pytorch-lightning#22017](https://github.com/Lightning-AI/pytorch-lightning/pull/22017)** — Improved error diagnostics and namespace validation when mixing conflicting distributed strategy configurations.
- **[huggingface/transformers#49192](https://github.com/huggingface/transformers/pull/49192)** — Fixed `AutoTokenizer` backend resolution logic for CohereLabs tiny-aya checkpoints.
- **[huggingface/diffusers#14971](https://github.com/huggingface/diffusers/pull/14971)** — Resolved offline loading failures for sharded model checkpoints in diffusion pipelines.

### Contribution Methodology

```text
  Isolate & Reproduce
          |
          v
 Minimal, Defensive Patch
          |
          v
 Comprehensive Regression Tests
          |
          v
 Multi-Platform CI & Upstream Review
```

---

## Current Technical Interests

- **Query Engines & Analytical Systems:** Vectorized execution kernels, query plan optimization, and schema inference in Rust (Apache DataFusion, Arrow).
- **ML Inference & Runtime Systems:** Memory-efficient attention mechanisms, KV cache lifecycle management, and zero-copy tensor serialization (`safetensors`).
- **Spatial Computing & Geospatial Data:** High-throughput spatial indexing, PostGIS partitioning strategies, and satellite SAR radar processing pipelines.

---

<div align="center">

[GitHub](https://github.com/Subodh-17) &nbsp;&bull;&nbsp; [Email](mailto:subodh171011@gmail.com) &nbsp;&bull;&nbsp; [Instagram](https://www.instagram.com/subodh17_)

</div>
