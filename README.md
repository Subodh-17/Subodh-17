<div align="center">



<img src="assets/profile_banner.jpg" alt="Subodh Bansode Portfolio Banner — Systems and ML Engineering" width="100%" />



<br>



# Subodh Bansode



### Computer Science Student | Systems & ML Engineering



<p><strong>Vectorized Query Engines &bull; ML Runtime Systems &bull; Geospatial Pipelines &bull; OSS Infrastructure</strong></p>



<p>

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

</p>



<p align="center">

  <a href="https://www.rust-lang.org/"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/rust/rust-original.svg" alt="Rust" width="28" height="28" /></a> &nbsp;&nbsp;&nbsp;&nbsp;

  <a href="https://www.python.org/"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" alt="Python" width="28" height="28" /></a> &nbsp;&nbsp;&nbsp;&nbsp;

  <a href="https://datafusion.apache.org/"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/apache/apache-original.svg" alt="Apache DataFusion" width="28" height="28" /></a> &nbsp;&nbsp;&nbsp;&nbsp;

  <a href="https://pytorch.org/"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/pytorch/pytorch-original.svg" alt="PyTorch" width="28" height="28" /></a> &nbsp;&nbsp;&nbsp;&nbsp;

  <a href="https://fastapi.tiangolo.com/"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/fastapi/fastapi-original.svg" alt="FastAPI" width="28" height="28" /></a> &nbsp;&nbsp;&nbsp;&nbsp;

  <a href="https://www.postgresql.org/"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/postgresql/postgresql-original.svg" alt="PostgreSQL" width="28" height="28" /></a> &nbsp;&nbsp;&nbsp;&nbsp;

  <a href="https://www.typescriptlang.org/"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/typescript/typescript-original.svg" alt="TypeScript" width="28" height="28" /></a> &nbsp;&nbsp;&nbsp;&nbsp;

  <a href="https://www.docker.com/"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/docker/docker-original.svg" alt="Docker" width="28" height="28" /></a> &nbsp;&nbsp;&nbsp;&nbsp;

  <a href="https://www.kernel.org/"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/linux/linux-original.svg" alt="Linux" width="28" height="28" /></a>

</p>



</div>



<br>



---



## Engineering Focus



Computer science student and systems contributor specializing in analytical query execution kernels, runtime determinism, zero-copy serialization, and production data infrastructure. Upstream open-source contributor across foundational systems: **Apache DataFusion** (Rust vectorized query engine), **SafeTensors**, and **PyTorch Lightning**, alongside **10 verified merged upstream pull requests across 8 open-source repositories**. Committed to empirical software engineering: isolating root causes, implementing minimal non-breaking patches, writing deterministic regression tests, and collaborating transparently through upstream peer review.



---



## Featured Engineering Projects



### [Marine Pollution Intelligence](https://github.com/Subodh-17/marine-pollution-intelligence)

*End-to-end Copernicus Sentinel-1 SAR satellite oil spill detection and maritime vessel attribution platform (Smart India Hackathon 2026).*



- **Architecture & Engineering:** Ingests Copernicus Sentinel-1 SAR Level-1 Ground Range Detected (GRD) imagery; applies Lee adaptive speckle filtering to suppress radar backscatter noise; segments oil slick candidate boundaries via adaptive Otsu thresholding; simulates leeway oceanographic drift hindcasting coupled with historical AIS maritime trajectory vectors to compute explainable vessel attribution scores.

- **Resilience & Concurrency:** Hardened with Metocean request coalescing, circuit breakers for rate-limit backoff, and non-blocking asynchronous event loop pipelines.

- **Verification:** Validated across 8 consecutive merged pull requests on GitHub `main` branch.

- **Stack:** `Python` &bull; `FastAPI` &bull; `React` &bull; `Leaflet` &bull; `GeoTIFF Radar Processing` &bull; `Lee Speckle Filter` &bull; `AIS Hindcast Modeling`



### [Predictive Logistics](https://github.com/Subodh-17/Predictive_Logistics_SIH_26251)

*Forward supply chain shortage forecasting and terrain-aware vehicle route optimization system (SIH Problem Statement 26251).*



