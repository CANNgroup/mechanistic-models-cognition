# Figure 3 — Cognition models (pedagogical notebooks)

This folder contains five Jupyter notebooks that accompany **Figure 3** of:

> Froudist-Walsh S, Ivanov TG, Magrou L, Cho H, Busch AN, Muller LE, et al. (in press): Mechanistic computational models of cognition across scales and species. *Biol Psychiatry*.

The review traces how a single recurrent-network building block — the Wong & Wang
(2006) two-population decision module — can be extended into mechanistic models
of a wide range of cognitive functions. These notebooks are **pedagogical
companions, not full replications**: each one re-implements the *minimal* version
of one model from the review, exposes the parameters that matter most, and
includes a "biological context" section explaining what the model can and cannot
tell you. Author: **Teo Fantacci**.

## The notebooks

| Notebook | Fig 3 panel | Review §  | Based on |
|---|---|---|---|
| [`working_memory_items.ipynb`](working_memory_items.ipynb) | 3A | §2 Working memory | Brunel & Wang (2001) |
| [`perceptual_decision_making.ipynb`](perceptual_decision_making.ipynb) | 3B | §3.1 Decision-making | Wong & Wang (2006) |
| [`conscious_access.ipynb`](conscious_access.ipynb) | 3C | §3.2 Conscious perception | Klatzmann et al. (2025) |
| [`multisensory_integration_audio_visual.ipynb`](multisensory_integration_audio_visual.ipynb) | 3D | §3.3 Multi-sensory integration | Brady & Butler (2025) |
| [`working_memory_for_spatial_location.ipynb`](working_memory_for_spatial_location.ipynb) | 3E | §3.4 Spatial WM (bump attractor) | Wimmer et al. (2014) — *Python port of MATLAB code* |

Each notebook is self-contained: you can run any one of them without the
others. Where one model reuses a building block from another (e.g. the
multisensory notebook reuses the Wong–Wang module from the perceptual
decision-making notebook), the relevant equations are restated inline.

### One special case

The **spatial-WM notebook** (`working_memory_for_spatial_location.ipynb`) is a
**faithful Python port of the MATLAB code released by Wimmer et al. (2014)**
(*Supplementary Code 1*). Parameter values, equations, integration scheme, and
noise conventions are taken verbatim from the `.m` file. As a result, this
notebook uses a **different transfer function**, **no AMPA/NMDA/GABA gating
variables**, **uniform all-to-all inhibition**, and **additive Gaussian noise on
the rate equation** rather than the OU current noise used in the other four. The
notebook documents these four deviations explicitly in its "What this notebook
is, and is not" section.

## Running

The notebooks require only `numpy` and `matplotlib`. They run in:

- **Google Colab** (recommended for first-time use — no install needed)
- **Local Jupyter** with Python ≥ 3.8

```bash
pip install numpy matplotlib jupyter
jupyter notebook
```

No external data files are needed; all simulations are generated at runtime.
Results are written to a `saved_results/` subfolder (path configurable in each
notebook's setup cell).

## What each notebook contains

A consistent structure across all five:

1. **Authorship and how to cite** — top cell.
2. **Model overview + Dynamics** — equations, notation, and the mechanism in
   words. *(In the spatial-WM notebook, this is split as "Model overview" +
   "What this notebook is, and is not" + "Task simulated" to flag the MATLAB-
   port conventions.)*
3. **Reference and scope** — what the notebook keeps, simplifies, or drops
   relative to the original paper.
4. **Parameters dict** — the knobs most worth varying.
5. **Connectivity, f-I curves, simulation core** — the actual code.
6. **Quick sanity checks** — reproducibility tests + key invariants.
7. **Biological context** — what the model represents in the brain, what it
   *can* explain, and what it *cannot*.

## Citing

If you use these notebooks in research or teaching, please cite **both** the
review and the original paper your notebook is based on (each notebook's "How
to cite" cell lists both, formatted in the review's reference style). All code
is original; for the spatial-WM notebook it is a Python re-implementation of
the published MATLAB source.

## Scope

These five notebooks cover panels A–E of the review's Figure 3. The remaining
panels (selective attention F, sustained attention G, sequence WM H, planning I)
and the multi-scale and cross-species models from the review's Sections 2.5 and
4 are not included here — they are substantial enough to deserve separate
companion notebooks.
