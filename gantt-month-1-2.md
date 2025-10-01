```mermaid
gantt
    title ML/DL Month 1 and 2 Roadmap
    dateFormat  YYYY-MM-DD
    tickInterval 1week
    weekday monday
    axisFormat  %m-%d

    %% ============================
    section Foundations
    Python + Git Refresher    :a1, 2025-09-29, 7d
    Linear Algebra Basics     :a2, 2025-09-29, 7d
    Weeks 1-2 Reading            :a3, after a2, 3d
    Vector/Matrix Project + Study    :a4, after a3, 4d
    Python Tooling          :a5, after a4, 7d
    Probability and Calc Intro.    :a6, after a4, 7d
    Weeks 3-4 Reading          :a7, after a6, 3d
    Distribution Calc. Project + Study  :a8, after a7, 4d

    section ML Fundamentals Intro
    scikit-learn and Core ML      :b1, after a8, 7d
    More Stats and Calc:          : b2, after a8, 7d
    Weeks 5-6 Reading             : b3, after b1, 3d
    Linear Regression Project + Study     : b4, after b3, 4d
    Decisions Trees and SVMs      :b5, after b4, 4d
    Model Evaluation              :b6, after b5, 3d
    Stats and Probability:        :b7, after b4, 7d
    Weeks 7-8 Reading             :b8, after b6, 3d
    ML Project on Real Data + Study      :b9, after b8, 4d

    %% ============================
    %%section ML Fundamentals (Months 3-4)
    %%Linear/Logistic Regression      :b1, 2025-11-15, 14d
    %%Gradient Descent Implementation :b2, after b1, 14d
    %%Decision Trees + SVMs           :b3, after b2, 14d
    %%Model Eval: ROC/AUC, CV         :b4, after b3, 14d
    %%PCA + Dimensionality Reduction  :b5, 2025-12-15, 14d
    %%Regularization + Bias-Variance  :b6, after b5, 14d
    %%End-to-End ML Pipeline Project  :b7, after b6, 14d

    %% ============================
    %%section Deep Learning Foundations (Months 5-6)
    %%Neural Net from Scratch (NumPy) :c1, 2026-01-15, 14d
    %%Backpropagation + Activations   :c2, after c1, 14d
    %%PyTorch Basics + MLP Training   :c3, after c2, 14d
    %%CNN Basics (CIFAR-10)           :c4, after c3, 14d
    %%Regularization (Dropout/BN)     :c5, 2026-02-15, 14d
    %%Transfer Learning w/ ResNet     :c6, after c5, 14d
    %%Final Report + Wrap-Up          :c7, after c6, 14d
```

## Reading List

| Weeks   | Textbook or Paper | Section |
| :---: | :---: | :---: |
| 1 and 2  | [Mathematics for Machine Learning](https://github.com/Dueling-W/ml-dl-skills/blob/main/Textbooks/mml-book.pdf)  | Chapters 2 and 3  |
| 1 and 2  | [The Elements of Statistical Learning](https://github.com/Dueling-W/ml-dl-skills/blob/main/Textbooks/ESLII_print12_toc.pdf)  | Intro and Chapter 1  |
| 3 and 4  | [Mathematics for Machine Learning](https://github.com/Dueling-W/ml-dl-skills/blob/main/Textbooks/mml-book.pdf)  | Chapters 5 and 6  |
| 3 and 4  | [Convext Optimization](https://stanford.edu/~boyd/cvxbook/bv_cvxbook.pdf)  | Sections 1.1-1.3  |
| 5 and 6  | [Pattern Recognition and Machine Learning](https://github.com/Dueling-W/ml-dl-skills/blob/main/Textbooks/Bishop-Pattern-Recognition-and-Machine-Learning-2006.pdf)  | Chapters 1-3  |
| 5 and 6  | [A Few Useful Things to Know About Machine Learning (2012)](https://github.com/Dueling-W/ml-dl-skills/blob/main/Academic%20Papers/useful_things_about_ml.pdf)  | All  |
| 7 and 8  | [Pattern Recognition and Machine Learning](https://github.com/Dueling-W/ml-dl-skills/blob/main/Textbooks/Bishop-Pattern-Recognition-and-Machine-Learning-2006.pdf)  | Chapter 4 |
| 7 and 8  | [PCA original paper (Hotelling, 1933)](https://github.com/Dueling-W/ml-dl-skills/blob/main/Academic%20Papers/pca_hotelling.pdf)  | Skim Notation  |

## Quick Links and Resources

### Weeks 1 and 2 All Resources
- **Python Videos**:
    - [Python Refresher](https://www.youtube.com/watch?v=VchuKL44s6E&t=94s)
    - [Python Concepts](https://www.youtube.com/watch?v=Gx5qb1uHss4)
    - [Python OOP Full Course](https://www.youtube.com/watch?v=Ej_02ICOIgs)
    - [Python Iterators](https://www.youtube.com/watch?v=jTYiNjvnHZY)
    - [Python Generators](https://www.youtube.com/watch?v=bD05uGo_sVI)
    - [Python Exceptions Intro](https://www.youtube.com/watch?v=6SPDvPK38tw)
- **GitHub Intro Videos**:
    - [GitHub Crash Course](https://www.youtube.com/watch?v=RGOj5yH7evk&t=425s)
- **Math Links**
    - [Vectors and Spaces](https://www.khanacademy.org/math/linear-algebra/vectors-and-spaces)
    - [Matrix Transformations](https://www.khanacademy.org/math/linear-algebra/matrix-transformations)

---

### Weeks 3 and 4 All Resources
- **Python Videos**
    - [PyTest Course](https://www.youtube.com/watch?v=cHYq1MRoyI0)
- **Math Links**
    - [Random Variables](https://www.khanacademy.org/math/statistics-probability/random-variables-stats-library)
    - [Probability Distributions](https://www.khanacademy.org/math/statistics-probability/modeling-distributions-of-data)

---

### Week 5 and 6 All Resources
- **Python and Theory Videos**
    - [scikit-learn Course - Up to Preprocessing](https://www.youtube.com/watch?v=0B5eIE_1vpU)
    - [Linear and Logistic Regression](https://www.youtube.com/watch?v=0B5eIE_1vpU)
    - [kNN](https://www.youtube.com/watch?v=CQveSaMyEwM)
    - [Gradient Descent](https://www.youtube.com/watch?v=IHZwWFHWa-w)
- **Math Links**
    - [Correlation and Regression](https://www.khanacademy.org/math/statistics-probability/describing-relationships-quantitative-data)
    - [Calculus Refresher](https://www.youtube.com/watch?v=WsQQvHm4lSw)
    - [Gradients and Directional Derivatives](https://www.khanacademy.org/math/multivariable-calculus/multivariable-derivatives/gradient-and-directional-derivatives)

---

### Week 7 and 8 All Resources
- **Python and Theory Videos**
    - [scikit-learn Course - Rest of Video](https://www.youtube.com/watch?v=0B5eIE_1vpU)
- **Math Links**
    - [Hypothesis Testing](https://www.khanacademy.org/math/statistics-probability/significance-tests-one-sample)
    - [Law of Large Numbers](https://www.khanacademy.org/math/statistics-probability/random-variables-stats-library/expected-value-lib/v/law-of-large-numbers)
    - [Sampling Distributions and Central Limit Theorem)[https://www.khanacademy.org/math/statistics-probability/sampling-distributions-library/sample-means]





