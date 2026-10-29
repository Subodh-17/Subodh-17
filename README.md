# Subodh Bansode

**Computer Science Student | Systems & ML Engineering**

I build systems software, machine learning tooling, and data-intensive applications. My recent work centers on query engines, ML inference runtimes, and geospatial pipeline engineering.

---

## Selected Projects

- **[Marine Pollution Intelligence](https://github.com/Subodh-17/Marine-Pollution-Intelligence-SIH)**
  End-to-end satellite oil-slick detection and vessel attribution platform developed for Smart India Hackathon 2026. Segments Sentinel-1 SAR imagery using Lee speckle filtering and adaptive Otsu thresholding, then correlates leeway drift hindcasting with historical AIS trajectories to generate vessel attribution scores.
  *Stack: Python, FastAPI, React, Leaflet, GeoTIFF, SAR Processing*

- **[Predictive Logistics](https://github.com/Subodh-17/Predictive_Logistics_SIH_26251)**
  Forward supply-chain forecasting and terrain-aware route optimization system for SIH Problem Statement 26251. Produces weather-adjusted statistical demand forecasts, scores delivery priority queues, and optimizes dispatch paths under elevation and weather penalties with simulated sensor inventory telemetry.
  *Stack: Python, FastAPI, PostgreSQL / PostGIS, SQLAlchemy, React, Vite, TypeScript, Docker*

- **[StockVision](https://github.com/Subodh-17/stockvision-scilab-gui)**
  Interactive numerical desktop studio built in Scilab for time-series forecasting, comparative model evaluation, and backtesting. Evaluates Linear Regression, Autoregressive (AR), and Holt exponential smoothing against naive baselines with expanding-window walk-forward validation and transaction cost modeling. *(Note: Dedicated Scilab GUI implementation, distinct from the Python prototype).*
  *Stack: Scilab (Numerics, Least Squares, GUI Engine, Plotting)*

- **[Blue Carbon MRV](https://github.com/Subodh-17/WCEHackathon2026_Proteas)**
  Measurement, Reporting, and Verification (MRV) platform for coastal blue carbon restoration projects. Provides field-worker mobile submission workflows and an administrative registry backend paired with an ERC-20 smart contract for audit-ready carbon credit issuance.
  *Stack: Solidity, Hardhat, Node.js, Express, PostgreSQL, JavaScript*

---

## Open-Source Contributions

A selection of upstream contributions focused on fixing runtime bugs, improving CI test suites, and resolving edge cases in production libraries.

### Merged Upstream

- **[huggingface/diffusers#9838](https://github.com/huggingface/diffusers/pull/9838)** — Fixed CogVideoX pipeline input validation for multi-view conditioning.
- **[ionfwsrijan/PatchPilot#350](https://github.com/ionfwsrijan/PatchPilot/pull/350)** — Implemented severity-based finding prioritization and deduplication ranking in the security analysis pipeline.
- **[ThreeMoonsLab/agents-shipgate#1007](https://github.com/ThreeMoonsLab/agents-shipgate/pull/1007)** — Resolved PEP 508 extras-qualified pin parsing failures during lockfile verification.
- **[batrapulkit/squidbrake#51](https://github.com/batrapulkit/squidbrake/pull/51)** — Established cross-platform GitHub Actions CI test matrices across Linux, Windows, macOS, and Python 3.13.
- **[knight22-21/CodePrism#72](https://github.com/knight22-21/CodePrism/pull/72)** — Added strict configuration schema validation to reject unmapped options and prevent silent fallbacks.
- **[corsairdev/corsair#1398](https://github.com/corsairdev/corsair/pull/1398)** — Integrated dynamic asset generation module into the TypeScript framework core.

### Active Work & RFCs (In Review)

- **[ionfwsrijan/PatchPilot#354](https://github.com/ionfwsrijan/PatchPilot/pull/354)** — Persists triaged finding status across page reloads (fixes [#319](https://github.com/ionfwsrijan/PatchPilot/issues/319)). All backend, frontend, coverage, and security CI gates passing; currently awaiting maintainer review.
- **[apache/datafusion#26465](https://github.com/apache/datafusion/pull/26465)** — Propagated CLI row counts in GCD function benchmarks. Approved by committer, 42/42 CI checks passing, in merge queue.
- **[huggingface/transformers#49712](https://github.com/huggingface/transformers/pull/49712)** — Corrected grouped RMSNorm reshape and weight broadcasting for Mamba2 on non-CUDA environments.
- **[safetensors/safetensors#873](https://github.com/safetensors/safetensors/pull/873)** — Added zero-length tensor slice handling in the Rust core to prevent panics.
- **[Lightning-AI/pytorch-lightning#22006](https://github.com/Lightning-AI/pytorch-lightning/pull/22006)** — Synchronized sampler epoch state before iterator creation for deterministic resumed training.

---

## Technical Toolkit

- **Languages:** Python, Rust, TypeScript, JavaScript, SQL (PostgreSQL), Scilab, Solidity
- **Backend & Data:** FastAPI, PostgreSQL / PostGIS, SQLAlchemy, Node.js, Express, Apache Arrow / DataFusion
- **Infrastructure & Tools:** Git, GitHub Actions (Multi-OS CI), Docker, Linux, Chrome DevTools Protocol (CDP), Model Context Protocol (MCP)
- **Machine Learning:** PyTorch, Hugging Face (	ransformers, diffusers, safetensors), PyTorch Lightning, Scikit-Learn, NumPy

---

## Recognition

- **[XERJ Corpus Hub Contributor](https://hub.xerj.org/contributors/Subodh-17)** — Recognized open-source contributor for dataset curation and corpus tooling.

---

## Contact & Links

- **GitHub:** [Subodh-17](https://github.com/Subodh-17)
- **Email:** [subodh171011@gmail.com](mailto:subodh171011@gmail.com)
- **Instagram:** [@subodh17_](https://www.instagram.com/subodh17_)
