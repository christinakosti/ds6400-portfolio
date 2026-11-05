# Advanced Machine Learning I - DS 6400 Portfolio

This repository contains my coursework and computational explorations from **DS 6400: Advanced Machine Learning I** at the University of Virginia.

The portfolio covers statistical learning methods, model evaluation, regularization and model interpretation through mathematical explanations, reproducible R code, and visualizations.

Where relevant, I incorporate examples from **exercise physiology, biomedical research and wearable technology** to connect statistical methods with research questions in my field.

📖 **[Explore the Interactive Portfolio](https://christinakosti.github.io/ds6400-portfolio/)**

## Featured applied examples

| Application | Where to look | What the analysis demonstrates |
|---|---|---|
| **Wearables → next-day performance** | **Chapter 4, §4.3.1–4.4.4** · [Case study](https://christinakosti.github.io/ds6400-portfolio/04-random-forests.html#case-study-predicting-next-day-performance) · [Sleep × training-strain interaction](https://christinakosti.github.io/ds6400-portfolio/04-random-forests.html#do-sleep-and-training-strain-interact) | A **simulated longitudinal wearable dataset** with 160 individuals and 2,240 person-days. Random Forest predicts a next-day performance score from sleep, HRV and resting-heart-rate deviations, training strain, activity, and other features; the analysis examines out-of-bag error, permutation importance, nonlinearities, and sleep–strain interactions. |
| **Muscle strength → nonlinear modeling** | **Chapter 5, §5.1.1–5.1.3 and §5.3–5.6** · [Muscle-strength example](https://christinakosti.github.io/ds6400-portfolio/05-polynomial-regression.html#applied-research-example-muscle-strength-assessment) · [Comparison of polynomial bases](https://christinakosti.github.io/ds6400-portfolio/05-polynomial-regression.html#comparison-of-polynomial-bases) | Compares **natural/raw, Bernstein, and orthogonal polynomial bases** using simulated age–isokinetic-strength data. §5.1.3 also connects polynomial fitting to my published research using knee-joint-angle and dynamometry measurements. |
| **Electrical impedance myography → handgrip strength** | **Chapter 7, §7.10** · [Physiological example](https://christinakosti.github.io/ds6400-portfolio/07-regularization-elastic-net.html#computational-exploration-a-physiological-example) · [Feature selection / grouping](https://christinakosti.github.io/ds6400-portfolio/07-regularization-elastic-net.html#variable-selection-and-the-grouping-effect) · [Independent test performance](https://christinakosti.github.io/ds6400-portfolio/07-regularization-elastic-net.html#predictive-performance-on-independent-test-data) | Compares **Ridge, LASSO, and Elastic Net** for predicting handgrip strength using **243 correlated, simulated EIM features**, with 60 training and 200 held-out test observations. Includes coefficient paths, 10-fold cross-validation, correlated-feature selection, and test-set errors. |

**Data transparency:** The wearable, age–strength, and EIM datasets above are **simulated teaching examples**, not clinical validation studies or analyses of actual wearable users.

## Explore the full portfolio

| Chapter | Topics / techniques | Key sections |
|---|---|---|
| [**1. Cross-Validation Selection Bias**](https://christinakosti.github.io/ds6400-portfolio/01-cross-validation-selection-bias.html) | Why selecting and evaluating a model with the same cross-validation results biases reported performance; nested CV, k-NN, held-out testing, repeated simulation | **§1.1.11** [Computational exploration](https://christinakosti.github.io/ds6400-portfolio/01-cross-validation-selection-bias.html#computational-exploration); **§1.1.12** conclusions |
| [**2. The .632+ Bootstrap Method**](https://christinakosti.github.io/ds6400-portfolio/02-632-plus-bootstrap.html) | Bootstrap estimation of prediction error; apparent error, out-of-bag error, .632 and .632+ estimators, bias–variance tradeoff | **§2.1.10** [Computational exploration](https://christinakosti.github.io/ds6400-portfolio/02-632-plus-bootstrap.html#computational-exploration) |
| [**3. Partial Dependence Plots**](https://christinakosti.github.io/ds6400-portfolio/03-pdp-visualizing-the-model.html) | Model interpretation; nonlinear relationships; comparing random-forest and spline-regression PDPs; cautions about correlated predictors | **§3.5–3.7** [Simulation, models, and PDPs](https://christinakosti.github.io/ds6400-portfolio/03-pdp-visualizing-the-model.html#computational-exploration) |
| [**4. Random Forests**](https://christinakosti.github.io/ds6400-portfolio/04-random-forests.html) | Ensemble learning, bootstrap aggregation, OOB evaluation, permutation importance, partial dependence, interactions | **§4.3–4.4** [Wearable-performance case study](https://christinakosti.github.io/ds6400-portfolio/04-random-forests.html#computational-demonstration) |
| [**5. Polynomial Regression**](https://christinakosti.github.io/ds6400-portfolio/05-polynomial-regression.html) | Basis expansions, numerical stability, raw/Bernstein/orthogonal polynomials, nonlinear muscle-strength relationships | **§5.1.3** [Research application](https://christinakosti.github.io/ds6400-portfolio/05-polynomial-regression.html#applied-research-example-muscle-strength-assessment); **§5.6** [Basis comparison](https://christinakosti.github.io/ds6400-portfolio/05-polynomial-regression.html#comparison-of-polynomial-bases) |
| [**7. Regularization — Elastic Net**](https://christinakosti.github.io/ds6400-portfolio/07-regularization-elastic-net.html) | High-dimensional regression, Ridge/LASSO/Elastic Net, shrinkage paths, feature selection, 10-fold CV, independent evaluation | **§7.10** [EIM and handgrip-strength example](https://christinakosti.github.io/ds6400-portfolio/07-regularization-elastic-net.html#computational-exploration-a-physiological-example) |

## Technical skills illustrated

**Programming & workflow:** R · Quarto · Git/GitHub · reproducible simulations · data visualization (`ggplot2`) · statistical modeling (`glmnet`)

**Statistical learning:** Linear and nonlinear regression · polynomial basis expansions · Random Forest · Ridge · LASSO · Elastic Net · k-nearest neighbors

**Evaluation & interpretation:** Cross-validation and nested cross-validation · bootstrap-based error estimation · out-of-bag validation · independent train/test evaluation · permutation importance · partial dependence · coefficient paths · multicollinearity and high-dimensional feature selection

## Source code and reproducibility

Each analysis has a `.qmd` source file at the repository root, with R code embedded alongside its explanations. The compiled book is stored under [`_book/`](./_book/).

| Example | Source code |
|---|---|
| Wearable / Random Forest | [`04-random-forests.qmd`](./04-random-forests.qmd) |
| Muscle-strength polynomial regression | [`05-polynomial-regression.qmd`](./05-polynomial-regression.qmd) |
| EIM / regularization | [`07-regularization-elastic-net.qmd`](./07-regularization-elastic-net.qmd) |

To render the book locally (with [Quarto](https://quarto.org/) and the R packages used in the chapters installed):

```bash
quarto render
```