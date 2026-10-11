<div align="center">

# SUBODH BANSODE
### AI/ML • SYSTEMS & DATA INFRASTRUCTURE • OPEN SOURCE

Building reliable ML infrastructure, data-intensive systems, and verified open-source tooling.

<br>

<a href="https://github.com/Subodh-17">
  <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub" />
</a>
<a href="mailto:subodh171011@gmail.com">
  <img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" />
</a>

</div>

<br>

## 🎯 Engineering Focus

- **ML Infrastructure & Systems:** Upstream contributions to PyTorch, Hugging Face (Diffusers, Transformers), and PyTorch Lightning covering attention caching, distributed training determinism, and sharded model persistence.
- **Data-Intensive Applications & Concurrency:** Multi-tenant and concurrent data pipelines, spatial data engineering (PostgreSQL/PostGIS), and query planner race condition isolation.
- **Developer Tooling & Reliability:** Multi-platform CI/CD automation across Linux, Windows, and macOS, PEP 508 / PEP 440 packaging verification, and strict schema validation.
- **Systems & Memory Safety:** Rust-based tensor indexing (`safetensors`), browser automation internals (Chrome DevTools Protocol / CDP), and native runtime exploration.

---

## 💻 Technical Portfolio & Technology Areas

A balanced multi-language portfolio grounded in verified code contributions, full-stack systems projects, and ongoing technical exploration across 19 technology areas:

### 🛠️ Demonstrated Through Contributions & Projects
*Technologies verified through merged upstream pull requests, active open-source fixes, or end-to-end applications:*
- **Python:** Core ML frameworks (PyTorch, Diffusers, Transformers), distributed training (PyTorch Lightning), backend services (FastAPI), packaging and lockfile verification (PEP 508 / PEP 440).
- **AI / ML Systems:** PEFT LoRA adapter inference, attention KV cache prefill, sharded checkpoint handling, computer vision / SAR satellite imagery pipelines.
- **Rust:** Tensor engine internals and zero-copy slice bounds (`safetensors` slice indexing & PyO3 integration).
- **JavaScript & TypeScript:** Plugin architectures (Corsair TypeScript plugin), UI components (Obsidian Agent React chart controls, Vite dashboards).
- **SQL & Databases:** Relational data modeling, spatial querying with **PostgreSQL & PostGIS**, database query planners and concurrent join synchronization (`mloda`).
- **Blockchain / Web3:** Environmental data verification, smart contracts (**Solidity**, **Hardhat**) in Blue Carbon MRV.
- **Docker & CI/CD:** Containerized multi-service architectures (Docker Compose), multi-platform CI matrices (**GitHub Actions** on Linux, Windows, macOS).
- **HTML & CSS:** Semantic structure and responsive styling across full-stack web applications and analytics dashboards.

### 🔬 Applied Exploration & Tooling
*Technologies explored through code investigations, connector runtimes, or systems internals:*
- **C & C++:** Systems internals, numerical runtime analysis, and GPU inference engine architecture (vLLM, Scilab engine integration).
- **Java:** Data integration architectures and connector lifecycles (Airbyte CDK connector exploration).
- **MongoDB:** Document datastore patterns and connector interfaces.

### 🧭 Active Learning & Technical Interests
*Ecosystems actively explored for cross-platform, systems, and distributed computing architectures:*
- **Kubernetes:** Cloud-native workload orchestration and service deployment patterns.
- **Kotlin & Dart:** Cross-platform and native mobile application architecture (Flutter / Android tooling).
- **Swift:** Native client runtimes and systems software.
- **Elixir:** Fault-tolerant distributed systems and actor-model concurrency on the BEAM virtual machine.
- **PHP:** Web application architectures and legacy open-source platform patterns.

---

## 🌐 Open Source Contributions

### ✅ Merged Upstream Contributions

