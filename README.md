# Biomedical NLP for Drug–Target Relation Extraction
**From Classical Models to Transformers**

## Goal
Identify and classify chemical–protein relations in biomedical abstracts using NLP.

## Scope
1. Explore the ChemProt dataset and its annotation schema.
2. Build a TF-IDF + Logistic Regression baseline for relation classification.
3. Fine-tune and evaluate a biomedical transformer (e.g., PubMedBERT).
4. Compare macro/micro F1, precision, recall, and class-wise errors.
5. Optional: apply the model to COX-2 literature and review evidence with a pharmacologist.
6. Future extension: evidence-grounded biomedical question answering (RAG).

## Important methodology notes
- ChemProt labels describe annotated chemical–protein relations in text, not independently proven pharmacological effects.
- Preserve official train/development/test splits and avoid document leakage.
- Define the candidate entity-pair and no-relation policy before training.
- Do not use the test set for tuning.
- Record PubMed ID, entity pair, supporting text, predicted label, and confidence where available.

## Getting started
```bash
python -m venv .venv
pip install -r requirements.txt
```
Download ChemProt from its official source after reviewing the dataset license.
Place downloaded files in `data/raw/` (excluded from git).
Begin with `notebooks/01_data_exploration.ipynb`.

## Status
Project scaffold initialized; dataset ingestion and models not yet implemented.
