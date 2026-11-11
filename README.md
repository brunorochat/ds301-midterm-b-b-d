# DS 301 Midterm Project: Reproducing a Classification Research Paper

**Course:** DS 301, Cornerstone International Community College of Canada (CICCC)
**Instructor:** Professor Padideh Sani
**Team:** Bruno, Booki, and Dilsher

---

## Project Overview

For this midterm we pick a published research paper on **classification**, get the dataset it uses (from GitHub, Kaggle, or UCI), and **reproduce its experiments**. We then compare our results with the paper's results and suggest ways to improve the model.

We only reproduce algorithms covered in DS 301 so far. If the paper uses a model we have not studied yet, we leave that part out and say so in this README and in the presentation.

| Item | Details |
|------|---------|
| Research paper | _TBD: title, authors, year, and link_ |
| Dataset | _TBD: name and link (GitHub / Kaggle / UCI)_ |
| Target variable | _TBD_ |
| Algorithms reproduced | _TBD (e.g. Logistic Regression, KNN, Decision Tree, ...)_ |
| Presentation | _TBD: link or file in `presentation/`_ |

---

## What We Will Deliver

1. **Paper and dataset selection.** Choose a classification paper with a public dataset, then send the team details, paper, and dataset link to Professor Sani on Slack.
2. **Data exploration (EDA).** Describe the dataset: its features, the target, the class balance, and summary statistics.
3. **Preprocessing and feature engineering.** Handle missing values, encode categorical variables, scale features, and split the data into training and test sets the way the paper did.
4. **Reproduce the paper's models.** Train the classifiers the paper describes with the same setup (hyperparameters, validation strategy, metrics).
5. **Evaluation and comparison.** Report accuracy, precision, recall, F1, and the confusion matrix (plus any other metrics the paper uses), and compare them side by side with the paper's numbers.
6. **Suggested improvements.** List ideas for improving the model, such as tuning, feature selection, resampling, or other algorithms. These are suggestions only; we do not need to implement them.
7. **Presentation (10 to 15 minutes)** covering:
   - the paper and the problem it solves
   - the dataset: its features, target, and descriptive features
   - the methodology and algorithms
   - a walkthrough of our reproduction code
   - our suggested improvements

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
├── README.md          # Project summary, structure, and how to run the code
├── LICENSE
├── data/              # Dataset files (.csv / .xlsx)
├── models/            # Notebooks and scripts for preprocessing, training, and evaluation
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
3. Put the dataset in `data/` (or follow the download link in the table above).
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
