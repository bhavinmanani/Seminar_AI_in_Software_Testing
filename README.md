# ML for Automated Software Testing — SoftLang Seminar 2026

University of Koblenz · SoftLang Seminar · Applications of AI · 2026
Application Area: AI in Software Engineering

# Seminar_AI_in_Software_Testing
Semi-systematic literature review investigating how machine learning techniques are applied to automate software testing. The study synthesizes evidence from empirical research on test generation, prioritization, defect prediction, and their impact on fault detection and testing efficiency.

# Research Question

RQ: How have machine learning techniques been applied to automate software testing (e.g., test generation or prioritization), and what gains in fault detection or efficiency do they offer?

# Why interesting?
Software testing is the largest quality-assurance cost in modern development. Understanding whether ML reliably reduces that cost — and by how much — has direct practical impact for QA engineers, developers, and project managers aiming to improve testing efficiency and software quality.

# Why the answer is not obvious:
ML techniques span supervised learning, reinforcement learning, and deep learning, each applied to different testing tasks (generation, prioritization, oracle construction). Gains vary by context, dataset, and training strategy — no single answer covers all cases.

# Repository Structure
```text
Seminar_AI_in_Software_Testing/
├── artifacts/
│   ├── searchlog.md
│   ├── connectedpapers_graph.png
│   ├── search_results_google_scholar.png
│   ├── search_results_ieee.png
│   ├── search_results_acm.png
│   ├── extraction_table.pdf
│   └── prompts_and_evidence.pdf
├── corpus/
│   └── references.md
├── slides/
│   └── Seminar_Presentation.pdf
└── README.md
```

# Methodology

Semi-systematic (narrative) literature review following Snyder (2019). Relevant studies were identified through keyword searches in Google Scholar, ACM Digital Library, IEEE Xplore, and SpringerLink, followed by backward and forward citation snowballing using Connected Papers. The review process followed the reporting recommendations of van Wee & Banister (2024). Data were extracted and synthesized using thematic analysis. Final corpus: 7 peer-reviewed studies.

# Findings

Machine learning has been successfully applied to several software testing activities, particularly test case prioritization, test generation, and regression testing. The reviewed studies consistently report earlier fault detection, faster developer feedback, and improved testing efficiency, especially in Continuous Integration (CI) environments. Reinforcement learning, deep learning, and learning-to-rank techniques were the most frequently investigated approaches.

# How to Validate a Finding
Open the presentation in slides/.
Navigate to the Findings and Analysis slides.
Each comparison table lists:
the selected paper,
the ML technique,
testing task,
reported findings, and
limitations.
Open the corresponding paper using the DOI listed in corpus/references.md.
Search for the cited methodology or reported results to verify the extracted evidence.

# How to Reproduce the Search
Execute the keyword searches documented in artifacts/searchlog.md using Google Scholar, ACM Digital Library, IEEE Xplore, and SpringerLink.
Initial ("seed") papers:
Durelli et al. (2019)
Pan et al. (2021)
Citation snowballing and Connected Papers were then used to identify:
Spieker et al. (2017)
Sharif et al. (2021)
Bagherzadeh et al. (2022)
Zhao et al. (2023)
Fontes & Gay (2023)
Screenshots stored in artifacts/ document the search results and citation graph used during the study.

# Answering the RQ

## How ML is applied:
Reinforcement learning (Q-learning, actor-critic) automates test prioritization in CI by learning from execution history cycle by cycle — no manual retraining required. Supervised learning (ANN, DNN, gradient boosting / MART) automates test generation, oracle construction, and failure prediction. Deep learning extends these with scalable regression models (DeepOrder) that use 14 test-execution features to predict priority scores.

# What gains in fault detection are offered:
NAPFD/APFD scores of 0.79–0.94 achieved vs ~0.5 for random ordering (Sharif et al. 2021)
Pretrained MART achieves optimal test sequence on 80% of subjects vs 50% for original MART — a 60% relative improvement from changing training strategy alone (Zhao et al. 2023)
RL consistently outperforms all traditional heuristics (random, history-based, coverage-based) across industrial CI datasets (Spieker et al. 2017; Bagherzadeh et al. 2022)

# What gains in efficiency are offered:
DeepOrder is 50× faster than RETECS (0.5 hrs vs 25 hrs on the Google dataset with 12 million test executions)
Prediction time under 2.22 seconds per CI cycle — zero delay added to the build process
ML dramatically reduces manual oracle construction effort (Durelli et al. 2019; Fontes & Gay 2023)

# Limitations
The review includes only English-language, peer-reviewed publications that directly address machine learning applications in software testing. Citation networks generated by Connected Papers may evolve as new publications are indexed. Consequently, future searches may produce slightly different citation graphs, although the seed papers and search strategy are documented to ensure transparency and reproducibility.

# Note on the Corpus
The repository contains references and supporting evidence only. Copyrighted research papers are not redistributed. All studies can be accessed through the DOIs listed in corpus/references.md.
