# Subodh

[![GitHub](https://img.shields.io/badge/GitHub-Subodh--17-0f172a?style=flat-square&logo=github&logoColor=white)](https://github.com/Subodh-17)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Subodh-0a66c2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/subodh-b-b705b5403)
[![Instagram](https://img.shields.io/badge/Instagram-subodh17__-e4405f?style=flat-square&logo=instagram&logoColor=white)](https://www.instagram.com/subodh17_?stkn=cnplbHl2dHA1a244)
[![Email](https://img.shields.io/badge/Email-subodh171011%40gmail.com-ea4335?style=flat-square&logo=gmail&logoColor=white)](mailto:subodh171011@gmail.com)

Software engineer focused on systems programming in Rust, columnar query processing, and backend data infrastructure.

I spend most of my time working on query execution kernels, spatial routing engines, and contributing fixes to open-source systems in the Apache Arrow and DataFusion ecosystems.

---

## Tech Stack

**Systems & Languages**  
[![Rust](https://img.shields.io/badge/Rust-000000?style=flat-square&logo=rust&logoColor=white)](https://www.rust-lang.org/)
[![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)](https://www.python.org/)
[![Apache Arrow](https://img.shields.io/badge/Apache%20Arrow-E23337?style=flat-square&logo=apachearrow&logoColor=white)](https://arrow.apache.org/)
[![Apache DataFusion](https://img.shields.io/badge/Apache%20DataFusion-D22128?style=flat-square&logo=apache&logoColor=white)](https://datafusion.apache.org/)

**Data & Infrastructure**  
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)](https://www.postgresql.org/)
[![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com/)
[![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)](https://www.docker.com/)
[![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)](https://git-scm.com/)

**Domain & Specialized**  
[![ONNX Runtime](https://img.shields.io/badge/ONNX%20Runtime-005CED?style=flat-square&logo=onnx&logoColor=white)](https://onnxruntime.ai/)
[![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB)](https://react.dev/)
[![Solidity](https://img.shields.io/badge/Solidity-363636?style=flat-square&logo=solidity&logoColor=white)](https://soliditylang.org/)
[![IPFS](https://img.shields.io/badge/IPFS-65C2CB?style=flat-square&logo=ipfs&logoColor=white)](https://ipfs.tech/)
[![Scilab](https://img.shields.io/badge/Scilab-002B49?style=flat-square&logo=scilab&logoColor=white)](https://www.scilab.org/)

**Core Focus Areas:** Vectorized query execution, zero-copy deserialization, geospatial routing, and deterministic runtime verification.

---

## Projects & Open-Source Work

### Apache Arrow & DataFusion Contributions
*Open-source query execution, columnar arithmetic, and kernel contributions across the Apache ecosystem.*
- **[Apache DataFusion](https://github.com/apache/datafusion):** Fixed benchmark row-count propagation in scalar GCD Criterion benchmarks; contributed compatibility fixes to [DataFusion-Spark](https://github.com/apache/datafusion-spark) covering Spark 4 string charset encoding and datetime interval overflow handling.
- **[Apache Arrow (Rust)](https://github.com/apache/arrow-rs):** Addressed decimal casting edge cases in `arrow-cast` under extreme scale expansion, preserving zero values while safely handling overflow.

### [Marine Pollution Intelligence](https://github.com/Subodh-17/marine-pollution-intelligence)
*Autonomous satellite radar (SAR) oil spill detection and hydrodynamic drift hindcasting platform.*
- Implemented Copernicus Sentinel-1 SAR image processing with 7x7 Lee speckle filtering and adaptive local Gaussian thresholding to isolate oil slicks from sea clutter.
- Integrated dual lightweight ONNX Runtime CPU models (`SpillUNet` and `SceneClassifier`, ~105 KB total payload) for zero-GPU edge inference.
- Built a 2D Euler hydrodynamic drift model driven by surface wind shear and ocean current vectors (Open-Meteo CMEMS/MET Norway).
- Built with FastAPI, React, Leaflet GIS, and SQLite/PostgreSQL.

### [Predictive Logistics — SIH 26251](https://github.com/Subodh-17/Predictive_Logistics_SIH_26251)
*Terrain- and weather-aware dynamic multi-modal freight routing engine (Smart India Hackathon).*
- Developed an A* graph routing engine factoring in Digital Elevation Model (DEM) slope penalties and physical speed floors.
- Built a 7-factor dispatch priority queue balancing perishability, contract SLAs, transport cost, and route reliability.
- Backed by PostgreSQL and PostGIS spatial queries (`ST_DWithin`, `ST_LineInterpolatePoint`) for waypoint tracking, covered by a 280-test regression suite.

### [StockVision V3 & Quantitative Forecasting](https://github.com/Subodh-17/stockvision-scilab-gui)
*Quantitative time-series forecasting terminal built in native Scilab for the Scilab GUIVerse Hackathon.*
- Implemented OLS polynomial trend fitting with 95% prediction intervals, autoregressive AR(p) modeling, and Holt double exponential smoothing.
- Evaluated models using multi-fold walk-forward validation against naive persistence baselines.
- Companion work in Python ([`stock_prediction_python`](https://github.com/Subodh-17/stock_prediction_python)) evaluates LSTM sequence models alongside regression baselines.

### [Blueledger](https://github.com/Subodh-17/Blueledger)
*Decentralized measurement, reporting, and verification (MRV) registry for blue carbon restoration credits (SIH PS 25038).*
- Solidity 0.8.20 smart contracts enforcing verification role separation so field verifiers cannot issue credits for their own assessments.
- Integrated IPFS (Kubo RPC & Pinata) for immutable content-addressed storage of remote-sensing evidence and field survey proofs.

---

## Connect

- **GitHub:** [@Subodh-17](https://github.com/Subodh-17)
- **LinkedIn:** [Subodh](https://www.linkedin.com/in/subodh-b-b705b5403)
- **Instagram:** [@subodh17_](https://www.instagram.com/subodh17_?stkn=cnplbHl2dHA1a244)
- **Email:** [subodh171011@gmail.com](mailto:subodh171011@gmail.com)
