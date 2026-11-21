# Subodh

[![GitHub](https://img.shields.io/badge/GitHub-Subodh--17-0f172a?style=flat-square&logo=github&logoColor=white)](https://github.com/Subodh-17)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Subodh-0a66c2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/subodh-b-b705b5403)
[![Instagram](https://img.shields.io/badge/Instagram-subodh17__-e4405f?style=flat-square&logo=instagram&logoColor=white)](https://www.instagram.com/subodh17_?stkn=cnplbHl2dHA1a244)
[![Email](https://img.shields.io/badge/Email-subodh171011%40gmail.com-ea4335?style=flat-square&logo=gmail&logoColor=white)](mailto:subodh171011@gmail.com)

Systems and open-source engineer focused on columnar query processing, distributed ML training determinism, and AI agent runtime verification.

I spend most of my time writing query execution kernels in the Apache Arrow and DataFusion ecosystems, building spatial routing engines, and contributing fixes to open-source data infrastructure.

---

<!-- OSS_DASHBOARD:START -->
## Open-Source Activity

[![Merged Upstream](https://img.shields.io/badge/Merged_Upstream-34_PRs-10b981?style=flat-square&logo=git&logoColor=white)](https://github.com/Subodh-17)
[![Open Upstream](https://img.shields.io/badge/Open_Upstream-21_PRs-2563eb?style=flat-square&logo=git&logoColor=white)](https://github.com/Subodh-17)
[![Repositories Contributed](https://img.shields.io/badge/Repositories_Contributed-12+-8b5cf6?style=flat-square&logo=github&logoColor=white)](https://github.com/Subodh-17)

A live snapshot of contributions across data systems, ML infrastructure, and runtime verification:

- **Merged Upstream (34 PRs):** Merged code in Apache DataFusion, DataFusion-Spark, Hugging Face Diffusers, DevTrack, AgentWatch, and the NSoC ecosystem.
- **Open Upstream (21 PRs):** Active PRs under review across Apache Arrow-rs, Apache DataFusion, PyTorch Lightning, SafeTensors, and Diffusers.
- **Repositories Contributed (12+):** Contributions spanning the Apache Software Foundation, Hugging Face, PyTorch / Lightning AI, and AI agent platforms.
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

- **[Apache DataFusion](https://github.com/apache/datafusion):** Merged fix for benchmark row-count propagation in scalar GCD Criterion benchmarks ([#26465](https://github.com/apache/datafusion/pull/26465)); submitted cumulative `Utf8` array offset overflow protection in `repeat` ([#27643](https://github.com/apache/datafusion/pull/27643)) and partition metadata handling fixes ([#27561](https://github.com/apache/datafusion/pull/27561)).
- **[DataFusion-Spark](https://github.com/apache/datafusion-spark):** Merged compatibility fixes matching Spark 4 string charset encoding ([#116](https://github.com/apache/datafusion-spark/pull/116)), datetime interval overflow handling ([#118](https://github.com/apache/datafusion-spark/pull/118), [#119](https://github.com/apache/datafusion-spark/pull/119)), and active port overflow validation in `parse_url` ([#390](https://github.com/apache/datafusion-spark/pull/390)).
- **[Apache Arrow (Rust)](https://github.com/apache/arrow-rs):** Submitted decimal safe-cast overflow handling under extreme scale expansion in `arrow-cast` ([#12389](https://github.com/apache/arrow-rs/pull/12389)) and strict duplicate key rejection in Parquet Variant parsing ([#12135](https://github.com/apache/arrow-rs/pull/12135)).

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
