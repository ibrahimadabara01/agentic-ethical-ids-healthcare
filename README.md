# agentic-ethical-ids-healthcare
Official code and setup for "Trustworthy and Ethical AI for Intrusion Detection in Healthcare IoT (IoMT) Systems: An Agentic Decision Loop Framework"
📋 Overview

This repository contains the official code, datasets, and configuration setup for the paper submitted to Springer’s Journal of Healthcare Informatics Research (JHIR).
The study presents a multi-agent intrusion detection architecture that integrates:

A supervised flow-based detector

A Deep Q-Network (DQN) triage agent

A NIST AI RMF–aligned ethical rule engine

The framework enables trustworthy, safe, and context-aware intrusion detection in healthcare IoT environments (IoMT).

🏗️ Repository Structure
agentic-ethical-ids-healthcare/
│
├── src/                     # Source code for model, rule engine, and agent
│   ├── train_agent.py
│   ├── ethical_engine.py
│   ├── detector_model.py
│   └── utils/
│
├── data/                    # Links or sample data subsets
│   ├── CIC-IoMT-2024/       
│   └── CSE-CIC-IDS2018/
│
├── notebooks/               # Jupyter notebooks for training and analysis
│
├── models/                  # Pretrained model checkpoints (.pth, .pkl)
│
├── results/                 # Evaluation outputs and figures
│
├── requirements.txt         # Python dependencies
├── LICENSE                  # MIT License for open research use
└── README.md                # Project documentation

⚙️ Setup and Installation

Clone the repository and set up your environment:

git clone https://github.com/ibrahimadabara01/agentic-ethical-ids-healthcare.git
cd agentic-ethical-ids-healthcare
python -m venv venv
source venv/bin/activate   # On Windows: venv\Scripts\activate
pip install -r requirements.txt

📊 Datasets

This project uses three datasets:

Dataset	Purpose	Source
CIC-IoMT 2024	Primary IoMT intrusion detection dataset	Canadian Institute for Cybersecurity

CSE-CIC-IDS2018	Domain-shift evaluation	CIC Dataset Portal

MIMIC-IV (Demo)	Clinical context signals	PhysioNet

⚠️ Note: All datasets are publicly available. The MIMIC-IV Demo contains only de-identified data.

🚀 How to Reproduce Results

Run the full pipeline (training + evaluation):

python src/train_agent.py --config configs/agentic_ids.yaml


This script:

Trains the supervised flow-based detector on CIC-IoMT 2024

Fine-tunes the DQN triage agent

Evaluates under domain-shift using CSE-CIC-IDS2018

Computes Ethical Compliance Rate (ECR), False Escalation Rate (FER), and CAS metrics

📈 Key Metrics
Metric	Description
Accuracy	Correct classification rate across all flows
F1-Score (Weighted)	Balanced measure of precision and recall
Ethical Compliance Rate (ECR)	Percentage of actions consistent with governance rules
False Escalation Rate (FER)	Proportion of overreactions (false alarms)
Contextual Adaptation Score (CAS)	Robustness under domain-shift
📘 Citation

If you use this repository, please cite:

Adabara, I. M., et al. (2025). Trustworthy and Ethical AI for Intrusion Detection in Healthcare IoT (IoMT) Systems: An Agentic Decision Loop Framework. Journal of Healthcare Informatics Research, Springer.

🔒 Ethical Compliance

All experiments comply with PhysioNet and HIPAA de-identification standards.
The MIMIC-IV Demo dataset was used under credentialed access and contains no PHI.

🧾 License

This project is released under the MIT License, allowing free use for research and educational purposes.