- **Architecture & Engineering:** Generates multi-horizon statistical demand forecasts (7, 14, and 30-day windows) using Random Forest cross-validation and priority dispatch queue scoring. Optimizes vehicle routing against terrain elevation gradients and road weather hazards, integrating simulated ESP32/RFID sensor inventory telemetry.

- **Verification:** Automated CI pipeline passing across live PostGIS spatial integration and machine learning pipeline test suites (GitHub Actions CI Run 40095697275, October 2026).

- **Stack:** `Python` &bull; `FastAPI` &bull; `PostgreSQL / PostGIS` &bull; `SQLAlchemy` &bull; `React` &bull; `Vite` &bull; `TypeScript` &bull; `Docker Compose`



### [StockVision](https://github.com/Subodh-17/stockvision-scilab-gui)

*Interactive numerical desktop studio for time-series forecasting, comparative model evaluation, and realistic backtesting.*



- **Architecture & Engineering:** Benchmarks 5 statistical forecasting models (Linear Regression, Autoregressive AR, Holt Exponential Smoothing, Ridge L2 Regularization, and naive persistence) on synchronized chronological test windows. Executes expanding-window walk-forward validation and backtests long-only trading signals with explicit 0.15% transaction friction, slippage, and execution lag.

- **Verification:** Verified production-ready under Scilab 2026.1.0; complete zero-network offline execution with deterministic linear algebra kernels.

- **Stack:** `Scilab` (Core Numerics, Least Squares Solver, Embedded GUI Controls, Matrix Plotting)



### [Blue Carbon MRV](https://github.com/Subodh-17/Blueledger)

*Coastal blue carbon restoration measurement, reporting, and verification platform.*



- **Architecture & Engineering:** Dual web and mobile interface for field ecological data submission coupled with a Node.js/PostgreSQL registry backend. Implements an ERC-20 carbon credit smart contract on Hardhat/Solidity for transparent, audit-ready ecological credit minting and verification.

- **Stack:** `Solidity` &bull; `Hardhat` &bull; `Node.js` &bull; `Express` &bull; `PostgreSQL` &bull; `JavaScript` &bull; `HTML5/CSS3`



---



## Open Source Contributions



### Merged Upstream Contributions (10 PRs across 8 Ecosystems)



| Pull Request & Ecosystem | Contribution Summary & Upstream Review | Status |

| :--- | :--- | :---: |

