# DS 301 Midterm Project: Reproducing "Evaluating LLM-Generated Rules for Heart Disease Prediction"

**Course:** DS 301, Cornerstone International Community College of Canada (CICCC)
**Instructor:** Professor Padideh Sani
**Team:** Bruno, Booki, and Dilsher

---

## Project Overview

For this midterm we reproduce the classification experiments from a recent research paper on **heart disease prediction**. Using the UCI Heart Disease dataset, we train the paper's traditional machine learning classifiers, compare our results with the paper's results, and suggest ways to improve the model.

The paper also builds classifiers from IF-THEN rules written by large language models (GPT-4o and Claude Sonnet 4.6). That part is outside the scope of DS 301, so **we focus on the traditional classifiers**. The original authors' code is our reference implementation.

---

## References

| Item | Details |
|------|---------|
| **Research paper** | Feisal Alaswad, Batoul Aljaddouh, Maher Alrahhal, Wafaa Al Nassan, Talal Bonny. *Evaluating LLM-Generated Rules for Heart Disease Prediction.* arXiv:2609.13192, 2026. [arxiv.org/abs/2609.13192](https://arxiv.org/abs/2609.13192) · [PDF](https://arxiv.org/pdf/2609.13192) |
| **Dataset** | UCI Machine Learning Repository: *Heart Disease* (Cleveland subset). [archive.ics.uci.edu/dataset/45/heart+disease](https://archive.ics.uci.edu/dataset/45/heart+disease) |
| **Original code** | Authors' repository: [github.com/FeisalAlaswad/LLM-Rule-ML-Heart-Disease-Prediction](https://github.com/FeisalAlaswad/LLM-Rule-ML-Heart-Disease-Prediction) |
| **Presentation** | _TBD: link or file in `presentation/`_ |

---

## The Paper in Brief

**Problem:** Predict whether a patient has heart disease from routine clinical measurements, and compare how accurate and how interpretable different approaches are.

**What the authors did:**
1. Preprocessed the UCI Heart Disease data and selected features.
2. Trained six traditional classifiers: Logistic Regression, K-Nearest Neighbors (KNN), Support Vector Machine (SVM), Naive Bayes, Decision Tree, and Random Forest.
3. Asked two LLMs (GPT-4o and Claude Sonnet 4.6) to write IF-THEN rules for diagnosis, then turned those rules into classifiers.
4. Compared all models on accuracy, precision, recall, and F1-score.

**Key results reported in the paper:**

| Model | Accuracy | Precision | Recall | F1-score |
|-------|----------|-----------|--------|----------|
| Random Forest (best) | 90.2% | 0.829 | 1.000 | 0.906 |
| Naive Bayes | 88.5% | — | — | 0.881 |
| Claude Sonnet 4.6 rules | 80.3% | — | — | 0.833 |
| GPT-4o rules | 70.5% | — | — | 0.690 |

**Conclusion:** The traditional ML models predict better, while the LLM-generated rules are easier for clinicians to read. The paper describes this as a trade-off between performance and interpretability.

---

## The Dataset

The Cleveland subset of the UCI Heart Disease dataset has **303 patient records** with **13 descriptive features** and one **target**.

| Feature | Description |
|---------|-------------|
| `age` | Age in years |
| `sex` | Sex (1 = male, 0 = female) |
| `cp` | Chest pain type (4 categories) |
| `trestbps` | Resting blood pressure (mm Hg) |
| `chol` | Serum cholesterol (mg/dl) |
| `fbs` | Fasting blood sugar > 120 mg/dl (1 = true) |
| `restecg` | Resting electrocardiographic results |
| `thalach` | Maximum heart rate achieved |
| `exang` | Exercise-induced angina (1 = yes) |
| `oldpeak` | ST depression induced by exercise relative to rest |
| `slope` | Slope of the peak exercise ST segment |
| `ca` | Number of major vessels (0 to 3) colored by fluoroscopy |
| `thal` | Thalassemia (normal / fixed defect / reversible defect) |
| **`target`** | **Heart disease present (1) or absent (0)** |

---

## What We Are Doing

1. **Exploratory data analysis (EDA).** Describe the features and the target, check the class balance, and look at distributions and correlations.
2. **Preprocessing and feature engineering.** Handle missing values, encode categorical variables, scale numeric features, and split the data into training and test sets following the paper.
3. **Reproduce the traditional classifiers.** Train the models from the paper that we have studied in DS 301, such as Logistic Regression, KNN, Decision Tree, and Random Forest, plus SVM and Naive Bayes if they are covered in class.
4. **Evaluate and compare.** Report accuracy, precision, recall, F1-score, and the confusion matrix, and compare them side by side with the paper's numbers.
5. **Suggest improvements.** For example: hyperparameter tuning with cross-validation, feature selection, ensemble or boosting methods, and checking how well results hold up with a small dataset of 303 rows.
6. **Present.** Give a 10 to 15 minute presentation covering the paper, the dataset, the methodology, our code, and our suggested improvements.

**Out of scope:** generating rules with LLMs (GPT-4o / Claude). We will mention it in the presentation as context but will not reproduce it. _We will confirm with Professor Sani that a partial reproduction is acceptable._

---

## Team Roles

All three of us take part in every stage. Each member leads one area:

| Member | Lead area |
|--------|-----------|
| **Bruno** | Repository setup and Git workflow, preprocessing pipeline, README and documentation |
| **Booki** | Dataset exploration (EDA), visualizations, feature analysis |
| **Dilsher** | Model reproduction, evaluation metrics, comparison with the paper's results |

The **presentation** and the **suggested improvements** are shared work. Each member presents the part they led.

---

## Repository Structure

```
ds301-midterm-b-b-d/
├── README.md          # Project summary, references, structure, and how to run the code
├── LICENSE
├── data/              # Dataset files (heart.csv)
├── models/            # Notebooks and scripts for EDA, preprocessing, training, and evaluation
├── paper/             # The research paper (PDF) or a link to it
└── presentation/      # Final presentation file (or a link in this README)
```

_The folders will be added as the work progresses._

---

## How to Run

> These instructions will be finalized once the code is in place.

1. Clone the repository:
   ```bash
   git clone https://github.com/brunorochat/ds301-midterm-b-b-d.git
   cd ds301-midterm-b-b-d
   ```
2. Install the dependencies (Python 3.10 or newer):
   ```bash
   pip install -r requirements.txt
   ```
3. Make sure the dataset is in `data/`. It is also available from the [UCI repository](https://archive.ics.uci.edu/dataset/45/heart+disease).
4. Open the notebooks in `models/` and run them in order.

---

## Grading Rubric (for reference)

| Component | Weight |
|-----------|--------|
| Quality of the research paper | 10% |
| Reproduction of the paper implementation | 30% |
| Quality of the work | 10% |
| Presentation and engagement with the audience | 50% |

---

## Git Workflow

- `main` holds the reviewed, submission-ready version.
- Each member works on a personal branch (for example `bruno`) and merges into `main` when the work is ready.
- The repository must stay **public** so the instructor can access it. The final GitHub link and presentation are submitted on Google Classroom.