- **[huggingface/diffusers#14961](https://github.com/huggingface/diffusers/pull/14961)** — Fix active adapter detection for text encoders
  - Corrected active PEFT LoRA adapter tracking during text-encoder inference.
- **[ThreeMoonsLab/agents-shipgate#1007](https://github.com/ThreeMoonsLab/agents-shipgate/pull/1007)** — Support PEP 508 extras-qualified pins in dependency lock verification
  - Resolved parser failures when package locks contain extras declarations (`pkg[extra]==x.y`).
- **[batrapulkit/squidbrake#51](https://github.com/batrapulkit/squidbrake/pull/51)** — Add cross-platform CI matrix on Windows, macOS, and Python 3.13
  - Established multi-OS GitHub Actions workflow coverage across platforms and modern Python versions.
- **[corsairdev/corsair#1398](https://github.com/corsairdev/corsair/pull/1398)** — Add Dynapictures image generation plugin
  - Integrated dynamic image generation capabilities into the Corsair plugin framework (TypeScript).
- **[knight22-21/CodePrism#72](https://github.com/knight22-21/CodePrism/pull/72)** — Reject unknown configuration keys
  - Implemented strict schema validation to prevent silent fallbacks on invalid user YAML config.
- **[knight22-21/CodePrism#70](https://github.com/knight22-21/CodePrism/pull/70)** — Parse requirement specifications correctly
  - Fixed version specifier parsing for complex PEP 440 constraints.

### 🔄 Active Upstream Pull Requests

*Live pull requests under active review or in-flight iteration:*

- **Hugging Face Transformers:**
  - **[PR #49192](https://github.com/huggingface/transformers/pull/49192)** — Fix `AutoTokenizer` backend selection for CohereLabs tiny-aya checkpoints *(111/111 passing CI checks, awaiting review)*
- **PyTorch Lightning:**
  - **[PR #22017](https://github.com/Lightning-AI/pytorch-lightning/pull/22017)** — Improve error diagnostics for mixed strategy namespaces *(Awaiting review)*
  - **[PR #22006](https://github.com/Lightning-AI/pytorch-lightning/pull/22006)** — Set sampler epoch before creating resumed iterator in distributed training *(Awaiting review)*
- **Hugging Face Diffusers:**
  - **[PR #14990](https://github.com/huggingface/diffusers/pull/14990)** — Support `torch.compile` for Qwen Image 2.1 transformer layers *(Awaiting review)*
  - **[PR #14989](https://github.com/huggingface/diffusers/pull/14989)** — Fix cross-variant shard deletion in `save_pretrained` *(Awaiting review)*
  - **[PR #14984](https://github.com/huggingface/diffusers/pull/14984)** — Preserve singleton dimensions in `numpy_to_pil` *(Awaiting review)*
  - **[PR #14983](https://github.com/huggingface/diffusers/pull/14983)** — Correct prompt embedding positional concatenation for Flux DreamBooth LoRA *(Awaiting review)*
  - **[PR #14982](https://github.com/huggingface/diffusers/pull/14982)** — Fix prior preservation weighting in advanced DreamBooth LoRA *(Awaiting review)*
  - **[PR #14971](https://github.com/huggingface/diffusers/pull/14971)** — Fix offline loading of sharded checkpoints *(Awaiting review)*
  - **[PR #14963](https://github.com/huggingface/diffusers/pull/14963)** — Validate PNDM inference step count *(Awaiting review)*
- **Hugging Face SafeTensors:**
  - **[PR #873](https://github.com/huggingface/safetensors/pull/873)** — Allow slicing zero-length dimensions in Rust core and Python bindings *(Awaiting review)*
- **Browser & Agent Tooling:**
  - **[Sentient PR #295](https://github.com/existence-master/Sentient/pull/295)** — Preserve user downloads during attached CDP browser sessions *(In progress — maintainer requested popup target tracking; local CDP fail-fast fix prepared)*
  - **[Obsidian Agent PR #68](https://github.com/aeshef/obsidian-agent/pull/68)** — Add per-chart reset control in TypeScript/React UI *(Awaiting review)*
- **Concurrent Data Systems:**
  - **[MLODA PR #1938](https://github.com/mloda-ai/mloda/pull/1938)** — Resolve race condition in concurrent joins sharing a destination *(Awaiting review)*
  - **[MLODA PR #1937](https://github.com/mloda-ai/mloda/pull/1937)** — Propagate `SystemExit` from multiprocessing workers *(Awaiting review)*
- **LLM Tooling:**
  - **[MS-Swift PR #10289](https://github.com/modelscope/ms-swift/pull/10289)** — Handle CLI help command gracefully *(Awaiting review)*

---

## 🚀 Selected Projects

### [Marine Pollution Intelligence](https://github.com/Subodh-17/Marine-Pollution-Intelligence-SIH)
End-to-end pipeline for detecting maritime oil spills and attributing them to responsible vessels.
- Implements Sentinel-1 SAR oil-slick detection and geometric characterization.
- Reconstructs historic AIS traffic and correlates it with drift hindcasting for vessel attribution scoring.
- Built with a FastAPI backend and interactive React map dashboard.

### [Predictive Logistics](https://github.com/Subodh-17/Predictive_Logistics_SIH_26251)
Full-stack forward supply chain simulation and predictive decision-support system.
- Predicts consumption shortages and optimizes delivery routing logic.
- Integrates geospatial data routing and a simulated ESP32/RFID sensor layer.
- Architecture driven by FastAPI, PostgreSQL/PostGIS, SQLAlchemy, and React/Vite in Docker.

### [Blue Carbon MRV](https://github.com/Subodh-17/WCEHackathon2026_Proteas)
Measurement, Reporting, and Verification platform for coastal blue carbon restoration projects.
- Deploys environmental data persistence and verification workflows utilizing Solidity and Hardhat.
- Provides specialized admin dashboards and field-worker mobile interfaces.
- Driven by a Node.js/Express backend coupled with PostgreSQL.

### [StockVision](https://github.com/Subodh-17/stockvision-scilab-gui)
Interactive time-series forecasting and market analysis tool.
- Fits Linear Regression, AR models, and Holt Exponential Smoothing.
- Executes 3-fold walk-forward validation and backtests BUY/SELL signals against standard benchmarks.
- Developed entirely as an interactive Scilab GUI.

---

## 📊 Open Source Activity Summary

<div align="center">
  <table>
    <tr>
      <td align="center" width="240">
        <b>✅ Merged Upstream</b><br>
        <b>6 PRs</b><br>
        Diffusers • Agents-Shipgate<br>Squidbrake • Corsair • CodePrism
      </td>
      <td align="center" width="240">
        <b>🔄 Active / In-Flight</b><br>
        <b>16 PRs</b><br>
        Transformers • Lightning<br>SafeTensors • Diffusers • Sentient
      </td>
      <td align="center" width="240">
        <b>🛠️ Engineering Domains</b><br>
        ML Infrastructure • Concurrency<br>Developer Tooling & CI/CD
      </td>
    </tr>
  </table>
</div>

<br>

### 🔄 Contribution Workflow

```text
       Identify Defect / Gap
                 ↓
       Reproduce & Isolate
                 ↓
     Implement Minimal Patch
                 ↓
       Add Regression Tests
                 ↓
   Run Multi-Platform Validation
                 ↓
Open PR → Maintainer Review → Merge
```

> Building, testing, reviewing, and contributing to real-world ML infrastructure and systems software — with a focus on reproducible fixes and meaningful upstream impact.