| [apache/datafusion#26465](https://github.com/apache/datafusion/pull/26465)<br>[![Apache DataFusion](https://img.shields.io/badge/Apache_DataFusion-D22128?style=flat-square&logo=apache&logoColor=white)](https://datafusion.apache.org/) | Propagated CLI row count argument through Criterion benchmark harness, preventing hardcoded defaults.<br>*(Merged by Apache DataFusion PMC Chair `@alamb`, approved by committer `@kumarUjjawal`)* | ![Merged](https://img.shields.io/badge/Merged-2da44e?style=flat-square&logo=git&logoColor=white) |

| [huggingface/diffusers#14961](https://github.com/huggingface/diffusers/pull/14961)<br>[![Hugging Face Diffusers](https://img.shields.io/badge/Hugging_Face_Diffusers-FFD21E?style=flat-square&logo=huggingface&logoColor=black)](https://github.com/huggingface/diffusers) | Corrected active PEFT LoRA adapter tracking across text encoders during multi-adapter inference pipelines.<br>*(Approved by PEFT maintainer `@BenjaminBossan`, reviewed by Diffusers lead `@sayakpaul`)* | ![Merged](https://img.shields.io/badge/Merged-2da44e?style=flat-square&logo=git&logoColor=white) |

| [ionfwsrijan/PatchPilot#350](https://github.com/ionfwsrijan/PatchPilot/pull/350)<br>[![PatchPilot](https://img.shields.io/badge/PatchPilot-000000?style=flat-square&logo=github&logoColor=white)](https://github.com/ionfwsrijan/PatchPilot) | Prioritized vulnerability findings by normalized severity scoring across backend scanner outputs.<br>*(Approved & merged by maintainer `@ionfwsrijan`)* | ![Merged](https://img.shields.io/badge/Merged-2da44e?style=flat-square&logo=git&logoColor=white) |

| [existence-master/Sentient#295](https://github.com/existence-master/Sentient/pull/295)<br>[![Sentient](https://img.shields.io/badge/Sentient-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/existence-master/Sentient) | Implemented target-scoped CDP download isolation to preserve user browser download integrity during automation sessions.<br>*(Approved by maintainer `@itsskofficial`)* | ![Merged](https://img.shields.io/badge/Merged-2da44e?style=flat-square&logo=git&logoColor=white) |

| [existence-master/Sentient#326](https://github.com/existence-master/Sentient/pull/326)<br>[![Sentient](https://img.shields.io/badge/Sentient-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/existence-master/Sentient) | Isolated Model Context Protocol (MCP) OAuth credentials by server URL to prevent cross-server credential collisions and leakage.<br>*(Approved by maintainer `@itsskofficial`)* | ![Merged](https://img.shields.io/badge/Merged-2da44e?style=flat-square&logo=git&logoColor=white) |

| [ThreeMoonsLab/agents-shipgate#1007](https://github.com/ThreeMoonsLab/agents-shipgate/pull/1007)<br>[![Agents Shipgate](https://img.shields.io/badge/Agents_Shipgate-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/ThreeMoonsLab/agents-shipgate) | Resolved PEP 508 extras-qualified pin parsing failures during deterministic dependency lockfile verification.<br>*(Approved by `@pengfei-threemoonslab`)* | ![Merged](https://img.shields.io/badge/Merged-2da44e?style=flat-square&logo=git&logoColor=white) |

| [knight22-21/CodePrism#72](https://github.com/knight22-21/CodePrism/pull/72)<br>[![CodePrism](https://img.shields.io/badge/CodePrism-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/knight22-21/CodePrism) | Enforced strict schema validation to reject unknown configuration keys and prevent silent runtime fallbacks.<br>*(Approved by `@knight22-21`)* | ![Merged](https://img.shields.io/badge/Merged-2da44e?style=flat-square&logo=git&logoColor=white) |

| [knight22-21/CodePrism#70](https://github.com/knight22-21/CodePrism/pull/70)<br>[![CodePrism](https://img.shields.io/badge/CodePrism-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/knight22-21/CodePrism) | Corrected complex PEP 440 version specifier parsing for dependency constraint boundaries.<br>*(Approved by `@knight22-21`)* | ![Merged](https://img.shields.io/badge/Merged-2da44e?style=flat-square&logo=git&logoColor=white) |

| [batrapulkit/squidbrake#51](https://github.com/batrapulkit/squidbrake/pull/51)<br>[![SquidBrake](https://img.shields.io/badge/SquidBrake-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/batrapulkit/squidbrake) | Established cross-platform GitHub Actions CI test matrices across Linux, Windows, macOS, and Python 3.13.<br>*(Merged by maintainer `@batrapulkit`)* | ![Merged](https://img.shields.io/badge/Merged-2da44e?style=flat-square&logo=git&logoColor=white) |

| [corsairdev/corsair#1398](https://github.com/corsairdev/corsair/pull/1398)<br>[![Corsair](https://img.shields.io/badge/Corsair-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/corsairdev/corsair) | Integrated Dynapictures dynamic image generation plugin into the Corsair TypeScript framework.<br>*(Approved by `@devjain32`, `@Dhirenderchoudhary`)* | ![Merged](https://img.shields.io/badge/Merged-2da44e?style=flat-square&logo=git&logoColor=white) |



---



### Selected In-Review Upstream Work



| Pull Request & Ecosystem | Contribution Scope & Verification Evidence | Status |

| :--- | :--- | :---: |

| [apache/datafusion#26376](https://github.com/apache/datafusion/pull/26376)<br>[![Apache DataFusion](https://img.shields.io/badge/Apache_DataFusion-D22128?style=flat-square&logo=apache&logoColor=white)](https://datafusion.apache.org/) | `fix(expr): differentiate aggregate functions with and without explicit cast in output schema (#26221)`. Rebased schema inference across 33 files; all required CI checks passing with zero merge conflicts against upstream `origin/main`. | ![In Review](https://img.shields.io/badge/In_Review-0969da?style=flat-square&logo=github&logoColor=white) |

| [safetensors/safetensors#873](https://github.com/safetensors/safetensors/pull/873)<br>[![SafeTensors](https://img.shields.io/badge/SafeTensors-FFD21E?style=flat-square&logo=huggingface&logoColor=black)](https://github.com/huggingface/safetensors) | `fix: allow slicing zero-length dimensions`. Supported zero-length slice operations in Rust tensor core without panics. | ![In Review](https://img.shields.io/badge/In_Review-0969da?style=flat-square&logo=github&logoColor=white) |

| [Lightning-AI/pytorch-lightning#22006](https://github.com/Lightning-AI/pytorch-lightning/pull/22006)<br>[![PyTorch Lightning](https://img.shields.io/badge/PyTorch_Lightning-792EE5?style=flat-square&logo=lightning&logoColor=white)](https://github.com/Lightning-AI/pytorch-lightning) | `fix: set sampler epoch before creating resumed iterator`. Synchronized sampler epoch state prior to iterator initialization for deterministic distributed training restarts. | ![In Review](https://img.shields.io/badge/In_Review-0969da?style=flat-square&logo=github&logoColor=white) |

| [Lightning-AI/pytorch-lightning#22017](https://github.com/Lightning-AI/pytorch-lightning/pull/22017)<br>[![PyTorch Lightning](https://img.shields.io/badge/PyTorch_Lightning-792EE5?style=flat-square&logo=lightning&logoColor=white)](https://github.com/Lightning-AI/pytorch-lightning) | `Improve error message for mixed strategy namespaces`. Validated distributed strategy configuration combinations and error diagnostics. | ![In Review](https://img.shields.io/badge/In_Review-0969da?style=flat-square&logo=github&logoColor=white) |



---



## Community Recognition



- **[XERJ Corpus Hub](https://hub.xerj.org/contributors/Subodh-17):** Featured contributor profile, with an [mloda-ai/mloda](https://github.com/mloda-ai/mloda) contribution included in the public reference index. Indexes commit [`e8f8eae2d2`](https://github.com/mloda-ai/mloda/commit/e8f8eae2d296f7957d3f94c266b051cd44d0c608) (*"fix: data race in concurrent joins sharing destination"*, 4 files &bull; 215 lines &bull; Python) as a worked reference implementation for AI coding agents.

  <br><br>

  <a href="https://hub.xerj.org/contributors/Subodh-17">

    <img src="https://hub.xerj.org/contributors/Subodh-17/badge.svg" alt="XERJ Corpus Hub contributor badge" />

  </a>



---



## Active Focus & Issue Work



- **[PatchPilot Issue #319](https://github.com/ionfwsrijan/PatchPilot/issues/319):** `[Bug] Finding Status Changes Silently Lost on Every Page Reload — Data Loss`

  - **Assignment Status:** Officially assigned by maintainer `@ionfwsrijan` on October 28, 2026 (1-week submission window ending November 4, 2026).

  - **Engineering Scope:** Eliminates silent finding status loss upon page refresh caused by frontend type omission (`BackendFinding`) and mapper hardcoded defaults (`mapBackendFindingToUi`).

  - **Validation:** Targeted fix and regression tests validated across 8 backend pytest tests and 3 frontend mapper tests (`feat/issue-319-finding-status-persistence`).



---



## Technical Stack



<table>

  <tr>

    <td width="22%"><strong>Languages</strong></td>

    <td>

      <a href="https://www.rust-lang.org/"><img src="https://img.shields.io/badge/Rust-000000?style=flat-square&logo=rust&logoColor=white" alt="Rust" /></a>

      <a href="https://www.python.org/"><img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python" /></a>

      <a href="https://www.typescriptlang.org/"><img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript" /></a>

      <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript"><img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black" alt="JavaScript" /></a>

      <a href="https://www.postgresql.org/"><img src="https://img.shields.io/badge/SQL_(PostgreSQL)-4169E1?style=flat-square&logo=postgresql&logoColor=white" alt="SQL (PostgreSQL)" /></a>

      <a href="https://www.scilab.org/"><img src="https://img.shields.io/badge/Scilab-002B49?style=flat-square&logo=scilab&logoColor=white" alt="Scilab" /></a>

    </td>

  </tr>

  <tr>

    <td><strong>Data & Query Systems</strong></td>

    <td>

      <a href="https://datafusion.apache.org/"><img src="https://img.shields.io/badge/Apache_DataFusion-D22128?style=flat-square&logo=apache&logoColor=white" alt="Apache DataFusion" /></a>

      <a href="https://arrow.apache.org/"><img src="https://img.shields.io/badge/Apache_Arrow-E41C23?style=flat-square&logo=apachearrow&logoColor=white" alt="Apache Arrow" /></a>

      <a href="https://www.postgresql.org/"><img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" alt="PostgreSQL" /></a>

      <a href="https://postgis.net/"><img src="https://img.shields.io/badge/PostGIS-336791?style=flat-square&logo=postgresql&logoColor=white" alt="PostGIS" /></a>

      <a href="https://www.sqlalchemy.org/"><img src="https://img.shields.io/badge/SQLAlchemy-D71F00?style=flat-square&logo=sqlalchemy&logoColor=white" alt="SQLAlchemy" /></a>

      <a href="https://fastapi.tiangolo.com/"><img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" alt="FastAPI" /></a>

    </td>

  </tr>

  <tr>

    <td><strong>ML & Runtime Systems</strong></td>

    <td>

      <a href="https://pytorch.org/"><img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white" alt="PyTorch" /></a>

      <a href="https://github.com/huggingface/diffusers"><img src="https://img.shields.io/badge/Hugging_Face_Diffusers-FFD21E?style=flat-square&logo=huggingface&logoColor=black" alt="Hugging Face Diffusers" /></a>

      <a href="https://github.com/huggingface/safetensors"><img src="https://img.shields.io/badge/SafeTensors-FFD21E?style=flat-square&logo=huggingface&logoColor=black" alt="SafeTensors" /></a>

      <a href="https://lightning.ai/"><img src="https://img.shields.io/badge/PyTorch_Lightning-792EE5?style=flat-square&logo=lightning&logoColor=white" alt="PyTorch Lightning" /></a>

      <a href="https://scikit-learn.org/"><img src="https://img.shields.io/badge/Scikit--Learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white" alt="Scikit-Learn" /></a>

      <a href="https://numpy.org/"><img src="https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white" alt="NumPy" /></a>

      <a href="https://scipy.org/"><img src="https://img.shields.io/badge/SciPy-8CAAE6?style=flat-square&logo=scipy&logoColor=white" alt="SciPy" /></a>

    </td>

  </tr>

  <tr>

    <td><strong>Cloud & Infrastructure</strong></td>

    <td>

      <a href="https://www.docker.com/"><img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" alt="Docker" /></a>

      <a href="https://www.kernel.org/"><img src="https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black" alt="Linux" /></a>

      <a href="https://chromedevtools.github.io/devtools-protocol/"><img src="https://img.shields.io/badge/Chrome_DevTools_Protocol-4285F4?style=flat-square&logo=googlechrome&logoColor=white" alt="Chrome DevTools Protocol" /></a>

      <a href="https://modelcontextprotocol.io/"><img src="https://img.shields.io/badge/Model_Context_Protocol-4A154B?style=flat-square&logo=anthropic&logoColor=white" alt="Model Context Protocol" /></a>

    </td>

  </tr>

  <tr>

    <td><strong>Developer Tooling & CI</strong></td>

    <td>

      <a href="https://git-scm.com/"><img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white" alt="Git" /></a>

      <a href="https://github.com/features/actions"><img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white" alt="GitHub Actions" /></a>

      <a href="https://docs.pytest.org/"><img src="https://img.shields.io/badge/pytest-0A9EDC?style=flat-square&logo=pytest&logoColor=white" alt="pytest" /></a>

      <a href="https://nodejs.org/"><img src="https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white" alt="Node.js" /></a>

    </td>

  </tr>

</table>



---



<div align="center">



**Subodh Bansode** &nbsp;&bull;&nbsp; [GitHub](https://github.com/Subodh-17) &nbsp;&bull;&nbsp; [Email](mailto:subodh171011@gmail.com) &nbsp;&bull;&nbsp; [Instagram](https://www.instagram.com/subodh17_)



*All contributions, pull requests, and project milestones cited above are grounded in verified Git commits and public repository records.*



</div>