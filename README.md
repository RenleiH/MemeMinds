# MEMEMINDS: RAG-Enhanced GPT for Psychological Diagnosis

## Overview

**MEMEMINDS** is an innovative system combining **Retrieval-Augmented Generation (RAG)** with an ensemble voting mechanism to provide accurate, engaging, and contextually rich psychological diagnostics. The system leverages large language models (LLMs) and integrates external knowledge bases to refine diagnostic reasoning and reduce biases, achieving a diagnostic accuracy of **82.4%**.

This project highlights the potential of AI-driven solutions in making psychological support more accessible and efficient, focusing on entertainment-based self-awareness and exploration.

---

## Features

- **Hybrid Retrieval**: Combines FAISS and BM25 to fetch contextually relevant information from external knowledge bases.
- **Ensemble Voting**: Multi-agent collaboration ensures consensus, compensating for individual model weaknesses.
- **Interactive Dialogue**: Designed with a casual, engaging tone to foster self-reflection and reduce stigma around mental health.
- **Scalability**: Applicable to both synthetic and real-world mental health datasets.

---

## System Architecture

1. **Input Query**: User provides an initial query describing symptoms or mental states.
2. **Hybrid Retrieval**: FAISS and BM25 retrieve relevant knowledge chunks from external sources.
3. **Follow-Up Queries**: System generates clarifying questions using tuned LLMs to refine diagnostic accuracy.
4. **Ensemble Voting**:
   - Multiple LLM agents score candidate diagnoses based on retrieved context.
   - Two-stage voting refines results, ensuring robust and reliable outcomes.
5. **Response Generation**: Final diagnosis and recommendations are delivered with contextual reasoning.

---

## Dataset

- **500 Psychological Cases**:
  - 74 mental health conditions sourced from clinical datasets (e.g., MDD-5k) and AI-generated profiles.
- **Performance**:
  - Overall accuracy: **82.4%**.
  - Demonstrated potential for near-human diagnostic reasoning.

---

## Key Results

- **Accuracy**:
  - 412 correct diagnoses out of 500 test cases.
  - Outperformed baseline models by 30%.
- **Agent Collaboration**:
  - GPT-4o: 366 correct diagnoses.
  - GPT-3.5: 39 correct diagnoses.
  - GPT-4: 45 correct diagnoses.
  - Collaborative voting enhanced final diagnostic accuracy.
- **Consensus**:
  - Average final vote: 13.5/15, reflecting high agent agreement.

---

## Challenges & Limitations

- **Data Diversity**: Limited availability of real-world clinical datasets.
- **Ethical Considerations**: Privacy and potential misinterpretation of outputs.
- **Agent Performance Imbalance**: Variability in diagnostic contributions among agents.

---

## Future Directions

- Incorporate real-world clinical data to improve generalizability.
- Address ethical concerns with enhanced privacy safeguards.
- Expand system capabilities for complex mental health conditions.
- Optimize ensemble methods for better agent collaboration.

---

## Usage

### Requirements

- Python 3.8+
- FAISS
- MongoDB
- Transformers (Hugging Face)
- BM25 Retrieval Library

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/<your-username>/MEMEMINDS.git
   cd MEMEMINDS
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

### Running the System

1. Start the database and retrieval system.
2. You should first have the following:
1. MongoDB in your local environment
2. An OpenAI API key

To setup the environment, you should build the retrival database first,
Before that, you should put your OpenAI key in whereever it asks for.

You can run RetrivalDB.py to setup the retrival database automatically.
You should use wiki_raw.csv to set up the database described above, otherwise, the FAISS index will process for a very long time.
3. Execute the main script:
   ```bash
   python main.py
   ```
4. Interact with the chatbot and explore diagnostics.

---

## Contributors

- **Qihui Fan**: Retrieval system development, database setup.
- **Renlei Huang**: Prompt engineering, testing, and benchmark analysis.
- **Jianqing Ma**: UI design, system optimization.
- **Yujia Zhou**: Benchmark testing, results analysis.
- **Jiarong Zhu**: System testing and presentation design.

---

## Acknowledgments
- **References**: DSM-5 guidelines, MDD-5k dataset, and related AI research.

---
