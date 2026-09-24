# Volume IV (`ep04_vllm_and_speculative_decoding`): *vLLM PagedAttention & Speculative Decoding* ([arXiv:2309.06180](https://arxiv.org/abs/2309.06180) / [arXiv:2211.17192](https://arxiv.org/abs/2211.17192))

- **Primary Citations**:
  1. W. Kwon et al., *"Efficient Memory Management for Large Language Model Serving with PagedAttention,"* `arXiv:2309.06180`, SOSP 2023. ([https://arxiv.org/abs/2309.06180](https://arxiv.org/abs/2309.06180))
  2. Y. Leviathan, M. Kalman, Y. Matias, *"Fast Inference from Transformers via Speculative Decoding,"* `arXiv:2211.17192`, ICML 2023. ([https://arxiv.org/abs/2211.17192](https://arxiv.org/abs/2211.17192))
- **Interactive Monograph Reader**: [https://kunruiw1991.github.io/llm-paper-summary/episodes/ep04_vllm_and_speculative_decoding/](https://kunruiw1991.github.io/llm-paper-summary/episodes/ep04_vllm_and_speculative_decoding/)
- **Interactive Visual Walkthrough**: [https://kunruiw1991.github.io/llm-paper-summary/episodes/ep04_vllm_and_speculative_decoding/interactive_walkthrough.html](https://kunruiw1991.github.io/llm-paper-summary/episodes/ep04_vllm_and_speculative_decoding/interactive_walkthrough.html)
- **Results & Telemetry Dashboard**: [https://kunruiw1991.github.io/llm-paper-summary/episodes/ep04_vllm_and_speculative_decoding/xm_results_dashboard.html](https://kunruiw1991.github.io/llm-paper-summary/episodes/ep04_vllm_and_speculative_decoding/xm_results_dashboard.html)

---

## Formal Mathematical Monograph Plates (I–VII)

| Plate | Archival Plate (`1080×1440`) | Formal Mathematical Contents |
| :---: | :---: | :--- |
| **Plate I** | <img src="plates/plate_1.png" width="280" /> | **§1.0. Foundational Memory Physics & The Memory Bandwidth Wall**: Arithmetic intensity of autoregressive generation `AI_decode ≈ 2B` [FLOP/Byte] (Eq. 1.1), memory-bound regime on modern accelerators, and Theorem 1.2 (Pathology and 60%–80% waste under contiguous static allocation). |
| **Plate II** | <img src="plates/plate_2.png" width="280" /> | **§2.0. PagedAttention: Virtual Memory Mapping of KV Tensors**: Partitioning sequence positions into physical blocks of size `B_s` (Eq. 2.1), block table indirection `M_i: b ↦ p_b`, and Theorem 2.2 (Elimination of external fragmentation, bounding internal waste to `< 4%`). |
| **Plate III** | <img src="plates/plate_3.png" width="280" /> | **§3.0. Non-Contiguous Attention Gathering & Copy-On-Write**: Paged attention gathering kernel formulation (Eq. 3.1–3.2), and Proposition 3.2 (Zero-copy branching via copy-on-write during beam search and parallel sampling, saving up to 55% memory). |
| **Plate IV** | <img src="plates/plate_4.png" width="280" /> | **§4.0. Speculative Decoding: Two-Model Asymmetric Formulation**: Draft model `M_draft` proposing `γ` tokens autoregressively (Eq. 4.1), and Theorem 4.2 (Parallel verification complexity: computing `γ+1` target distributions in a single forward pass with `T_verify ≈ T_target`). |
| **Plate V** | <img src="plates/plate_5.png" width="280" /> | **§5.0. Exact Lossless Rejection Sampling Theorem**: Exact acceptance probability `α_i = min(1, p(x)/q(x))` (Eq. 5.1), normalized residual distribution `p'(x)` (Eq. 5.2), and Theorem 5.2 (Rigorous proof of exact distributional equivalence `P_spec(X=x) = p(x)`). |
| **Plate VI** | <img src="plates/plate_6.png" width="280" /> | **§6.0. Theoretical Speedup & Horizon Optimization (γ*)**: Expected accepted tokens `E[N] = (1 - β^{γ+1}) / (1 - β)` (Eq. 6.1), Amdahl wall-clock speedup functional `S(γ)` (Eq. 6.2), and Corollary 6.2 (Optimal lookahead horizon derivation). |
| **Plate VII** | <img src="plates/plate_7.png" width="280" /> | **§7.0. Empirical Calibration Matrix & Serving Synergy**: Validated benchmark results from XManager experiment `292693865` (Paged memory waste reduced from 63.80% to 2.29%; speculative speedup reaching 6.38× at `γ=8` with zero distribution divergence). |

---

## Benchmark Scoreboard Summary

### Part 1: KV-Cache Memory Management

| Architecture | Memory Waste % | Internal Frag % | External Frag % | Max Concurrency | Batch Throughput |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **Contiguous Static** | 63.80% | 45.8% | 18.0% | 8 reqs | 84.0 tok/s |
| **vLLM PagedAttention** | **2.29%** | **2.29%** | **0.00%** | **8 reqs** | **84.0 tok/s** |

### Part 2: Speculative Decoding Speedup vs. Horizon γ

| Decoding Mode | Lookahead γ | Tokens / Forward Pass | Acceptance Rate | Effective Speedup | Exact Distribution Match |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **Standard Autoregressive** | 0 | 1.00 | 100.0% | 1.00× | True |
| **Speculative Decoding** | 1 | 1.94 | 93.9% | 1.85× | True |
| **Speculative Decoding** | 2 | 2.95 | 97.7% | 2.69× | True |
| **Speculative Decoding** | 4 | 4.71 | 92.9% | 3.93× | True |
| **Speculative Decoding** | 6 | 6.45 | 90.8% | 4.96× | True |
| **Speculative Decoding** | **8** | **8.93** | **99.2%** | **6.38×** | **True** |
