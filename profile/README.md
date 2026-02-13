<h1>
  MAGMA-s 🔥
  <img src="assets/magma_logo.png" align="right" width="120"/>
</h1>

**Multi-Agent for Manipulation – by Siléane**

MAGMA-s is a CIFRE PhD research project conducted jointly by **Siléane** and **LAAS-CNRS**.

MAGMA-s is a modular research framework for building, training, and deploying **small-scale multimodal agents (<2B parameters)** capable of reasoning, planning, and acting in robotic environments.

The project focuses on structured tool use, embodied reasoning, simulation-driven training, and real-world robotic deployment with a strong emphasis on **long-horizon interactive tasks** and efficiency on limited hardware (e.g., laptops or edge devices)

<p align="center">
  <img src="assets/sileane_logo.png" height="60"/>
  &nbsp;&nbsp;&nbsp;
  <img src="assets/laas_logo.png" height="60"/>
</p>

---

## 🎯 Vision

MAGMA-s aims to:

- Enable **language-conditioned robotic reasoning and control**
- Structure agent behavior through **explicit tool abstraction and callable actions**
- Target **non-episodic, evolving tasks**, where:
  - The environment state is not reset
  - Each stage depends on previous outcomes
  - Errors compound over time

We explicitly study **compounding error and misalignment** as primary causes of long-horizon failure in robotic agents.

MAGMA-s is designed for research in embodied AI, adaptive robotics, and tool-augmented small foundation models.

---

## 🧠 Core Design Principles

- Small models (<2B parameters)
- Simulation-first training
- Human-defined task primitives
- Self-play and autonomous data generation
- Tool-structured reasoning
- Efficient deployment on constrained hardware

---

## 🏗 Architecture Overview

MAGMA-s follows a layered modular structure:

### **MAGMA-GEN**
A simulation-based data generation pipeline that produces interaction-grounded training data **without human demonstrations**.

Humans define:
- Task components
- Stage primitives
- Environment constraints

The system then performs structured self-play in simulation to generate training trajectories.

---

### **MAGMA-ROS2-\***
A suite of ROS2 packages enabling deployment of MAGMA-s agents on robotic systems across various platforms and tasks.

These packages expose robot capabilities as callable tools within the agent reasoning loop.

---

### **MAGMA-BENCH**
A benchmarking framework designed to evaluate:

- Long-horizon reasoning
- Tool selection accuracy
- Compounding error behavior
- Task completion over 12+ sequential stages

The benchmark specifically avoids episodic resets to reflect realistic robotic deployment.

---

### Supporting Packages

Additional internal packages (e.g., **MAGMA-CORE**, **MAGMA-AGENT**, planners, etc.) provide runtime infrastructure and orchestration.  
They support the main research contributions but are not standalone scientific releases.

---

## 📦 Repository Status

The publication of MAGMA-s is currently in progress.  
Packages will be released progressively according to the following roadmap:

| Package | Planned Release |
|----------|----------------|
| MAGMA-GEN | March 2026 |
| MAGMA-CORE | March 2026 |
| MAGMA-AGENT | March 2026 |
| MAGMA-ROS2-CORE | March 2026 |
| MAGMA-ROS2-APPS | March 2026 |
| MAGMA-BENCH | September 2026 |

During this transition phase, APIs and documentation may evolve.

---

## 🎓 Research Context

MAGMA-s is developed as part of a CIFRE PhD thesis focusing on:

- Long-horizon robotic manipulation
- Tool-aware small language models
- Autonomous data generation in simulation
- Structured reasoning under compounding error
- Deployment-efficient multimodal agents

---

## 🎯 Intended Use

MAGMA-s is designed for:

- Academic research laboratories
- Industrial robotics R&D teams
- Embodied AI experimentation
- Efficient foundation-model deployment on real robots

---

## 📜 License

BSD 2-Clause License.

---

## 📖 Citation

If you use MAGMA-s in academic work, please cite:

- **MAGMA-GEN**: <Under review, RSS 2026>
- **MAGMA-ROS2-\***: <Under review, RSS 2026>
- A comprehensive paper will be released with **MAGMA-BENCH** (September 2026)

Full citation details will be provided upon publication.

---

## 📬 Contact

For collaboration, research inquiries, or early access discussions:

l.bernat@sileane.com
