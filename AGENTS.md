# Codex Agent Instructions

## Repository Overview
This repository contains three course assignments and one final project.

- assignment2/main.ipynb  
  Reference implementation for classification tasks.

- assignment3/main.ipynb  
  Reference implementation for segmentation using Implicit Neural Representations (INR).

These notebooks are provided as READ-ONLY references.

## Authoritative Project Specification
The final project requirements are defined in:

- project/PROJECT_SPEC.md

This file is the authoritative source of truth for:
- project goals
- constraints
- required components
- deliverables

Do not deviate from these specifications unless explicitly instructed.

## Development Scope
- You MAY read and inspect:
  - assignment2/main.ipynb
  - assignment3/main.ipynb
- You MUST NOT modify anything inside:
  - assignment1/
  - assignment2/
  - assignment3/

All new code, experiments, and notebooks must be created inside:

- project/

## Final Code Output
- The final implementation must be contained in a single notebook:
  - project/final_project.ipynb
- This notebook must be runnable end-to-end on Google Colab.
- Do not create multiple alternative notebooks.

## Working Methodology
Do NOT attempt to solve the entire project in a single iteration.

Instead, proceed using incremental subtasks.
Before each subtask:
- Briefly state what the subtask will achieve.
- List which files will be modified or created.

After each subtask:
- Perform a minimal sanity check (e.g., forward pass, small training run, visualization).
- Do not continue if the sanity check fails.

## Recommended Subtasks (to be executed sequentially)
1. Repository inspection and planning:
   - Inspect assignment2/main.ipynb and assignment3/main.ipynb.
   - Identify reusable components (data loading, model structure, training loop).
   - Propose a clear execution plan.

2. Data handling:
   - Implement data loading utilities inside project/.
   - Ensure compatibility with the data format used in assignment3.

3. Soft-label target generation:
   - Implement conversion from hard segmentation masks to soft targets
     (e.g., signed distance fields or equivalent).
   - Validate correctness with visualizations.

4. Model adaptation:
   - Adapt the INR model for regression output.
   - Remove or replace classification-specific layers or activations.

5. Loss functions and metrics:
   - Implement regression losses (e.g., L1 as primary).
   - Define appropriate evaluation metrics.

6. Training pipeline:
   - Integrate model, loss, and data pipeline.
   - Run a minimal training loop to verify convergence.

7. Baseline comparison:
   - Reproduce a baseline derived from assignment3.
   - Ensure fair comparison under the same data splits.

8. Cross-validation and robustness:
   - Implement patient-aware data splitting and cross-validation.
   - Log metrics per fold.

9. Ablation experiments:
   - Implement controlled ablations (loss type, target representation, etc.).
   - Collect results for later analysis.

## Constraints
- Prefer explicit, readable code over compact or clever solutions.
- Avoid unnecessary refactoring.
- Do not introduce new dependencies unless strictly necessary.
- Use fixed random seeds where applicable.

## Communication Style
- When unsure, ask for clarification before proceeding.
- Explain decisions briefly in markdown cells when helpful.
