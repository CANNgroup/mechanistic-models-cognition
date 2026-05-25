
# Pedagogical notebooks for mechanistic computational models of cognition

This repository contains pedagogical code notebooks accompanying the review article:

**Mechanistic computational models of cognition across scales and species**  
Sean Froudist-Walsh, Tsvetoslav G. Ivanov, Teo Fantacci, Loic Magrou, Harper Cho, Eleonora Russo, Alexandra N. Busch, Lyle E. Muller, Hongyu John Meng, John D. Murray, and Xiao-Jing Wang.

The notebooks are intended to help readers interactively explore the computational modelling ideas discussed in the review. They are designed for teaching, self-study, and conceptual understanding rather than as exact reproductions of all simulations in the original research articles.

## Notebooks

| Notebook / topic | Related figure or section | Primary notebook author(s) |
|---|---|---|
| Models of cognition beyond working memory | Figure 3 | Teo Fantacci |
| Marmoset vs macaque spiking model of distractibility | Figure 4 | Tsvetoslav G. Ivanov |
| Marmoset vs macaque large-scale working memory model | Figure 4 | Loic Magrou |
| Large-scale dopamine model of distributed working memory | Figure 2 / Section 2.5 | Sean Froudist-Walsh |

Additional contributors and acknowledgements may be listed in individual notebooks.

## Purpose

The notebooks illustrate how mechanistic computational models can link:

- synaptic, cellular, and circuit mechanisms to cognition;
- local circuit dynamics to brain-wide activity;
- working memory models to broader cognitive functions;
- species-specific anatomical and physiological parameters to cross-species differences in cognition.

They are intended to accompany the review article and provide readers with runnable examples of the modelling principles discussed there.

## Getting started

Clone the repository:

```bash
git clone mechanistic-models-cognition
cd mechanistic-models-cognition
````

Install the required Python packages using the environment file, if provided:

```bash
conda env create -f environment.yml
conda activate <environment-name>
```

or, if using `pip`:

```bash
pip install -r requirements.txt
```

Then open the notebooks:

```bash
jupyter lab
```

## Citation

If you use these notebooks, please cite the accompanying review article:

> Froudist-Walsh, S., Ivanov, T. G., Fantacci T., Magrou, L., Cho, H., Russo. E., Busch, A. N., Muller, L. E., Meng, H. J., Murray, J. D., & Wang, X.-J.
> *Mechanistic computational models of cognition across scales and species.*
> [Journal / DOI to be added]

Please also cite the original research articles referenced within each notebook where appropriate.

If a versioned release of this repository is archived on Zenodo, please cite the repository DOI as well:

> [Repository Zenodo DOI to be added]

## Authorship and credit

Each notebook lists its primary author(s) at the top of the file. GitHub commit history, this README, and any future archived release should be used together to document contributions.

For questions about the repository, please contact:

**Sean Froudist-Walsh**
Cognition, Anatomy & Neural Networks group
University of Oxford / Trinity College Dublin
[sean.froudist-walsh@ndcn.ox.ac.uk](mailto:sean.froudist-walsh@ndcn.ox.ac.uk)

## Licence

Code and notebooks are released under the licence specified in the `LICENSE` file. Please check individual notebooks for any additional data, figure, or third-party code acknowledgements.

```
```
