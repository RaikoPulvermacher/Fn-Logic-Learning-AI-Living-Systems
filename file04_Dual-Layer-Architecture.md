# file04: Dual-Layer Architecture (Integer Standard & Masking)

## 1. The Principle of Scaling: Away with the Decimal Point

In conventional systems, rounding errors arise because the attempt is made to press reality into decimal places (floating-point numbers). Fn-Logic instead uses the **Atomic Integer Level**[^1].

* **The Trick**: Instead of calculating $127.53$ metres (which requires floats), the system computes in the background with femtometres ($10^{-15}\ \text{m}$).
* **The Value**: $127{,}530{,}000{,}000{,}000{,}000$ femtometres — a pure integer.
* **The Advantage**: There are no "fractional" units, only discrete ticks. All precision is structurally guaranteed, not numerically approximated[^2].

| Classical Architecture (Float) | Fn-Dual-Layer Architecture (Integer) |
| :--- | :--- |
| Computes internally with decimal places | Computes internally with femtometre integers |
| Rounding errors already in the core | Core is 100% lossless |
| Display ≈ calculation basis | Display (mask) is strictly separated from the core |
| Heat from irrational operations | Cold, since no division or root in the core |

## 2. The Two Layers of the System

```
[Input / Impulse]
        │
        ▼
┌───────────────────────────────────┐
│  CORE  (Back-End: Atomic Level)   │
│  • Unit:    Femtometre / Planck-tick│
│  • Logic:   Pure Integer Addition  │
│  • Quality: lossless, cold,        │
│             absolute precision     │
└───────────────┬───────────────────┘
                │  exact integer
                ▼
┌───────────────────────────────────┐
│  MASK  (Front-End: Macro Level)   │
│  • Function: Set decimal point    │
│  • Allowed: Rounding for the eye  │
│  • Forbidden: Writing back to Core│
└───────────────┬───────────────────┘
                │
                ▼
     [Output for the Human]
       e.g. "127.53 m"
```

### A. The Core (Back-End: Atomic Level)
This is where actual intelligence takes place. The core works exclusively with Fn-addition logic on the smallest possible physical scale[^1].

* **Unit**: Femtometre / Planck-tick.
* **Logic**: Pure integer addition — no dividing, no root extraction.
* **Property**: 100% lossless, no thermal emission (cold), absolute precision.

### B. The Mask (Front-End: Macro Level)
The mask is the interface for the human. It "translates" the enormous integers of the core into readable formats[^1].

* **Function**: Shifting the decimal point for display.
* **Example**: The core delivers $127{,}530{,}000{,}000{,}000{,}000\ \text{fm}$, the mask shows "$127.53\ \text{m}$".
* **One-Way Principle**: The mask may round or approximate for the eye — the core must never round, in order to preserve the integrity of the process. Corrections flow back into the core as new impulses, never as direct overwriting.

## 3. Convergence with the Biological Model

The Dual-Layer Architecture is not a purely technical decision — it mirrors the design principle of living systems[^1][^2]:

| Biological System | Dual-Layer Architecture |
| :--- | :--- |
| **Cell Nucleus** — DNA, exact replication, cold | **Fn-Core** — integer addition, lossless |
| **Cell Membrane** — external communication | **Mask** — scaling for human readability |
| Internal processes run stably at 37 °C | Core generates no waste heat through rounding |
| Membrane filters: not everything reaches inside | Mask does not write back into the core |

Biological cells reach their saturation point after exactly $F_{11} = 89$ ticks[^2]. In the Dual-Layer Architecture, this corresponds to the moment at which a complete learning cycle in the core is finished and the result is passed to the mask — not before.

## 4. Why AI Learns Better with This

When an AI today "learns", it loses information through float-conversion at every layer transition. In the Dual-Layer Architecture, this does not happen[^1][^2]:

1. **AI Training in the Core**: Every "weight" is an exact position on the atomic scale — no approximation.
2. **No Friction Between Layers**: Since the core never divides or extracts roots, there is no data congestion and no heat generation.
3. **Infinite Network Depth**: Neural networks with millions of layers can be built without any loss of precision — integers retain their accuracy completely[^1].
4. **Stable Feedback**: Corrections (e.g., backpropagation) are added as new impulses, not multiplied as float gradients — the Fn-rhythm U-U-E is preserved[^3].

## 5. Example: The Vacuum Fall ($127.53\ \text{m}$)

* **Euler Computer**: Calculates with $9.81 \times 5^2 / 2 = 122.625\ \text{m}$. Floats require rounding operations — this generates heat and a measurement error of approximately 5 m compared to the real result[^2].
* **Fn-Computer (Core)**: Adds exactly 13 ticks on the atomic scale. The result is $127{,}530{,}000{,}000{,}000{,}000\ \text{fm}$ — an exact integer, no approximation error.
* **Fn-Computer (Mask)**: Sets the decimal point for the user: $127.53\ \text{m}$.

The difference of approximately $5\ \text{m}$ between the Euler model and the Fn-model is not a measurement error — it is proof that the classical model is structurally incomplete[^2].

---

**Reference Documents & Sources:**

[^1]: Fn-Logic: The Mathematics of Process — DOI: [10.5281/zenodo.19101547](https://doi.org/10.5281/zenodo.19101547)
[^2]: Energy-Revolution 8911: Overcoming Euler-Resistance through Procedural FN Resonance — DOI: [10.5281/zenodo.18842797](https://doi.org/10.5281/zenodo.18842797)
[^3]: Tensor Realities (TdR) — DOI: [10.5281/zenodo.18727529](https://doi.org/10.5281/zenodo.18727529)

---
*License: Pulvermacher Open Research License (PORL) v1.0*
