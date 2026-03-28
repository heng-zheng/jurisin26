# Repository Overview

This repository contains materials for extracting and reviewing legal propositions (LPs) from the Summary of Argument sections of U.S. Supreme Court briefs.

## Files

- `prompt.txt`  
  The prompt used to instruct the LLM to extract contestable legal propositions from Summary of Argument paragraphs.

- `annotation_protocol.md`  
  The protocol followed by the expert to review and refine LLM-generated legal propositions.

- `soa_lp.ipynb`  
  The Jupyter notebook used to extract legal propositions from Summary of Argument sections using Llama-3.1-8B-Instruct.

- `final_jurisin_cleaned_public.csv`  
  The dataset containing expert review results of model-generated legal propositions, along with additional propositions identified by the expert after reviewing the Summary of Argument.

## Dataset Columns

lp_id - Unique identifier for each legal proposition

case_group - Case identifier. In consolidated cases, multiple case numbers are grouped together using "|" (e.g., 24-656|24-657)

brief_role - Role of the brief (e.g., petitioner or respondent)

brief_uid - Unique identifier for each brief

model_name - Name of the model that generated the legal proposition

lp_text - Text of the legal proposition

lp_source - Source of the legal proposition, such as model-generated or expert-added

decision - Expert review decision for the legal proposition; accept, reject, edit, and split apply only to model-generated legal propositions after expert review, while not applicable is used for legal propositions added by the expert

reject_reason - Reason for rejection when the decision is rejected

evidence_para_ids_joined - Paragraph ID or IDs supporting the legal proposition

evidence_text - Text of the supporting paragraph or paragraphs
