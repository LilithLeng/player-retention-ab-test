# Mobile Game A/B Testing Analysis (Cookie Cats)

This project analyzes an A/B test conducted in a mobile game to evaluate how a change in game design affects player retention and engagement.

The experiment tests two different versions of a level gate in the game:

- **gate_30** – the original design
- **gate_40** – the experimental design

The goal of this analysis is to determine whether moving the game gate affects player behavior and retention.

---

# Project Overview

In many mobile games, level gates are used to control player progression. Gates are often placed at specific levels to slow progression and encourage players to engage more deeply with the game.

However, changing the position of a gate may influence player experience and retention.

This project analyzes an A/B test to understand whether moving the gate from **level 30 to level 40** impacts:

- player engagement
- 1-day retention
- 7-day retention

The analysis uses statistical testing to determine whether the observed differences between the two groups are significant.

---

# Business Questions

This project aims to answer several key product analytics questions:

- Does moving the level gate affect player engagement?
- Does the change improve or reduce player retention?
- Is the difference statistically significant?
- Which version should the product team adopt?

---

# Dataset

The dataset contains player-level data from the mobile game **Cookie Cats**.

Each row represents one player.

Key variables include:

- **userid** — unique player identifier
- **version** — experiment group (`gate_30` or `gate_40`)
- **sum_gamerounds** — total number of game rounds played
- **retention_1** — whether the player returned after 1 day
- **retention_7** — whether the player returned after 7 days

Total players in the dataset: **90,189**

The two experiment groups are roughly balanced.

---

# Tools & Technologies

The analysis was conducted using **Python**.

Main libraries used:

- **Pandas** — data manipulation
- **NumPy** — numerical calculations
- **Matplotlib** — visualization
- **Seaborn** — statistical plots
- **SciPy / Statsmodels** — hypothesis testing

The analysis was performed in **Jupyter Notebook**.

---

# Analysis Workflow

The project follows a standard data analysis and experimentation workflow.

---

## 1. Data Loading

The dataset was imported and inspected to understand its structure.

Initial checks confirmed:

- no missing values
- balanced sample sizes between experiment groups

---

## 2. Exploratory Data Analysis (EDA)

Player behaviour was explored using descriptive statistics and visualizations.

Key metrics examined include:

- number of game rounds played
- player activity distribution
- engagement outliers

This step helps identify patterns and anomalies before running statistical tests.

---

# A/B Test Analysis

The experiment compares two versions of the game gate:

| Version | Description |
|------|------|
| gate_30 | Original gate position |
| gate_40 | Experimental gate position |

Player retention rates were calculated for both groups.

The analysis focuses on:

- **1-day retention**
- **7-day retention**

Retention rates were compared across the two groups to determine whether the change in game design affected player behaviour.

---

# Hypothesis Testing

Statistical tests were performed to determine whether the differences between the two groups are significant.

The hypotheses are:

**Null hypothesis (H0)**  
There is no difference in player retention between the two gate positions.

**Alternative hypothesis (H1)**  
Player retention differs between the two gate positions.

A **two-sample Z-test** was used to compare retention rates between the experiment groups.

---

# Key Insights

The analysis reveals several important findings.

Player engagement shows large variability, with some players playing significantly more rounds than others.

The difference in retention between the two groups is relatively small, but statistical testing helps determine whether the difference is meaningful.

The results provide data-driven evidence that can support product decisions regarding level design.
