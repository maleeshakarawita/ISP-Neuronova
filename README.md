# 🧠 Bilateral Hemispheric Coupling in the Mouse Brain
### *Widespread. Dissociated. Revealing.*

<img width="1858" height="902" alt="image" src="https://github.com/user-attachments/assets/97deee8f-f8e7-4d31-a2fe-fe182c1ebc67" />



---

## ✦ Overview

This repository accompanies the paper:

**"Bilateral hemispheric coupling is widespread but dissociated from choice encoding across the mouse brain"**
*Yegarmina, A. · Karawita, M. · Kaleem, H. · Samimi, Z.*
Neuromatch Academy, Neuromatch Inc. | NUST, Pakistan

We set out to answer a deceptively simple question: **Do the brain regions that talk to each other the most also make decisions together?**

The answer — emphatically, elegantly — is **NO**.

---

## ✦ The Big Idea

Using the **IBL Brain-wide Map** (699 Neuropixels insertions, 39 homotopically recorded regions), we applied **Canonical Correlation Analysis (CCA)** to characterize how the left and right hemispheres of the mouse brain synchronize during a visual decision-making task.

What we found rewrites intuition:

| What we expected | What we found |
|---|---|
| Strongly coupled regions = strong decision encoders | **They're completely uncorrelated** (ρ = −0.21) |
| Hippocampus drives decisions bilaterally | **Hippocampus synchronizes maximally but encodes choice minimally** |
| Cross-hemisphere relay is sequential | **Zero-lag dominance suggests simultaneous common-input drive** |

---

## ✦ Key Findings

### 1 · Coupling Is Everywhere — But Unequal
All 39 brain regions showed **significant bilateral coupling** (r = 0.25 → 0.96), ranging from the faint whisper of higher visual cortex to the thunderous synchrony of the hippocampal subiculum.

```
SUB  ████████████████████  r = 0.96  ← Strongest
CA1  ████████████████████  r = 0.91
APN  ████████████████████  r = 0.89
MRN  ████████████████████  r = 0.87
...
VISpm2/3  ██████            r = 0.25  ← Weakest
```

<img width="1125" height="692" alt="image" src="https://github.com/user-attachments/assets/8e9750ed-cb08-486e-be17-c2892e3151b6" />

### 2 · Coupling ≠ Choice
The **prefrontal cortex** — not the hippocampus — routes decision information bilaterally:

- **PL6a**: decision fraction = 0.22 · pre-movement · motor planning
- **ILA6a**: decision fraction = 0.20 · post-movement · integration
- **CA1**: decision fraction = 0.04 · despite r = 0.91 coupling

<img width="1128" height="846" alt="image" src="https://github.com/user-attachments/assets/0511c2ec-ea1e-4da3-b789-6f4d2cf257ad" />


> Hippocampal hemispheres *know* the animal's choice (AUC ≈ 0.65) — they just don't *talk about it* across the midline.

### 3 · Three Temporal Regimes of Interhemispheric Coordination
Cross-correlograms revealed three distinct coupling fingerprints:

| Profile | Regions | Mechanism |
|---|---|---|
| 🌊 Oscillatory zero-lag | Hippocampus, Midbrain | Theta-driven common input |
| 🔵 Broad sustained zero-lag | Prefrontal, Superior Colliculus | Tonic bilateral coordination |
| ⬆️ Asymmetric positive-lag | Retrosplenial, Posterior Thalamus | Directional relay |

<img width="1109" height="741" alt="image" src="https://github.com/user-attachments/assets/439c70ef-668c-4538-96d9-4f730dc52394" />


---

## ✦ Methods at a Glance


<img width="960" height="540" alt="image" src="https://github.com/user-attachments/assets/89a370b5-6f54-4f02-9ff4-1260ffee49d4" />


**Significance**: 500-permutation shuffle test (right-hemisphere trial order)
**Aggregation**: Fisher z-transformation across sessions

---

## ✦ The Four-Quadrant Brain

Plotting **within-hemisphere decision strength** (Fréchet distance) against **between-hemisphere coupling** reveals a 2D organizational space with four functional identities:

```
High coupling ┤
              │  🔵 Hippocampus     🟢 PL6a, ILA6a, PO
              │  (sync but silent)  (the decision makers)
              │
              │  ⬜ Weak both       🟡 MOs5, MOs6a
              │                     (independent encoders)
Low coupling  ┤
              └─────────────────────────────────────────
              Low encoding          High encoding
```

---

## ✦ Implications

**For systems neuroscience:**
Interhemispheric synchrony and decision-specific lateralization are **orthogonal organizational principles** — not two sides of the same coin.

**For clinical neuroscience:**
Motor and hippocampal regions, being maximally coupled, are predicted to be most vulnerable to **callosal disruption** (e.g., split-brain, lesion, demyelination).

**For computational neuroscience:**
The CCA pipeline here is fully reusable — and naturally extends to **ML-based inference of contralateral dynamics from unilateral recordings**.

---

## ✦ Repository

```bash
git clone https://github.com/maleeshakarawita/Neuronova
```

**Stack**: Python 3.10 · one-api · scikit-learn · numpy · scipy · pandas

---

## ✦ Authors & Acknowledgments

| Author | Affiliation |
|---|---|
| A. Yegarmina | Neuromatch Academy |
| M. Karawita | Neuromatch Academy |
| H. Kaleem | SEECS, NUST Pakistan |
| Z. Samimi | Neuromatch Academy |

We owe deep thanks to our mentor **Nader Nikbakht** and to the **Neuromatch Impact Scholars Program** for making this work possible.

---

## ✦ Citation

```bibtex
@article{yegarmina2025bilateral,
  title   = {Bilateral hemispheric coupling is widespread but dissociated
             from choice encoding across the mouse brain},
  author  = {Yegarmina, A. and Karawita, M. and Kaleem, H. and Samimi, Z.},
  journal = {Neuromatch Academy},
  year    = {2025}
}
```

---

*Built with curiosity. Powered by spikes. Rendered in both hemispheres.*
