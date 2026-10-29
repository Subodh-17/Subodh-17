# Subodh Bansode

**Computer Science Student | Systems & ML Engineering**

I build systems software, machine learning tooling, and data-intensive applications. My recent work centers on analytical query engines, ML inference runtimes, and distributed geospatial data pipelines.

<p align="left">
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python" />
  <img src="https://img.shields.io/badge/Rust-000000?style=flat-square&logo=rust&logoColor=white" alt="Rust" />
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript" />
  <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" alt="FastAPI" />
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" alt="PostgreSQL" />
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" alt="Docker" />
  <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white" alt="PyTorch" />
  <img src="https://img.shields.io/badge/Apache_Arrow-E25A22?style=flat-square&logo=apachearrow&logoColor=white" alt="Apache Arrow" />
  <img src="https://img.shields.io/badge/Solidity-363636?style=flat-square&logo=solidity&logoColor=white" alt="Solidity" />
  <img src="https://img.shields.io/badge/Scilab-002B49?style=flat-square&logo=scilab&logoColor=white" alt="Scilab" />
</p>

---

## Featured Projects

### [Marine Pollution Intelligence](https://github.com/Subodh-17/Marine-Pollution-Intelligence-SIH)
*Satellite oil-slick detection and vessel attribution platform (Smart India Hackathon 2026)*

> **Problem & Approach:** Automated detection of marine oil slicks from high-noise radar imagery, coupled with physical drift hindcasting to attribute spills to historical vessel transits.
>
> **Engineering Pipeline:**
> - **SAR Segmentation:** Ingests Sentinel-1 SAR imagery, applies adaptive Lee speckle filtering to suppress multiplicative radar noise, and segments candidate slicks via dynamic Otsu thresholding.
> - **Attribution Engine:** Simulates leeway drift hindcasting using wind and ocean surface current vectors, correlating modeled slick trajectories with historical AIS vessel corridors to score candidate vessels.
>
> *Stack: Python, FastAPI, React, Leaflet, GeoTIFF, SAR Processing*

### [Predictive Logistics](https://github.com/Subodh-17/Predictive_Logistics_SIH_26251)
*Forward supply-chain forecasting and route optimization platform (SIH Problem Statement 26251)*

> **Problem & Approach:** Decision-support platform resolving forward supply-chain bottlenecks and dispatch routing across rugged terrain under dynamic weather and elevation constraints.
>
> **Engineering Architecture:**
> - **Demand Forecasting:** Generates weather-adjusted statistical demand forecasts, managing multi-tier delivery priority queues based on urgency, shelf-life, and storage capacity.
> - **Geospatial Routing:** Leverages PostgreSQL/PostGIS to evaluate terrain elevation gradients and weather friction surfaces, producing cost-minimized, risk-scored dispatch itineraries.
>
> *Stack: Python, FastAPI, PostgreSQL / PostGIS, SQLAlchemy, React, TypeScript, Docker*

### [StockVision -- Scilab GUI](https://github.com/Subodh-17/stockvision-scilab-gui)
*Dedicated desktop numerical studio for time-series forecasting and quantitative backtesting*

> **Problem & Approach:** Native desktop quantitative studio in Scilab for model evaluation, comparing regression and smoothing models against naive baselines under transaction friction.
>
> **Engineering Implementation:**
> - **Comparative Modeling:** Evaluates Ordinary Least Squares (OLS) Linear Regression, Autoregressive (AR), and Holt exponential smoothing against random-walk baselines.
> - **Backtesting Engine:** Executes expanding-window walk-forward validation with realistic transaction cost modeling, slippage parameters, and performance diagnostics.
> - *(Note: Dedicated Scilab GUI implementation, engineered separately from the earlier Python prototype).*
>
> *Stack: Scilab (Numerics, Least Squares, GUI Engine, Plotting)*

### [Blue Carbon MRV](https://github.com/Subodh-17/WCEHackathon2026_Proteas)
*Measurement, Reporting, and Verification (MRV) platform for coastal blue carbon restoration*

> **Problem & Approach:** Hybrid on-chain/off-chain registry tracking ecological field measurements, ensuring verifiable record custody without offloading heavy telemetry on-chain.
>
> **Engineering Architecture:**
> - **Off-Chain Pipeline:** Mobile ecological field-data collection paired with a Node.js/Express and PostgreSQL backend for storing monitoring datasets and evidence documents.
> - **On-Chain Anchoring:** The `BlueCarbonRegistry.sol` Solidity smart contract anchors cryptographic hashes of monitoring records and records whole-tonne credit issuance (1 credit = 1 tCO2e) with strict role separation (verifier vs. admin issuer).
>
> *Stack: Solidity, Hardhat, Node.js, Express, PostgreSQL, JavaScript*

