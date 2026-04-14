# NeuroTutor

### A Hybrid Transformer and Reinforcement Learning Framework for Personalized Learning Path Optimization

---

## Overview

NeuroTutor is an intelligent tutoring system designed to personalize student learning using advanced AI techniques. The system models student knowledge, detects misconceptions, and dynamically recommends optimal learning paths to improve understanding and academic performance.

Unlike traditional systems that only evaluate correctness, NeuroTutor analyzes *why* a student makes mistakes and adapts accordingly, mimicking a human tutor’s behavior.

---

## Key Features

* Personalized learning paths using Reinforcement Learning
* Student knowledge modeling using Transformer networks
* Misconception detection and targeted remediation
* Confidence-based scoring using response time
* Multi-student profile support with persistent storage
* Structured prerequisite enforcement using a knowledge graph
* Advanced evaluation metrics (HITS@K, NDCG, F1, RMSE, MAE)
* Interactive dashboard for performance visualization

---

## System Architecture

The system is composed of three core AI modules:

1. **Transformer Model (Student Modeling)**
   Predicts knowledge mastery levels for each topic based on student interaction history.

2. **Reinforcement Learning Agent (PPO)**
   Selects the next topic and difficulty level to optimize learning outcomes.

3. **Knowledge Graph**
   Maintains prerequisite relationships between topics to ensure structured learning.

---

## Workflow

1. Student attempts a question
2. System evaluates correctness
3. If incorrect:

   * Detects misconception
   * Generates human-like feedback
4. Interaction is recorded
5. Transformer updates knowledge state
6. RL agent selects next topic and difficulty
7. Question is generated and presented
8. Process repeats

---

## Tech Stack

* **Language:** Python
* **Deep Learning:** PyTorch
* **Reinforcement Learning:** Stable-Baselines3 (PPO), Gymnasium
* **Data Processing:** Pandas, NumPy
* **Graph Modeling:** NetworkX
* **Database:** SQLite
* **Evaluation:** scikit-learn
* **Visualization:** Streamlit, Matplotlib

---

## Project Structure

```
its_system/

├── data/
│   ├── student_interactions.csv
│   ├── question_bank.json
│
├── modules/
│   ├── transformer_model.py
│   ├── knowledge_graph.py
│   ├── rl_agent.py
│   ├── question_selector.py
│   ├── misconception_detector.py
│   ├── feedback_generator.py
│   ├── misconception_logger.py
│   ├── student_profiles.py
│   ├── confidence_scoring.py
│   ├── enhanced_rl_env.py
│   ├── evaluation_metrics.py
│   ├── session_report.py
│
├── dashboard.py
├── train.py
├── evaluate.py
├── main.py
├── its_data.db
├── reports/
```

---

## Installation

Clone the repository:

```
git clone https://github.com/your-username/neurotutor.git
cd neurotutor
```

Install dependencies:

```
pip install torch stable-baselines3 gymnasium networkx pandas scikit-learn streamlit matplotlib
```

---

## Usage

### 1. Train Models

```
python train.py
```

### 2. Run the System

```
python main.py
```

### 3. Evaluate Performance

```
python evaluate.py
```

### 4. Launch Dashboard

```
streamlit run dashboard.py
```

---

## Evaluation Metrics

The system is evaluated using:

* Accuracy, Precision, Recall, F1 Score
* RMSE, MAE
* Learning Gain
* HITS@K
* NDCG
* Cumulative Reward

---

## Key Contributions

* Transformer-based student modeling (replacing traditional CRNN approaches)
* Reinforcement learning for adaptive learning path optimization
* Concept-level misconception detection
* Confidence-aware reward shaping
* Fully local implementation (no external APIs required)

---

## Advantages

* Personalized and adaptive learning experience
* Identifies exact conceptual gaps
* Provides human-like feedback
* Scalable architecture
* Works completely offline

---

## Limitations

* Requires a well-annotated question bank
* RL training can be computationally intensive
* Performance improves with more student data
* Feedback is limited to predefined templates

---

## Future Improvements

* Integration of lightweight local language models for richer feedback
* Dynamic question generation
* Explainable AI visualizations
* Integration with real-world educational datasets

---

## Team Structure

* Member 1: Transformer Model (Student Modeling)
* Member 2: Reinforcement Learning Agent
* Member 3: Data Processing and System Logic
* Member 4: Evaluation, Reporting, and Dashboard

---

## License

This project is for academic and educational purposes.

---

## Acknowledgment

This project is inspired by research on adaptive learning systems and reinforcement learning-based path optimization, extended with Transformer-based student modeling and practical implementation features.

---
