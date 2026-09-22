# Volume II (`ep02_deepseek_r1_grpo`): *DeepSeek-R1 & GRPO* ([arXiv:2501.12948](https://arxiv.org/abs/2501.12948))

- **Primary Citations**:
  1. DeepSeek-AI (D. Guo et al.), *"DeepSeek-R1: Incentivizing Reasoning Capability in LLMs via Reinforcement Learning,"* `arXiv:2501.12948`, January 2025. ([https://arxiv.org/abs/2501.12948](https://arxiv.org/abs/2501.12948))
  2. Z. Shao et al., *"DeepSeekMath: Pushing the Limits of Mathematical Reasoning in Open Language Models,"* `arXiv:2402.03300`, February 2024. ([https://arxiv.org/abs/2402.03300](https://arxiv.org/abs/2402.03300))
- **Interactive Monograph Reader**: [https://kunruiw1991.github.io/rednote-llm-paper-summary/episodes/ep02_deepseek_r1_grpo/](https://kunruiw1991.github.io/rednote-llm-paper-summary/episodes/ep02_deepseek_r1_grpo/)

---

## Formal Mathematical Monograph Plates (I–VII)

| Plate | Archival Plate (`1080×1440`) | Formal Mathematical Contents |
| :---: | :---: | :--- |
| **Plate I** | <img src="cards/rednote_card_1.png" width="280" /> | **§1. Autoregressive Token MDP & Actor-Critic Obstructions**: Token trajectory generation `o ~ π_θ(· | q)` and Proposition 1.2 (Memory doubling and intermediate GAE credit-assignment variance of learned critic `V_ψ(s_t)` in PPO). |
| **Plate II** | <img src="cards/rednote_card_2.png" width="280" /> | **§2.1.1. The GRPO Surrogate Functional `J_GRPO(θ)` (Eq. 1–3)**: Group rollout sampling `{o_1, ..., o_G} ~ π_{θ_old}(· | q)`, token importance ratio `ρ_{i,t}(θ)`, trajectory-broadcast z-score advantage `Â_{i,t} = (r_i - μ_r)/(σ_r + δ)`, and per-trajectory length normalization `1/|o_i|`. |
| **Plate III** | <img src="cards/rednote_card_3.png" width="280" /> | **§2.1.1. Statistical Invariants & Boundary Degeneracy**: Formal proofs of exact empirical control-variate centering (`∑_{i=1}^G Â_{i,t} = 0`), positive affine reward invariance (`r'_i = a r_i + b`), and zero-gradient saturation (`p(q) ∈ {0, 1} ⟹ σ_r = 0 ⟹ ∇_θ J_GRPO = 0`). |
| **Plate IV** | <img src="cards/rednote_card_4.png" width="280" /> | **§2.1.1. Schulman `k_3` Reverse-KL Estimator (Eq. 2)**: Pointwise non-negativity and unbiasedness proof of `𝔻_KL(π_θ ‖ π_ref)_{i,t} = u_{i,t} - log u_{i,t} - 1 ≥ 0` (`u_{i,t} = π_ref / π_θ`) via strict convexity `f''(u) = 1/u^2 > 0`. |
| **Plate V** | <img src="cards/rednote_card_5.png" width="280" /> | **§2.1.2 & §2.2. Rule-Based Verifiable Rewards (`RLVR`)**: Deterministic symbolic/execution reward `R(q, o) = R_acc(q, o) + λ_fmt R_fmt(o)`, immunity to Goodhart's Law reward hacking, and emergent test-time compute scaling (`15.6% → 71.0% pass@1` on AIME 2024). |
| **Plate VI** | <img src="cards/rednote_card_6.png" width="280" /> | **§2.3 & §2.4. Four-Stage DeepSeek-R1 Pipeline & Dense Distillation**: Language-consistency reward `R_lang(o)`, Cold-Start SFT → Reasoning GRPO → Rejection-Sampled SFT (`800k`) → All-Scenario RL, and distillation superiority (`72.6%` vs `47.0%` scratch RL on Qwen-32B). |
| **Plate VII** | <img src="cards/rednote_card_7.png" width="280" /> | **§3.1–§3.2. Empirical Benchmark Verification Matrix**: Full comparison across DeepSeek-V3-Base, OpenAI o1-1217, DeepSeek-R1-Zero, DeepSeek-R1 (`79.8%` AIME 2024, `97.3%` MATH-500, `2029` Codeforces Elo), and distilled checkpoints. |
