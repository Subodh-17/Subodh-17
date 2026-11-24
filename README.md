# Subodh

[![GitHub](https://img.shields.io/badge/GitHub-Subodh--17-0f172a?style=flat-square&logo=github&logoColor=white)](https://github.com/Subodh-17)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Subodh-0a66c2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/subodh-b-b705b5403)
[![Instagram](https://img.shields.io/badge/Instagram-subodh17__-e4405f?style=flat-square&logo=instagram&logoColor=white)](https://www.instagram.com/subodh17_?stkn=cnplbHl2dHA1a244)
[![Email](https://img.shields.io/badge/Email-subodh171011%40gmail.com-ea4335?style=flat-square&logo=gmail&logoColor=white)](mailto:subodh171011@gmail.com)

Systems and open-source engineer focused on columnar query processing, distributed ML training determinism, and AI agent runtime verification.

I spend most of my time writing query execution kernels in the Apache Arrow and DataFusion ecosystems, building spatial routing engines, and contributing fixes to open-source data infrastructure.

---

<!-- OSS_DASHBOARD:START -->
## Open-Source Contributions

A verified snapshot of contributions across core data systems, ML infrastructure, and developer ecosystems:

### Core Systems & ML Infrastructure (Claude OSS)
- **Merged Upstream (5 PRs):**
  - **Apache DataFusion:** [#26465](https://github.com/apache/datafusion/pull/26465) — Fix row-count propagation in scalar GCD Criterion benchmarks.
  - **Apache DataFusion-Spark:** [#116](https://github.com/apache/datafusion-spark/pull/116) — Spark 4 string charset encoding and runtime error alignment; [#118](https://github.com/apache/datafusion-spark/pull/118) — ANSI mode error enforcement in `next_day`; [#119](https://github.com/apache/datafusion-spark/pull/119) — Microsecond overflow prevention in `make_dt_interval`.
  - **Hugging Face Diffusers:** [#14961](https://github.com/huggingface/diffusers/pull/14961) — Multi-LoRA active adapter state leakage fix across secondary text encoders.
- **Open / Under Active Review (18 PRs):**
  - **Apache DataFusion-Spark:** [#390](https://github.com/apache/datafusion-spark/pull/390) [Pending Review] — Port overflow handling and error normalization in `parse_url`; [#401](https://github.com/apache/datafusion-spark/pull/401) [Pending Review] — Untyped null rejection and type coercion in `array_contains`; [#402](https://github.com/apache/datafusion-spark/pull/402) [Pending Review] — Null-typed column rejection and Spark-aligned null coercion in `stack`.
  - **Apache DataFusion:** [#27643](https://github.com/apache/datafusion/pull/27643) [Pending Review] — Cumulative `Utf8` array offset capacity check in `repeat`; [#27561](https://github.com/apache/datafusion/pull/27561) [Pending Review] — Partition column min/max statistics handling on empty files.
  - **Apache Arrow (Rust):** [#12389](https://github.com/apache/arrow-rs/pull/12389) [Pending Review] — Decimal safe-cast overflow handling under extreme scale increases; [#12315](https://github.com/apache/arrow-rs/pull/12315) [Pending Roll-up] — Bound gzip and brotli decompression in Parquet; [#12135](https://github.com/apache/arrow-rs/pull/12135) [Pending Review] — Strict duplicate key rejection in Parquet Variant parsing.
  - **SafeTensors:** [#927](https://github.com/safetensors/safetensors/pull/927) [Pending Review] — Disjoint interleaved shared tensor views in PyTorch serialization.
  - **PyTorch Lightning:** [#22017](https://github.com/Lightning-AI/pytorch-lightning/pull/22017) [Pending Review] — Strategy namespace diagnostic error messages; [#22006](https://github.com/Lightning-AI/pytorch-lightning/pull/22006) [Pending Review] — Resumed DataLoader sampler epoch sequencing.
  - **Hugging Face Diffusers:** [#14990](https://github.com/huggingface/diffusers/pull/14990), [#14984](https://github.com/huggingface/diffusers/pull/14984), [#14983](https://github.com/huggingface/diffusers/pull/14983), [#14982](https://github.com/huggingface/diffusers/pull/14982), [#14971](https://github.com/huggingface/diffusers/pull/14971), [#14963](https://github.com/huggingface/diffusers/pull/14963) [Pending Review] — Model loading, LoRA weighting, torch.compile support, and scheduler validation.
  - **ModelScope Swift:** [#10289](https://github.com/modelscope/ms-swift/pull/10289) [Pending Review] — CLI help command handler.
- **Formal Code Reviews Submitted (15 PRs):**
  - Peer code reviews on pull requests across Apache DataFusion (including merged [#27501](https://github.com/apache/datafusion/pull/27501)), Apache Arrow-rs (including merged [#12293](https://github.com/apache/arrow-rs/pull/12293)), SafeTensors (approved [#900](https://github.com/safetensors/safetensors/pull/900)), PyTorch Lightning, and MLflow.
- **Authored Issues & RFCs (3):**
  - **RFC:** [apache/datafusion#26425](https://github.com/apache/datafusion/issues/26425) — WindowAggExec streaming execution plan design.
  - **Issues:** [mlflow/mlflow#27862](https://github.com/mlflow/mlflow/issues/27862) — SQL escaped apostrophe handling in search filters; [apache/arrow-rs#12200](https://github.com/apache/arrow-rs/issues/12200) — ByteViewArrayDecoder Plain 32-bit wrap handling (resolved).

### Program & Mentored Open Source (NSoC / Hackathons)
- **Merged (29 PRs):** Mentored program contributions across DevTrack ([VarshithReddy2006/DevTrack](https://github.com/VarshithReddy2006/DevTrack) — 18 PRs merged: Redis stream sharding, saga cohort rollover, MongoDB change stream search indexing), ReconGrid-AI ([AkshayHaldar/ReconGrid-AI](https://github.com/AkshayHaldar/ReconGrid-AI) — 2 PRs merged: CSV column mapper, bank statement parsers), AgentWatch, and community event repositories.
<!-- OSS_DASHBOARD:END -->

---

## Technologies

**Systems & Query Engines**  
[![Rust](https://img.shields.io/badge/Rust-000000?style=flat-square&logo=rust&logoColor=white)](https://www.rust-lang.org/)
[![Apache Arrow](https://img.shields.io/badge/Apache%20Arrow-E23337?style=flat-square&logo=apachearrow&logoColor=white)](https://arrow.apache.org/)
[![Apache DataFusion](https://img.shields.io/badge/Apache%20DataFusion-D22128?style=flat-square&logo=apache&logoColor=white)](https://datafusion.apache.org/)
[![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)](https://www.python.org/)

**Backend & Infrastructure**  
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)](https://www.postgresql.org/)
[![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com/)
[![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)](https://www.docker.com/)
[![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)](https://git-scm.com/)

**ML & Specialized Technologies**  
[![ONNX Runtime](https://img.shields.io/badge/ONNX%20Runtime-005CED?style=flat-square&logo=onnx&logoColor=white)](https://onnxruntime.ai/)
[![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB)](https://react.dev/)
[![Solidity](https://img.shields.io/badge/Solidity-363636?style=flat-square&logo=solidity&logoColor=white)](https://soliditylang.org/)
[![IPFS](https://img.shields.io/badge/IPFS-65C2CB?style=flat-square&logo=ipfs&logoColor=white)](https://ipfs.tech/)
[![Scilab](https://img.shields.io/badge/Scilab-002B49?style=flat-square&logo=scilab&logoColor=white)](https://www.scilab.org/)

---

## Selected Projects

### Apache Arrow & DataFusion
*Columnar query execution, arithmetic kernels, and engine compatibility across the Apache ecosystem.*

[![Rust](https://img.shields.io/badge/Rust-000000?style=flat-square&logo=rust&logoColor=white)](https://www.rust-lang.org/)
[![Apache Arrow](https://img.shields.io/badge/Apache%20Arrow-E23337?style=flat-square&logo=apachearrow&logoColor=white)](https://arrow.apache.org/)
[![Apache DataFusion](https://img.shields.io/badge/Apache%20DataFusion-D22128?style=flat-square&logo=apache&logoColor=white)](https://datafusion.apache.org/)

- **[Apache DataFusion](https://github.com/apache/datafusion):** Merged fix for benchmark row-count propagation in scalar GCD Criterion benchmarks ([#26465](https://github.com/apache/datafusion/pull/26465)); submitted cumulative `Utf8` array offset overflow protection in `repeat` ([#27643](https://github.com/apache/datafusion/pull/27643), pending review) and partition metadata handling fixes ([#27561](https://github.com/apache/datafusion/pull/27561), pending review).
- **[DataFusion-Spark](https://github.com/apache/datafusion-spark):** Merged compatibility fixes matching Spark 4 string charset encoding ([#116](https://github.com/apache/datafusion-spark/pull/116)) and datetime interval overflow handling ([#118](https://github.com/apache/datafusion-spark/pull/118), [#119](https://github.com/apache/datafusion-spark/pull/119)); submitted port overflow validation in `parse_url` ([#390](https://github.com/apache/datafusion-spark/pull/390), pending review), untyped null rejection in `array_contains` ([#401](https://github.com/apache/datafusion-spark/pull/401), pending review), and null-typed column handling in `stack` ([#402](https://github.com/apache/datafusion-spark/pull/402), pending review).
- **[Apache Arrow (Rust)](https://github.com/apache/arrow-rs):** Submitted decimal safe-cast overflow handling under extreme scale expansion in `arrow-cast` ([#12389](https://github.com/apache/arrow-rs/pull/12389), pending review), bounded decompression in Parquet ([#12315](https://github.com/apache/arrow-rs/pull/12315), pending roll-up), and strict duplicate key rejection in Parquet Variant parsing ([#12135](https://github.com/apache/arrow-rs/pull/12135), pending review).

### [Marine Pollution Intelligence](https://github.com/Subodh-17/marine-pollution-intelligence)
*Autonomous satellite radar (SAR) oil spill segmentation and hydrodynamic drift hindcasting platform.*

[![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)](https://www.python.org/)
[![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com/)
[![ONNX Runtime](https://img.shields.io/badge/ONNX%20Runtime-005CED?style=flat-square&logo=onnx&logoColor=white)](https://onnxruntime.ai/)
[![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB)](https://react.dev/)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)](https://www.postgresql.org/)

- Ingestion pipeline for Copernicus Sentinel-1 SAR radar imagery, applying 7x7 Lee speckle filtering and adaptive local Gaussian thresholding to isolate oil slicks from sea clutter.
- Dual lightweight ONNX Runtime CPU models (`SpillUNet` and `SceneClassifier`, ~105 KB total payload) for zero-GPU edge inference.
- 2D Euler hydrodynamic drift model simulating slick advection and dispersion driven by surface wind shear and ocean current vectors (Open-Meteo CMEMS/MET Norway).
- Full-stack geospatial architecture combining FastAPI, React, Leaflet GIS, and SQLite/PostgreSQL caching.

### [Indian Army Predictive Logistics](https://github.com/Subodh-17/Predictive_Logistics_SIH_26251)
*Terrain- and weather-aware dynamic multi-modal freight routing engine and forward supply chain decision support.*

[![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)](https://www.python.org/)
[![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com/)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)](https://www.postgresql.org/)
[![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB)](https://react.dev/)
[![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)](https://www.docker.com/)

- Dynamic multi-modal graph routing engine (A* search) factoring in Digital Elevation Model (DEM) slope penalties and physical speed floors across difficult terrain.
- 7-factor dispatch priority queue balancing cargo perishability, medical criticality, contract SLAs, transport cost, and route reliability.
- PostgreSQL and PostGIS spatial queries (`ST_DWithin`, `ST_LineInterpolatePoint`) for real-time waypoint tracking, backed by a 280-test regression suite.

### [StockVision V3 & Quantitative Forecasting](https://github.com/Subodh-17/stockvision-scilab-gui)
*Quantitative time-series forecasting terminal and backtester built in native Scilab with companion Python models.*

[![Scilab](https://img.shields.io/badge/Scilab-002B49?style=flat-square&logo=scilab&logoColor=white)](https://www.scilab.org/)
[![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)](https://www.python.org/)

- Pure Scilab numerical engine implementing Ordinary Least Squares (OLS) polynomial trend fitting with exact 95% prediction intervals, Autoregressive AR(p) modeling, and Holt double exponential smoothing.
- Chronological multi-fold walk-forward validation across market regimes evaluated against naive persistence baselines.
- Companion work in Python ([`stock_prediction_python`](https://github.com/Subodh-17/stock_prediction_python)) evaluates LSTM sequence architectures alongside statistical baselines.

### [Blueledger](https://github.com/Subodh-17/Blueledger)
*Decentralized measurement, reporting, and verification (MRV) registry for blue carbon restoration credits.*

[![Solidity](https://img.shields.io/badge/Solidity-363636?style=flat-square&logo=solidity&logoColor=white)](https://soliditylang.org/)
[![IPFS](https://img.shields.io/badge/IPFS-65C2CB?style=flat-square&logo=ipfs&logoColor=white)](https://ipfs.tech/)

- Solidity 0.8.20 smart contracts enforcing cryptographic verification role separation so field verifiers cannot issue credits for their own assessments.
- Immutable, content-addressed storage integration via IPFS (Kubo RPC & Pinata) for remote-sensing evidence and field survey proofs.

---

## Connect

- **GitHub:** [@Subodh-17](https://github.com/Subodh-17)
- **LinkedIn:** [Subodh](https://www.linkedin.com/in/subodh-b-b705b5403)
- **Instagram:** [@subodh17_](https://www.instagram.com/subodh17_?stkn=cnplbHl2dHA1a244)
- **Email:** [subodh171011@gmail.com](mailto:subodh171011@gmail.com)
