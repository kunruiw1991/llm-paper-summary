# Volume V (`ep05_test_time_compute_scaling`): *Scaling LLM Test-Time Compute Optimally* ([arXiv:2408.03314](https://arxiv.org/abs/2408.03314))

- **Primary Citation**: C. Snell, J. Lee, K. Xu, A. Kumar, *"Scaling LLM Test-Time Compute Optimally Can Be More Effective than Scaling Model Parameters,"* `arXiv:2408.03314`, UC Berkeley & Google DeepMind, August 2024. ([https://arxiv.org/abs/2408.03314](https://arxiv.org/abs/2408.03314))
- **Interactive Monograph Reader**: [https://kunruiw1991.github.io/llm-paper-summary/episodes/ep05_test_time_compute_scaling/](https://kunruiw1991.github.io/llm-paper-summary/episodes/ep05_test_time_compute_scaling/)
- **Interactive Visual Walkthrough**: [https://kunruiw1991.github.io/llm-paper-summary/episodes/ep05_test_time_compute_scaling/interactive_walkthrough.html](https://kunruiw1991.github.io/llm-paper-summary/episodes/ep05_test_time_compute_scaling/interactive_walkthrough.html)
- **Results & Telemetry Dashboard**: [https://kunruiw1991.github.io/llm-paper-summary/episodes/ep05_test_time_compute_scaling/xm_results_dashboard.html](https://kunruiw1991.github.io/llm-paper-summary/episodes/ep05_test_time_compute_scaling/xm_results_dashboard.html)

---

## Formal Mathematical Monograph Plates (I–VII)

| Plate | Archival Plate (`1080×1440`) | Formal Mathematical Contents |
| :---: | :---: | :--- |
| **Plate I** | <img src="plates/plate_1.png" width="280" /> | **§1.0. Formulation of the Test-Time Inference Frontier**: Inference FLOP budget `C_test` definition (Eq. 1.1), and Theorem 1.2 (Test-Time Search vs. Parameter Scaling: `Acc(7B, C*) ≥ Acc(70B, C_greedy)` on complex reasoning). |
| **Plate II** | <img src="plates/plate_2.png" width="280" /> | **§2.0. Step-Level Credit Assignment (PRM vs. ORM)**: PRM step soundness formulation `r_PRM(s_t)` (Eq. 2.1), Proposition 2.2 (Surgical error localization in `O(1)` vs. `O(2^T)` diffuse ORM backtracking, saving `(k-1)/T` prefix compute). |
| **Plate III** | <img src="plates/plate_3.png" width="280" /> | **§3.0. Search Paradigms (Parallel BoN vs. Sequential Revision)**: Parallel `ŷ_BoN` (Eq. 3.1), sequential critique revision `y_{(m)}` (Eq. 3.2), and Theorem 3.3 (`O(log(1/ε))` compute scaling of revision vs. `O(1/ε)` for independent sampling). |
| **Plate IV** | <img src="plates/plate_4.png" width="280" /> | **§4.0. Step-Level Beam & Tree Search**: Search tree `T = (V, E)` with edge transitions `w(v → v')` (Eq. 4.1), and Theorem 4.2 (Exponential pruning reducing `K^T` exhaustive branches to `O(B · T · K)`). |
| **Plate V** | <img src="plates/plate_5.png" width="280" /> | **§5.0. Difficulty-Aware Optimal Compute Allocation**: Optimal allocation functional `M*(x, C)` (Eq. 5.1), and Theorem 5.2 (Tri-phasic regime: Greedy on Easy, Sequential Revision on Medium, PRM Tree Search on Hard). |
| **Plate VI** | <img src="plates/plate_6.png" width="280" /> | **§6.0. Flop Equivalence & Parameter Tradeoff**: Virtual parameter equivalence ratio `ρ = N_eff / N_base` (Eq. 6.1), and Proposition 6.2 (Economic inversion threshold `Q*` proving 7B + Tree out-economizes 70B pretraining). |
| **Plate VII** | <img src="plates/plate_7.png" width="280" /> | **§7.0. Empirical Benchmark Calibration**: Replication results (Hard problem accuracy boosted from 10.0% to 100.0%; Medium sequential revision saving 4.2× compute over BoN; PRM verification AUC = 0.880). |

---

## Empirical Benchmark Matrix

| Strategy | Difficulty | Solved / Total | Accuracy % | Tokens / Problem | PRM Invocations | Efficiency Score |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: |
| **Greedy (Single-Shot)** | EASY | 16 / 20 | 80.0% | 80.0 | 0.0 | 10.00 |
| **Greedy (Single-Shot)** | MEDIUM | 8 / 20 | 40.0% | 200.0 | 0.0 | 2.00 |
| **Greedy (Single-Shot)** | HARD | 2 / 20 | 10.0% | 320.0 | 0.0 | 0.31 |
| **Parallel Best-of-8** | EASY | 20 / 20 | 100.0% | 640.0 | 16.0 | 1.56 |
| **Parallel Best-of-8** | MEDIUM | 20 / 20 | 100.0% | 1600.0 | 40.0 | 0.63 |
| **Parallel Best-of-8** | HARD | 10 / 20 | 50.0% | 2560.0 | 64.0 | 0.20 |
| **Sequential Revision** | EASY | 19 / 20 | 95.0% | 110.0 | 2.8 | 8.64 |
| **Sequential Revision** | **MEDIUM** | **11 / 20** | **55.0%** | **376.0** | **9.4** | **1.46 (4.2× cheaper than BoN)** |
| **Sequential Revision** | HARD | 4 / 20 | 20.0% | 712.0 | 17.8 | 0.28 |
| **PRM Tree Search** | EASY | 19 / 20 | 95.0% | 480.0 | 12.0 | 1.98 |
| **PRM Tree Search** | MEDIUM | 20 / 20 | 100.0% | 1560.0 | 39.0 | 0.64 |
| **PRM Tree Search** | **HARD** | **20 / 20** | **100.0%** | **2640.0** | **66.0** | **0.38 (10.0× boost over Greedy)** |
