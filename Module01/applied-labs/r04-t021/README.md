# R04-T021: Token-Budget Preflight Example

A deterministic, local whitespace-token preflight check demonstrating how incoming prompts are evaluated against a configured token budget before inference on resource-constrained edge devices.

## Files
- `example.py` — Implements `check_token_budget(prompt, budget)` using whitespace splitting.
- `test_example.py` — Unit tests covering normal, boundary, empty-input, and negative-budget scenarios.

## Prerequisites
- Python 3 standard library only (no external packages, model downloads, or GPU required).

## Usage & Verification

- **Run the standalone concept example:**
  `python3 Module01/applied-labs/r04-t021/example.py`

- **Run the automated test suite:**
  `python3 -m unittest discover -s Module01/applied-labs/r04-t021 -p "test_*.py"`

## Scope & Limitations
- **Teaching Approximation:** Uses `prompt.split()` (whitespace tokenization) solely as a deterministic teaching approximation, **not** a real model tokenizer (such as BPE or WordPiece).
- **No Hardware/Model Claims:** Makes no claims regarding real edge device latency, memory usage, or trained model accuracy.
