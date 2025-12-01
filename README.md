# 🛠️ NTN-Environment-Docker: Reproducible Base Environment for Quantum-AI-Space Communications

**QASCOM Lab Initiative** | **[Associated with All QASCOM Journal & Conference Papers]**

[![GitHub Stars]](https://github.com/QASCOM-Lab/NTN-Environment-Docker/stargazers)
[![License: MIT]](https://opensource.org/licenses/MIT)
[![Docker Hub]](https://hub.docker.com/u/qascom)
[![QASCOM Lab Website]](https://phuchaodo.coregenaihub.com/)

---

### 🚀 Overview

The `NTN-Environment-Docker` repository is the **cornerstone for reproducibility** across all QASCOM Lab research. It provides a standardized, version-controlled set of Docker images and configurations (Dockerfiles) that define the exact computational environment used for our published experiments in Quantum, AI, and Satellite Communications.

By encapsulating complex dependencies—such as specific versions of quantum libraries (Qiskit/PennyLane) alongside orbital mechanics tools (Poliastro)—this environment eliminates dependency conflicts, guaranteeing that researchers worldwide can easily validate and extend our published results.

### 💡 Key Contents & Technical Contributions (PoC Focus)

1.  **Modular Dockerfiles:** Contains specialized `Dockerfiles` tailored for the unique needs of our research pillars:
    *   `Dockerfile.QuantumStack`: Optimized for Qiskit, PennyLane, and quantum simulators (used by **Quantum-NTN-Scheduler** and **Hybrid-QML-Detector**).
    *   `Dockerfile.AITelecomStack`: Optimized for PyTorch/TensorFlow, PyTorch Geometric, and specialized networking libraries (used by **FedSatSim-Security** and **ST-GNN-Traffic-Compressor**).
2.  **Core Simulation Libraries:** Pre-configured with essential space and network simulation tools: `Poliastro`, `Skyfield`, `PyTorch Geometric`, and specific FL frameworks.
3.  **Dependency Mapping:** A detailed `requirements.txt` and documentation outlining the exact library versions used for each major paper submission, ensuring long-term archival integrity.
4.  **Base Tutorials:** Includes introductory Jupyter Notebooks guiding users on basic environment verification, orbital mechanics setup, and GNN data loading within the containerized environment.

### 📈 Business & Research Impact Showcase

This repository emphasizes the commitment of QASCOM Lab to open, verifiable science:

*   **Scientific Rigor:** Guarantees that all findings published by QASCOM Lab are easily verifiable by the scientific community, boosting trust and citation rates.
*   **Rapid Onboarding:** Allows new collaborators or research interns to set up a fully working research environment in minutes, maximizing productivity.
*   **Industrial Deployment Foundation:** Provides stable, containerized environments that can serve as the deployment base for Proof-of-Concept models in a real-world production setting.

### ⚙️ Setup and Usage

**Prerequisites:** Docker must be installed.

#### Step 1: Clone the Repository

```bash
git clone https://github.com/QASCOM-Lab/NTN-Environment-Docker.git
cd NTN-Environment-Docker
```

#### Step 2: Build the Base Image (Quantum Stack Example)

This example builds the environment required for our quantum research (Repo 1 & 4).

```bash
# Build the specialized Quantum Stack image
docker build -f Dockerfile.QuantumStack -t qascom-quantum-base:latest .
```

#### Step 3: Utilize in Other Repositories

Other QASCOM Lab repositories (e.g., `Quantum-NTN-Scheduler`) will reference this base image in their respective `Dockerfiles` or `docker-compose.yml` to minimize size and build time, ensuring consistency across all experiments.

### 🗺️ Project Roadmap

| Phase | Goal | Status |
| :--- | :--- | :--- |
| **V1.0 (Current)** | Definition and stabilization of `Dockerfile.QuantumStack` and `Dockerfile.AITelecomStack` based on current paper dependencies. | *Planning* |
| **V1.1 (Q1 2026)** | Integration of GPU support (CUDA) for the AI Telecom Stack to enable large-scale GNN/FL training. | *Planned* |
| **V2.0 (H1 2026)** | Implementation of automated dependency checks and version bump alerts across all derived repositories. | *Planned* |

### 📚 Associated Publications

This environment underpins the reproducibility of all QASCOM Lab research, including:

*   All papers associated with **Quantum-NTN-Scheduler** and **Hybrid-QML-Detector**.
*   All papers associated with **FedSatSim-Security** and **ST-GNN-Traffic-Compressor**.

### 🤝 Contribution

We welcome suggestions for optimizing the environment, updating library versions, and adding new simulation utilities beneficial to space communications research.
