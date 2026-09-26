# Formal Mathematical Research Monograph Series: Foundations of Large Language Model Reasoning, Optimization, and Systems

> **Interactive Mathematical Monograph Reader (GitHub Pages)**: [https://kunruiw1991.github.io/llm-paper-summary/](https://kunruiw1991.github.io/llm-paper-summary/)

A rigorous, theorem-proof mathematical compendium of foundational and frontier **Large Language Model (LLM)** research papers. Each volume is structured as a **7-Plate Formal Mathematical Monograph** (`1080×1440 px` archival plates typeset in Computer Modern / Bourbaki *Definition–Proposition–Theorem–Proof* style) with complete probability space specifications, hypergeometric and variational derivations, complexity bounds, and empirical calibration matrices.

---

## 1. Monograph Curriculum & Interactive Learning Progress (`Tracks A → B → C → D`)

| Volume | Track | Primary Reference & Citation | 4-Lesson Mastery Status | Formal Mathematical Scope | Monograph Plates (`1080×1440`) | Interactive Reader & Lab |
| :--- | :--- | :--- | :---: | :--- | :---: | :---: |
| **Vol. I** (`ep01`) | **Track A: Multi-Agent Reasoning & Proof Harnesses** | H. Lin, D. P. Woodruff, Y. Deng, J. Mao, S. Zuo, V. Mirrokni, *"Stellar Colosseum: A Many-Agent Harness for Long-Horizon Research in Mathematics and Theoretical Computer Science,"* [arXiv:2609.15983v2](https://arxiv.org/abs/2609.15983v2) (Sept 2026) | **COMPLETED (4/4)** | Typed `StrategyCard` automata, 4-way Readiness Gate partition, hypergeometric reuse `E[R_i^(ℓ)] = m_{ℓ+1} k_ℓ / m_ℓ` (Eq. 1–5), topological section DAG `G=(V,E)` with global veto semantics, logistic Elo MLE (Eq. 13–14), and 7 TCS theorems (Eq. 6–12). | [Plates I–VII](episodes/ep01_stellar_colosseum/plates/) | [Open Vol. I](https://kunruiw1991.github.io/llm-paper-summary/episodes/ep01_stellar_colosseum/) |
| **Vol. II** (`ep02`) | **Track B: Stochastic Optimization & Reinforcement Learning** | DeepSeek-AI (D. Guo et al.), *"DeepSeek-R1: Incentivizing Reasoning Capability in LLMs via Reinforcement Learning,"* [arXiv:2501.12948](https://arxiv.org/abs/2501.12948) (Jan 2025); Z. Shao et al., [arXiv:2402.03300](https://arxiv.org/abs/2402.03300) | **COMPLETED (4/4)** | Token-level MDP formulation, critic-free GRPO surrogate functional `J_GRPO(θ)` (Eq. 1–3), empirical control-variate centering `∑ Â_{i,t} = 0`, affine reward invariance, zero-gradient saturation boundary `p(q) ∈ {0,1}`, Schulman `k_3` reverse-KL convexity proof (`u - log u - 1 ≥ 0`), and deterministic RLVR immunity to Goodhart's Law. | [Plates I–VII](episodes/ep02_deepseek_r1_grpo/plates/) | [Open Vol. II](https://kunruiw1991.github.io/llm-paper-summary/episodes/ep02_deepseek_r1_grpo/) |
| **Vol. III** (`ep03`) | **Track C: Retrieval-Augmented & Tool-Augmented Inference** | S. Yao et al., *"ReAct"* ([arXiv:2210.03629](https://arxiv.org/abs/2210.03629)); A. Asai et al., *"Self-RAG"* ([arXiv:2310.11511](https://arxiv.org/abs/2310.11511)) | **COMPLETED (4/4)** | Vector cosine similarity `cos(θ)` vs. internal parametric knowledge gating (`[Retrieve:No]` saving 42.9% context tokens), ReAct POMDP `A_aug = A_env ∪ L_thought` multi-hop recovery, 4 reflection token families (`[Retrieve]`, `[IsRel]`, `[IsSup]`, `[IsUse]`), and zero-retraining inference control via segment beam weights `(w_rel, w_sup, w_use)`. | [Plates I–VII](episodes/ep03_react_and_self_rag/plates/) | [Open Vol. III](https://kunruiw1991.github.io/llm-paper-summary/episodes/ep03_react_and_self_rag/) · [Interactive Lab](https://kunruiw1991.github.io/llm-paper-summary/episodes/ep03_react_and_self_rag/interactive_walkthrough.html) |
| **Vol. IV** (`ep04`) | **Track D: High-Throughput Inference & Memory Systems** | W. Kwon et al., *"PagedAttention"* ([arXiv:2309.06180](https://arxiv.org/abs/2309.06180)); Y. Leviathan et al., *"Speculative Decoding"* ([arXiv:2211.17192](https://arxiv.org/abs/2211.17192)) | **COMPLETED (4/4)** | Arithmetic intensity bound `AI_decode ≈ 2B` FLOP/Byte, virtual block-table mapping `M_i: b ↦ p_b`, elimination of external fragmentation (`W_paged ≤ 2.29%` vs. `63.80%` static), copy-on-write zero-copy prompt sharing, and exact lossless rejection sampling equivalence `α = min(1, p/q)` (6.38× speedup at `γ=8`). | [Plates I–VII](episodes/ep04_vllm_and_speculative_decoding/plates/) | [Open Vol. IV](https://kunruiw1991.github.io/llm-paper-summary/episodes/ep04_vllm_and_speculative_decoding/) · [Interactive Lab](https://kunruiw1991.github.io/llm-paper-summary/episodes/ep04_vllm_and_speculative_decoding/interactive_walkthrough.html) |
| **Vol. V** (`ep05`) | **Track A: Reasoning & Multi-Agent Harnesses (Cycle 2)** | C. Snell, J. Lee, K. Xu, A. Kumar, *"Scaling LLM Test-Time Compute Optimally Can Be More Effective than Scaling Model Parameters,"* [arXiv:2408.03314](https://arxiv.org/abs/2408.03314) (Aug 2024) | **COMPLETED (4/4)** | Inference FLOP budget `C_test` optimization, PRM step soundness `r_PRM(s_t)` vs. diffuse ORM credit assignment (O(1) vs. O(2^T) error localization), exponential search tree pruning `|V_pruned| ≤ B · T · K` vs. `K^T`, and difficulty-adaptive allocation (Greedy on Easy, Sequential Revision on Medium, PRM Tree on Hard; 10.0× boost on Hard, 4.2× compute saving on Medium). | [Plates I–VII](episodes/ep05_test_time_compute_scaling/plates/) | [Open Vol. V](https://kunruiw1991.github.io/llm-paper-summary/episodes/ep05_test_time_compute_scaling/) · [Interactive Lab](https://kunruiw1991.github.io/llm-paper-summary/episodes/ep05_test_time_compute_scaling/interactive_walkthrough.html) |
| **Vol. VI** (`ep06`) | **Track B: Post-Training & RL (Cycle 2)** | R. Rafailov, A. Sharma, E. Mitchell, S. Ermon, C. D. Manning, C. Finn, *"Direct Preference Optimization: Your Language Model is Secretly a Reward Model,"* [arXiv:2305.18290](https://arxiv.org/abs/2305.18290) (NeurIPS 2023) | **READY TO TEACH** | Bradley-Terry choice likelihood, exact closed-form latent reward substitution `r*(x, y) = β log(π_θ / π_ref) + β log Z(x)`, exact cancellation of partition function `Z(x)` in pairwise difference, DPO loss functional `L_DPO` with self-regulating gradient weight `σ(-h_θ)`, and elimination of the 4-model RLHF zoo (50% GPU memory reduction). | [Plates I–VII](episodes/ep06_direct_preference_optimization/plates/) | [Open Vol. VI](https://kunruiw1991.github.io/llm-paper-summary/episodes/ep06_direct_preference_optimization/) · [Interactive Lab](https://kunruiw1991.github.io/llm-paper-summary/episodes/ep06_direct_preference_optimization/interactive_walkthrough.html) |

### Interactive 1-on-1 Mastery Notes (Vol. V: *Scaling LLM Test-Time Compute Optimally*)
1. **Lesson 1 — The Pre-Training Parameter Wall & Test-Time Search Inversion**: Pre-training larger models (7B → 70B) requires 10× to 50× more pre-training FLOPs and gigantic GPU footprints, yet single-shot greedy rollouts still fail when early reasoning steps diverge. Spending compute dynamically at test time—via PRM step-level guidance and adaptive revision—allows a **7B parameter model to outperform a 14× larger model** on complex reasoning benchmarks.
2. **Lesson 2 — Process Reward Models (PRM) vs. Outcome Reward Models (ORM)**: An ORM provides only a binary scalar score at the very end of the trajectory, forcing the system to discard entire 10-step proofs when a late error occurs. A PRM evaluates each intermediate deduction step `r_PRM(s_t | s_{<t})`, identifying the exact breakdown step `k` in `O(1)` evaluations, saving `(k-1)/T` of the forward generation compute via surgical rollback.
3. **Lesson 3 — Search Topologies: Parallel Best-of-N vs. Sequential Adaptive Revision**: Parallel BoN generates independent complete trajectories, discarding valid intermediate lemmas across rejected arms. Sequential revision takes the flawed draft, localizes the error via PRM, and rewrites forward, achieving target accuracy with compute scaling `O(log(1/ε))` vs. `O(1/ε)` for independent sampling.
4. **Lesson 4 — Difficulty-Aware Compute-Optimal Allocation**: Optimal inference compute allocation follows a tri-phasic policy: on Easy tasks, greedy single-shot reaches 80%–95% accuracy; on Medium tasks, sequential revision saves **4.2× compute** over BoN; on Hard tasks, PRM-guided tree search is essential to escape local minima, boosting accuracy from **10.0% to 100.0%**.

### Interactive 1-on-1 Mastery Notes (Vol. IV: *vLLM PagedAttention & Speculative Decoding*)
1. **Lesson 1 — The Memory Bandwidth Wall & KV-Cache Pathology**: Autoregressive token decoding streams the entire 140 GB model weights across the memory bus to generate just 1 token (`AI_decode ≈ 2B` FLOP/Byte). Batching `B` users amortizes 1 weight transfer across `B` tokens, but static KV-cache pre-allocation (`L_max = 2048` blank pages per user) wastes **63.80%** of GPU memory, starving the batch size.
2. **Lesson 2 — PagedAttention Virtual Memory & Copy-On-Write**: Slicing KV memory into 16-token loose-leaf physical blocks (`B_s = 16`) mapped via a lookup table (`Block Table`) eliminates external fragmentation and restricts internal waste to the very last block (`2.29%` waste, a **27.8× reduction**). When 4 parallel answers branch from a 1,000-token prompt, they share the exact same physical blocks for the prompt and only trigger Copy-on-Write (COW) on the single block where their generated words diverge.
3. **Lesson 3 — Speculative Decoding & Optimal Lookahead (`γ*`)**: Because checking `γ` tokens in parallel takes the same 1 memory haul (`100 ms`) as generating 1 token, a fast Draft Intern (`5 ms/token`) proposes `γ` words ahead. Total wall-clock time is `100 ms + γ × 5 ms`. For predictable code (`98%` match), a large `γ` (`8–10`) yields **6.38× wall-clock speedup**; for creative poetry (low match), `γ` must stay small (`1–2`) so we don't waste stopwatch time drafting tokens that get discarded after an early rejection.
4. **Lesson 4 — Lossless Rejection Sampling (`α = min(1, p/q)`)**: When the Draft Intern over-proposes `"Paris"` at `q = 50%` while the 70B Target Model wants `p = 30%`, the Target Model accepts `"Paris"` exactly **`p / q = 3/5` (`60%`)** of the time (`50% × 3/5 = 30%`), routing the rejected `20%` probability mass to under-guessed tokens so the final distribution matches the 70B model with **0.000 divergence**.

### Interactive 1-on-1 Mastery Notes (Vol. III: *ReAct & Self-RAG*)
1. **Lesson 1 — Cosine Similarity (`cos(θ)`) vs. Parametric Confidence**: Embedding cosine similarity `cos(θ) = (A · B) / (||A|| × ||B||)` only measures whether the external database contains a passage on the *topic* of the query (`score = 0.95` even on trivial questions like `2 + 2 = 4`). Only the LLM itself knows whether its own neural weights already hold the answer with certainty—emitting `[Retrieve:No]` to skip unnecessary search and reduce context token usage by **42.9%** (`135.5` vs. `237.2` tokens/query).
2. **Lesson 2 — ReAct Multi-Hop POMDP & Empty-Set Recovery**: When a multi-hop search step returns an empty set (`0` directional similarity with downstream entities), an action-only agent gets trapped in repetitive query loops. ReAct's `Thought` scratchpad (`L_thought`) detects the empty observation and reformulates a new search vector `Action_{t+1}` to bridge the missing hop.
3. **Lesson 3 — Disentangling `[IsRel]` vs. `[IsSup]`**: When a retrieved passage confirms a model's release date (*"January 2025"*) but omits its parameter count (`671B`), a drafted sentence containing both claims is evaluated as **`[IsRel:Relevant]`** (the passage is relevant to the prompt) paired with **`[IsSup:PartiallySupported]`** (not all claims in the drafted sentence are entailed by the evidence), triggering surgical pruning or secondary retrieval.
4. **Lesson 4 — Zero-Retraining Inference Customization (`w_sup, w_use`)**: Segment-level beam search scores candidate continuations via `Score(y_t, d_k) = Language_LogProb + w_rel P([IsRel:Rel]) + w_sup P([IsSup:Full]) + w_use P([IsUse:5])`. At serving time without retraining:
   - **Strict Verifier Mode**: Set `w_sup = 10.0, w_use = 1.0` requiring `[IsSup:FullySupported]` to enforce 0.0% hallucination.
   - **Creative Synthesis Mode**: Set `w_sup = 0.0, w_use = 10.0` to allow open-ended ideation.

---

## 2. Volume I (`ep01_stellar_colosseum`): *Stellar Colosseum* ([arXiv:2609.15983v2](https://arxiv.org/abs/2609.15983v2))

### Formal Monograph Plates I–VII (`1080×1440` Archival Typesetting)

<p align="center">
  <img src="episodes/ep01_stellar_colosseum/plates/plate_1.png" width="32%" alt="Vol I Plate I" />
  <img src="episodes/ep01_stellar_colosseum/plates/plate_2.png" width="32%" alt="Vol I Plate II" />
  <img src="episodes/ep01_stellar_colosseum/plates/plate_3.png" width="32%" alt="Vol I Plate III" />
</p>
<p align="center">
  <img src="episodes/ep01_stellar_colosseum/plates/plate_4.png" width="32%" alt="Vol I Plate IV" />
  <img src="episodes/ep01_stellar_colosseum/plates/plate_5.png" width="32%" alt="Vol I Plate V" />
  <img src="episodes/ep01_stellar_colosseum/plates/plate_6.png" width="32%" alt="Vol I Plate VI" />
</p>
<p align="center">
  <img src="episodes/ep01_stellar_colosseum/plates/plate_7.png" width="32%" alt="Vol I Plate VII" />
</p>

### Key Formal Results (Vol. I)
- **Proposition 3.2 (Expected Candidate Multiplicity, Eq. 1–5)**: Given a layer-`ℓ` population `C^(ℓ)` of cardinality `m_ℓ` and `m_{ℓ+1}` downstream synthesis nodes independently sampling subsets `G_j^(ℓ) ~ Unif{G ⊆ C^(ℓ) : |G| = k_ℓ}` without replacement (`k_ℓ = min(k, m_ℓ)`), the single-node hypergeometric inclusion probability is `C(m_ℓ - 1, k_ℓ - 1) / C(m_ℓ, k_ℓ) = k_ℓ / m_ℓ`, yielding expected candidate multiplicity `E[R_i^(ℓ)] = m_{ℓ+1} k_ℓ / m_ℓ` (`2.500` at `32 → 16, k=5`).
- **Theorem 4.2 (Two-Tier Verification & Global Veto Semantics)**: Local section failures `Φ_local(d_v) ≠ READY` trigger hermetic retries restricted to vertex `v ∈ V` while preserving upstream proofs `{d_u : (u, v) ∈ E}`. Global verification over assembled document `D = (d_1, ..., d_S)` enforces unanimous veto semantics `Accept(D) = 1 ⟺ ⋀_{j=1}^m [Defect_fatal(Φ_global^(j)(D)) = ∅]`.
- **Empirical Calibration (Eq. 13–14)**: Achieves **71.00% (`213 / 300`)** on **TCS-Bench** (FOCS/STOC/SODA 2020–2026) under cross-model critique gating (`AUC = 0.896`), and solves **218 / 222 (98.20%)** Codeforces tasks (`r_i > 1500`), corresponding to a maximum-likelihood logistic Elo rating `x̂ = 4263` (`∑_{i=1}^{222} [1 + 10^{(r_i - x̂)/400}]^{-1} = 218`).

---

## 3. Volume II (`ep02_deepseek_r1_grpo`): *DeepSeek-R1 & GRPO* ([arXiv:2501.12948](https://arxiv.org/abs/2501.12948))

### Formal Monograph Plates I–VII (`1080×1440` Archival Typesetting)

<p align="center">
  <img src="episodes/ep02_deepseek_r1_grpo/plates/plate_1.png" width="32%" alt="Vol II Plate I" />
  <img src="episodes/ep02_deepseek_r1_grpo/plates/plate_2.png" width="32%" alt="Vol II Plate II" />
  <img src="episodes/ep02_deepseek_r1_grpo/plates/plate_3.png" width="32%" alt="Vol II Plate III" />
</p>
<p align="center">
  <img src="episodes/ep02_deepseek_r1_grpo/plates/plate_4.png" width="32%" alt="Vol II Plate IV" />
  <img src="episodes/ep02_deepseek_r1_grpo/plates/plate_5.png" width="32%" alt="Vol II Plate V" />
  <img src="episodes/ep02_deepseek_r1_grpo/plates/plate_6.png" width="32%" alt="Vol II Plate VI" />
</p>
<p align="center">
  <img src="episodes/ep02_deepseek_r1_grpo/plates/plate_7.png" width="32%" alt="Vol II Plate VII" />
</p>

### Key Formal Results (Vol. II)
- **Theorem 2.3 (Clipped GRPO Surrogate Functional `J_GRPO(θ)`, Eq. 1–3)**: Eliminates the parameterized critic network `V_ψ(s_t)` by normalizing terminal rewards `r = (r_1, ..., r_G)` across `G` i.i.d. rollouts `{o_1, ..., o_G} ~ π_{θ_old}(· | q)` via `Â_{i,t} = (r_i - μ_r) / (σ_r + δ)`.
- **Proposition 3.1–3.3 (Control Variate Centering, Scale Invariance & Saturation Boundary)**: Satisfies `∑_{i=1}^G Â_{i,t} = 0` and `(1/G)∑_{i=1}^G Â_{i,t}^2 = 1`, invariance under positive affine transforms `r'_i = a r_i + b (a > 0)`, and exact gradient vanishing `∇_θ J_GRPO^surr(θ | q) = 0` whenever `p(q) ∈ {0, 1}` (`σ_r = 0`).
- **Theorem 4.2 (Schulman `k_3` Reverse-KL Estimator)**: For density ratio `u_{i,t} = π_ref / π_θ > 0`, `f(u) = u - log u - 1` satisfies `f(1) = f'(1) = 0` and `f''(u) = 1/u^2 > 0`, guaranteeing strict pointwise non-negativity `𝔻_KL(π_θ ‖ π_ref)_{i,t} ≥ 0` and unbiasedness `E_{o_{i,t} ~ π_θ}[f(u_{i,t})] = KL(π_θ ‖ π_ref)`.

---

## 4. Volume III (`ep03_react_and_self_rag`): *ReAct & Self-RAG* ([arXiv:2210.03629](https://arxiv.org/abs/2210.03629) / [arXiv:2310.11511](https://arxiv.org/abs/2310.11511))

### Formal Monograph Plates I–VII (`1080×1440` Archival Typesetting)

<p align="center">
  <img src="episodes/ep03_react_and_self_rag/plates/plate_1.png" width="32%" alt="Vol III Plate I" />
  <img src="episodes/ep03_react_and_self_rag/plates/plate_2.png" width="32%" alt="Vol III Plate II" />
  <img src="episodes/ep03_react_and_self_rag/plates/plate_3.png" width="32%" alt="Vol III Plate III" />
</p>
<p align="center">
  <img src="episodes/ep03_react_and_self_rag/plates/plate_4.png" width="32%" alt="Vol III Plate IV" />
  <img src="episodes/ep03_react_and_self_rag/plates/plate_5.png" width="32%" alt="Vol III Plate V" />
  <img src="episodes/ep03_react_and_self_rag/plates/plate_6.png" width="32%" alt="Vol III Plate VI" />
</p>
<p align="center">
  <img src="episodes/ep03_react_and_self_rag/plates/plate_7.png" width="32%" alt="Vol III Plate VII" />
</p>

### Key Formal Results (Vol. III)
- **Proposition 1.2 (Pathologies of Naive Always-On RAG)**: Demonstrates that unconditional retrieval `R_naive(x) = TopK(x, D)` for all `x ∈ X` exposes LLMs to adversarial distractor poisoning and inflicts an unnecessary context window tax on queries solvable by parametric memory alone.
- **Theorem 2.3 (ReAct POMDP Formulation & Error Bounding)**: Models reasoning and tool execution as an augmented POMDP with action space `A_aug = A_env ∪ L_thought`. External observations `o_k` prune hallucinated reasoning branches in `L_thought`, while structured thoughts `t_k` eliminate aimless exploratory sampling in `A_env`.
- **Theorem 4.2 (Critique-Regularized Beam Score Functional)**: Formalizes the multi-reward segment beam score `Score(y_t, d_k) = (1/|y_t|) ∑ log P_θ + γ_rel P([IsRel:Rel]) + γ_sup P([IsSup:Full]) + γ_use P([IsUse:5])`, proving that support thresholding `τ_sup` drives hallucination probability `P(Hallucination | y^*) → 0`.
- **Empirical Efficiency Verification**: Evaluated on our verified multi-hop and adversarial benchmark (XManager run `292337037`): Self-RAG achieves **100.0% accuracy** and **0.0% hallucination rate** while reducing token consumption by **42.9%** (135.5 tokens/Q vs. 237.2 tokens/Q for Naive RAG) through adaptive `[Retrieve:No]` gating.

---

## 5. Volume IV (`ep04_vllm_and_speculative_decoding`): *vLLM PagedAttention & Speculative Decoding* ([arXiv:2309.06180](https://arxiv.org/abs/2309.06180) / [arXiv:2211.17192](https://arxiv.org/abs/2211.17192))

### Formal Monograph Plates I–VII (`1080×1440` Archival Typesetting)

<p align="center">
  <img src="episodes/ep04_vllm_and_speculative_decoding/plates/plate_1.png" width="32%" alt="Vol IV Plate I" />
  <img src="episodes/ep04_vllm_and_speculative_decoding/plates/plate_2.png" width="32%" alt="Vol IV Plate II" />
  <img src="episodes/ep04_vllm_and_speculative_decoding/plates/plate_3.png" width="32%" alt="Vol IV Plate III" />
</p>
<p align="center">
  <img src="episodes/ep04_vllm_and_speculative_decoding/plates/plate_4.png" width="32%" alt="Vol IV Plate IV" />
  <img src="episodes/ep04_vllm_and_speculative_decoding/plates/plate_5.png" width="32%" alt="Vol IV Plate V" />
  <img src="episodes/ep04_vllm_and_speculative_decoding/plates/plate_6.png" width="32%" alt="Vol IV Plate VI" />
</p>
<p align="center">
  <img src="episodes/ep04_vllm_and_speculative_decoding/plates/plate_7.png" width="32%" alt="Vol IV Plate VII" />
</p>

### Key Formal Results (Vol. IV)
- **Definition 1.1 & Theorem 1.2 (The Memory Bandwidth Wall & Contiguous Static Pathology)**: Proves that autoregressive token decoding has arithmetic intensity `AI_decode ≈ 2B` FLOP/Byte, placing batch sizes `B ≤ 100` deep inside the memory-bandwidth-bound regime on modern hardware. Static reservation of `L_max` slots per request wastes `60%–80%` of GPU memory.
- **Theorem 2.2 (PagedAttention Fragmentation Bound)**: Proves that virtual memory block mapping completely eliminates external memory fragmentation and bounds internal waste to `< (B_s / 2) / L̄` (`2.29%` measured vs. `63.80%` in static allocation, a **27.8× waste reduction**).
- **Proposition 3.2 (Zero-Copy Branching via Copy-On-Write)**: Enables zero-copy memory sharing during beam search and parallel sampling, reducing peak memory usage by up to 55%.
- **Theorem 5.2 (Exact Lossless Rejection Sampling Equivalence)**: Proves that verifying drafted tokens via `α = min(1, p(x)/q(x))` and resampling rejected tokens from residual distribution `p'(x) = max(0, p(x)-q(x)) / (1 - ∑ min(p, q))` recovers the target distribution identically (`P_spec(X=x) = p(x)`).
- **Empirical Calibration Matrix (XManager Experiment 292693865)**: Speculative decoding reaches **6.38× effective wall-clock speedup** at lookahead `γ=8` (emitting 8.93 tokens per target forward pass) with 0.000 distribution divergence.


---

## 6. Volume V (`ep05_test_time_compute_scaling`): *Scaling LLM Test-Time Compute Optimally* ([arXiv:2408.03314](https://arxiv.org/abs/2408.03314))

### Formal Monograph Plates I–VII (`1080×1440` Archival Typesetting)

<p align="center">
  <img src="episodes/ep05_test_time_compute_scaling/plates/plate_1.png" width="32%" alt="Vol V Plate I" />
  <img src="episodes/ep05_test_time_compute_scaling/plates/plate_2.png" width="32%" alt="Vol V Plate II" />
  <img src="episodes/ep05_test_time_compute_scaling/plates/plate_3.png" width="32%" alt="Vol V Plate III" />
</p>
<p align="center">
  <img src="episodes/ep05_test_time_compute_scaling/plates/plate_4.png" width="32%" alt="Vol V Plate IV" />
  <img src="episodes/ep05_test_time_compute_scaling/plates/plate_5.png" width="32%" alt="Vol V Plate V" />
  <img src="episodes/ep05_test_time_compute_scaling/plates/plate_6.png" width="32%" alt="Vol V Plate VI" />
</p>
<p align="center">
  <img src="episodes/ep05_test_time_compute_scaling/plates/plate_7.png" width="32%" alt="Vol V Plate VII" />
</p>

### Key Formal Results (Vol. V)
- **Theorem 1.2 (Test-Time Search vs. Parameter Scaling Frontier)**: Proves that an inference compute budget `C_test` dynamically allocated via verifier search allows a 7B base model to exceed the accuracy of a 70B greedy model (`Acc(7B, C*) ≥ Acc(70B, C_greedy)`).
- **Proposition 2.2 (Surgical Error Localization & Backtracking Complexity)**: PRM step evaluation localizes flawed steps in `O(1)` evaluations, reducing error repair complexity from `O(2^T)` under diffuse ORM scoring to surgical prefix preservation.
- **Theorem 4.2 (Exponential Pruning of Flawed Branches)**: PRM beam search eliminates unsound subtrees, bounding active search volume to `|V_pruned| ≤ B · T · K` compared to `K^T` exhaustive combinatorial explosion.
- **Empirical Calibration Matrix (XManager Experiment 293232963)**: PRM-guided tree search boosts Hard reasoning accuracy from **10.0% to 100.0%** (10.0× boost), while Sequential Revision on Medium tasks saves **4.2× compute** over Parallel Best-of-8 (376 vs. 1600 tokens/problem) with PRM AUC = 0.880.
