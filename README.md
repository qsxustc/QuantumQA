# QuantumQA: Enhancing Scientific Reasoning via Physics-Consistent Dataset and Verification-Aware Reinforcement Learning

[![Paper](https://img.shields.io/badge/arXiv-Paper-<COLOR>.svg)]([https://arxiv.org/abs/2604.18176](https://arxiv.org/abs/2604.18176))
[![Dataset](https://img.shields.io/badge/HuggingFace-Dataset-<COLOR>.svg)](https://huggingface.co/datasets/qsxjack44/QuantumQA)
[![License: CC BY-NC 4.0](https://img.shields.io/badge/License-CC_BY--NC_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc/4.0/)

## 📖 Abstract

Large language models (LLMs) show strong capabilities in general reasoning but typically lack reliability in scientific domains like quantum mechanics, which demand strict adherence to physical constraints. This limitation arises from the scarcity of verifiable training resources and the inadequacy of coarse feedback signals in standard alignment paradigms. To address the data challenge, we introduce **QuantumQA**, a large-scale dataset constructed via a task-adaptive strategy and a hybrid verification protocol that combines deterministic solvers with semantic auditing to guarantee scientific rigor. 

Building on this foundation, we propose the **verification-aware reward model (VRM)** tailored for Reinforcement Learning with Verifiable Rewards (RLVR), which employs an adaptive reward fusion (ARF) mechanism to dynamically integrate deterministic signals from a scientific execution suite (SES) with multidimensional semantic evaluations for precise supervision. Experimental results demonstrate that our method consistently outperforms baselines and general-purpose preference models. Notably, our optimized 8B model achieves performance competitive with proprietary models, validating that incorporating verifiable, rule-based feedback into the reinforcement learning loop offers a parameter-efficient alternative to pure scaling. 

---

## 📢 News
* **[2026-04]** Paper uploaded to arXiv! Check it out [here](https://arxiv.org/abs/2604.18176).
* **[2026-04]** The QuantumQA is coming soon. 

---

## 🚀 Key Contributions

### 1. The QuantumQA Dataset
QuantumQA is a large-scale dataset comprising 92,749 samples designed for verifiable scientific reasoning. 
* **Task Diversity:** Encompasses five distinct types of tasks: Short Answer, Fill-in-the-Blank, True/False, Multiple Choice, and Problem Solving. 
* **Hybrid Verification Protocol:** Integrates deterministic verification tools via our Scientific Execution Suite (SES) with semantic auditing to guarantee scientific rigor. 
* **Task-Adaptive Construction:** Mitigates hallucination by tailoring response structures to task complexity, enforcing conciseness for simple tasks and mandating detailed Chain-of-Thought (CoT) derivations for complex reasoning. 

![Category_Distribution_Pie](assets/category_distribution_pie.png)

![Datatype_Distribution](assets/datatype_distribution.png)



### 2. Verification-Aware Reward Model (VRM)
Tailored for Reinforcement Learning with Verifiable Rewards (RLVR), our VRM effectively bridges the gap between general preference optimization and the rigorous supervision required for complex scientific reasoning. 
* Combines deterministic signals from the SES with multi-dimensional semantic evaluations (Mathematical Correctness, Physical Consistency, and Instruction Following). 
* Utilizes an **Dynamic Weight Allocation (DWA) head** to dynamically modulate supervision strength based on verifiability. 

![VRM Architecture](assets/model_arch.jpg)


## 📝 Citation

If you find our dataset or methodology helpful in your research, please consider citing our paper:

```bibtex
@misc{qu2026quantumqa,
      title={QuantumQA: Enhancing Scientific Reasoning via Physics-Consistent Dataset and Verification-Aware Reinforcement Learning}, 
      author={Songxin Qu and Tai-Ping Sun and Yun-Jie Wang and Huan-Yu Liu and Cheng Xue and Xiao-Fan Xu and Han Fang and Yang Yang and Yu-Chun Wu and Guo-Ping Guo and Zhao-Yun Chen},
      year={2026},
      eprint={2604.18176},
      archivePrefix={arXiv},
      primaryClass={cs.AI},
      url={https://arxiv.org/abs/2604.18176}, 
}
```