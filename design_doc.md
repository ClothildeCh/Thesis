# Routine Design Documentation

This project follows a modular NLP pipeline structure:

1. **Data Ingestion & Cleaning**: Load Trustpilot reviews and apply whitespace trimming, casing, and standardisation.
2. **Annotation Protocol**: Manual annotation of ~1,000 reviews into ACOS quadruples following predefined schema.
3. **Model Training**:
   - Prompt-based T5 model (`t5-small` → `flan-t5-base` could try in later versions)
   - Semi-supervised loop: human-corrected outputs reused for expansion
4. **Evaluation**:
   - Exact match, partial match, component F1, and error tagging
5. **Dashboard Output**:
   - Model predictions parsed and exported to Power BI for visualisation

All key modules are documented in code comments and the README.
