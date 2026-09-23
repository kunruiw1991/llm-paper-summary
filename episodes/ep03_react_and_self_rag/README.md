# Volume III (`ep03_react_and_self_rag`): *ReAct & Self-RAG* ([arXiv:2210.03629](https://arxiv.org/abs/2210.03629) / [arXiv:2310.11511](https://arxiv.org/abs/2310.11511))

- **Primary Citations**:
  1. S. Yao et al., *"ReAct: Synergizing Reasoning and Acting in Language Models,"* `arXiv:2210.03629`, ICLR 2023. ([https://arxiv.org/abs/2210.03629](https://arxiv.org/abs/2210.03629))
  2. A. Asai et al., *"Self-RAG: Learning to Retrieve, Generate, and Critique through Self-Reflection,"* `arXiv:2310.11511`, ICLR 2024. ([https://arxiv.org/abs/2310.11511](https://arxiv.org/abs/2310.11511))
- **Interactive Monograph Reader**: [https://kunruiw1991.github.io/llm-paper-summary/episodes/ep03_react_and_self_rag/](https://kunruiw1991.github.io/llm-paper-summary/episodes/ep03_react_and_self_rag/)
- **Interactive Visual Walkthrough**: [https://kunruiw1991.github.io/llm-paper-summary/episodes/ep03_react_and_self_rag/interactive_walkthrough.html](https://kunruiw1991.github.io/llm-paper-summary/episodes/ep03_react_and_self_rag/interactive_walkthrough.html)
- **Results & Telemetry Dashboard**: [https://kunruiw1991.github.io/llm-paper-summary/episodes/ep03_react_and_self_rag/xm_results_dashboard.html](https://kunruiw1991.github.io/llm-paper-summary/episodes/ep03_react_and_self_rag/xm_results_dashboard.html)

---

## Formal Mathematical Monograph Plates (I–VII)

| Plate | Archival Plate (`1080×1440`) | Formal Mathematical Contents |
| :---: | :---: | :--- |
| **Plate I** | <img src="plates/plate_1.png" width="280" /> | **§1.0. Parametric vs. Non-Parametric Memory & Naive RAG Failure Modes**: The dual knowledge formulation `P(y \| x) = P_θ(y \| x, D)`, Proposition 1.2 (Adversarial distractor poisoning, parametric redundancy tax, and multi-hop disconnection in unconditional static retrieval). |
| **Plate II** | <img src="plates/plate_2.png" width="280" /> | **§2.0. ReAct: POMDP Formalism & Augmented Action Space**: Augmented action space `A_aug = A_env ∪ L_thought` (Eq. 2.1), external environment observations `o_t ~ O(s_t)`, and Theorem 2.3 (Synergistic error bounding between internal reasoning steps and external tool actions). |
| **Plate III** | <img src="plates/plate_3.png" width="280" /> | **§3.0. Self-RAG: Reflection Token Taxonomy & Critic Distillation**: Vocabulary extension `V_aug = V ∪ Γ` with 4 token families: `[Retrieve]`, `[IsRel]`, `[IsSup]`, and `[IsUse]` (Eq. 3.1), and dual-model critic-generator distillation via supervised fine-tuning. |
| **Plate IV** | <img src="plates/plate_4.png" width="280" /> | **§3.2. Segment-Level Beam Search & Multi-Reward Decoding**: Segment boundary evaluation, the critique-regularized beam score functional `Score(y_t, d_k)` (Eq. 4.1), and mathematical proof of hallucination suppression via support thresholding `τ_sup`. |
| **Plate V** | <img src="plates/plate_5.png" width="280" /> | **§4.0. Multi-Hop Deduction & Adversarial Distractor Immunity**: Proposition 5.1 (Asymmetric distractor susceptibility), verification under adversarial poisoning, and test-case comparison across parametric invariants, multi-hop chains, and poisoned passages. |
| **Plate VI** | <img src="plates/plate_6.png" width="280" /> | **§5.0. Empirical Benchmark Scoreboard & Token Efficiency Frontiers**: Head-to-head empirical results (Vanilla vs. Naive RAG vs. ReAct vs. Self-RAG), 42.9% context token reduction via `[Retrieve:No]`, and zero hallucination Pareto dominance. |
| **Plate VII** | <img src="plates/plate_7.png" width="280" /> | **§6.0. Systems Architecture & Production Trade-Offs**: Speculative critique decoding for low-latency serving (Eq. 7.1), asynchronous candidate pre-filtering, KV-cache footprint management, and the future of agentic RAG. |

---

## Benchmark Scoreboard Summary

| Paradigm | Accuracy | Hallucination Rate | Retrievals / Q | Avg Tokens / Q | Unnecessary Ret% |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **Vanilla (No RAG)** | 25.0% | 75.0% | 0.00 | 85.0 | 0.0% |
| **Naive (Always-On RAG)** | 87.5% | 12.5% | 1.00 | 237.2 | 25.0% |
| **ReAct (Interleaved Trace)** | **100.0%** | **0.0%** | 0.88 | 174.8 | **0.0%** |
| **Self-RAG (Reflection Tokens)** | **100.0%** | **0.0%** | **0.75** | **135.5** | **0.0%** |
