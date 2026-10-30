# Pharmaceutical Chemistry Data Analysis Notebooks

Re-analysing my own first-year undergraduate lab data (MSci Pharmaceutical Chemistry, University of Huddersfield) in Python, using the statistical and validation methods applied in analytical and QC laboratories.

In each practical I first analysed the results by hand or in Excel. In these notebooks I go back to the same raw readings and ask what a more rigorous analysis shows. In two of the three cases, it changed or sharpened my conclusion.

| # | Notebook | Technique | Key finding | Open |
|---|---|---|---|---|
| 01 | [UV-Vis calibration (Beer-Lambert)](notebooks/01_uvvis_calibration_beer_lambert.ipynb) | UV-Vis spectrophotometry | ε = 334 ± 14 M⁻¹ cm⁻¹ (free fit), 344 through the origin, compared with 348 from my hand-drawn graph. The residual plot finds one standard reading about 3% low. Includes LOD/LOQ and inverse-prediction uncertainty. | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/YOUR-GITHUB-USERNAME/pharma-data-notebooks/blob/main/notebooks/01_uvvis_calibration_beer_lambert.ipynb) |
| 02 | [Reaction kinetics & Arrhenius](notebooks/02_reaction_kinetics_and_arrhenius.ipynb) | Kinetics by UV-Vis | The textbook R² test suggested second order. A first-order model with an absorbance baseline (Cr³⁺ product) fits best by AICc: k′ = 0.057 ± 0.005 min⁻¹, t½ ≈ 12 min. Eₐ = 48.5 kJ mol⁻¹, with a shelf-life-style extrapolation to 25 °C. | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/YOUR-GITHUB-USERNAME/pharma-data-notebooks/blob/main/notebooks/02_reaction_kinetics_and_arrhenius.ipynb) |
| 03 | [Size-exclusion chromatography](notebooks/03_size_exclusion_chromatography.ipynb) | Sephadex G-25 gel filtration | BSA elutes before vitamin B12, as size exclusion predicts. Two artefact fractions are flagged by a rule. The 460 nm signal turns out not to be specific to B12. Data-driven pooling selects fractions 9–13 (≈ 69% recovery). | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/YOUR-GITHUB-USERNAME/pharma-data-notebooks/blob/main/notebooks/03_size_exclusion_chromatography.ipynb) |

## Data provenance

- **My own measurements:** Notebook 01, Notebook 02 Part A and Notebook 03.
- **Course-supplied model data:** Notebook 02 Parts B and C (clearly labelled in the notebook).

Only my recorded readings are reproduced here. No lab manuals or course materials are included.

## Skills demonstrated

- Linear and non-linear least-squares regression (`scipy.stats`, `scipy.optimize.curve_fit`)
- Confidence intervals, prediction intervals and propagation of calibration uncertainty
- Method-validation concepts: linearity, residual analysis, LOD/LOQ (ICH Q2)
- Kinetic model selection with AICc, integrated rate laws and numerical differentiation
- Arrhenius analysis and its link to accelerated stability testing (ICH Q1A)
- Chromatogram interpretation: peak centroids, artefact detection, wavelength specificity, yield-purity trade-off
- Data handling with `pandas` and publication-style plots with `matplotlib`

## Running the notebooks

Click any **Open in Colab** badge above. Nothing needs installing, and every notebook contains its own data.

To run locally:

```bash
pip install -r requirements.txt
jupyter notebook notebooks/
```

## About me

Ali Sher Afzaal, MSci Pharmaceutical Chemistry student, University of Huddersfield. Seeking a 12-month industrial placement from September 2027.
Certifications: freeCodeCamp *Scientific Computing with Python*