---

## Open-Source Contributions

A curated selection of upstream contributions focused on fixing runtime bugs, standardizing CI test matrices, and handling core edge cases.

### Merged Upstream

- ![Merged](https://img.shields.io/badge/Merged-8957e5?style=flat-square) **[apache/datafusion#26465](https://github.com/apache/datafusion/pull/26465)** -- Passed CLI row counts into GCD function benchmarks in the DataFusion query engine.
- ![Merged](https://img.shields.io/badge/Merged-8957e5?style=flat-square) **[ionfwsrijan/PatchPilot#350](https://github.com/ionfwsrijan/PatchPilot/pull/350)** -- Implemented normalized severity ranking and deduplication in the security finding pipeline.
- ![Merged](https://img.shields.io/badge/Merged-8957e5?style=flat-square) **[ThreeMoonsLab/agents-shipgate#1007](https://github.com/ThreeMoonsLab/agents-shipgate/pull/1007)** -- Fixed parsing of PEP 508 extras-qualified pins during lockfile verification.
- ![Merged](https://img.shields.io/badge/Merged-8957e5?style=flat-square) **[batrapulkit/squidbrake#51](https://github.com/batrapulkit/squidbrake/pull/51)** -- Established cross-platform GitHub Actions CI test matrices across Linux, Windows, macOS, and Python 3.13.
- ![Merged](https://img.shields.io/badge/Merged-8957e5?style=flat-square) **[knight22-21/CodePrism#72](https://github.com/knight22-21/CodePrism/pull/72)** -- Added strict configuration schema validation to reject unmapped settings and prevent silent fallbacks.
- ![Merged](https://img.shields.io/badge/Merged-8957e5?style=flat-square) **[corsairdev/corsair#1398](https://github.com/corsairdev/corsair/pull/1398)** -- Integrated dynamic image asset generation plugin into the TypeScript framework core.

### Active Work (In Review)

- ![In Review](https://img.shields.io/badge/In_Review-2da44e?style=flat-square) **[ionfwsrijan/PatchPilot#354](https://github.com/ionfwsrijan/PatchPilot/pull/354)** -- Persists triaged finding status across page reloads (fixes [#319](https://github.com/ionfwsrijan/PatchPilot/issues/319)). All backend, frontend, coverage, and security CI gates passing; awaiting maintainer review.
- ![In Review](https://img.shields.io/badge/In_Review-2da44e?style=flat-square) **[safetensors/safetensors#873](https://github.com/safetensors/safetensors/pull/873)** -- Adds zero-length tensor slice handling in the Rust core to prevent panics on empty slices.
- ![In Review](https://img.shields.io/badge/In_Review-2da44e?style=flat-square) **[Lightning-AI/pytorch-lightning#22006](https://github.com/Lightning-AI/pytorch-lightning/pull/22006)** -- Synchronizes sampler epoch state before iterator initialization for deterministic resumed training restarts.

[View full contribution history on GitHub →](https://github.com/Subodh-17?tab=overview)

---

## Technical Toolkit

| Category | Technologies & Tools |
| :--- | :--- |
| **Languages** | Python, Rust, TypeScript, JavaScript, SQL (PostgreSQL), Scilab, Solidity |
| **Systems & Data Engineering** | Apache Arrow / DataFusion, PostgreSQL / PostGIS, SQLAlchemy, FastAPI, Node.js, Express |
| **Machine Learning & Numerics** | PyTorch, Hugging Face (`transformers`, `diffusers`, `safetensors`), PyTorch Lightning, Scikit-Learn, NumPy |
| **Infrastructure & Protocols** | Git, GitHub Actions, Docker, Linux, Chrome DevTools Protocol (CDP), Model Context Protocol (MCP) |

---

## Recognition

- **[XERJ Corpus Hub Contributor](https://hub.xerj.org/contributors/Subodh-17)** -- Included in the XERJ Corpus Hub reference catalogue for open-source work in `mloda-ai/mloda`.

---

## Contact & Links

- **GitHub:** [Subodh-17](https://github.com/Subodh-17)
- **Email:** [subodh171011@gmail.com](mailto:subodh171011@gmail.com)
- **Instagram:** [@subodh17_](https://www.instagram.com/subodh17_)
