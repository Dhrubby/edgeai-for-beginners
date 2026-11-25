# Verification Log — R04-T021

## Tool Versions
Python 3.14.7
git version 2.54.0 (Apple Git-157)

## Example Script Output
Prompt: 'one two three four' | Budget: 3
Preflight Result: {'retained_tokens': ['one', 'two', 'three'], 'retained_count': 3, 'removed_count': 1, 'truncated': True, 'tokenizer_note': 'Teaching approximation (whitespace split), not a real model tokenizer.'}

## Unit Test Output
test_empty_input_retains_none (test_example.TestTokenBudgetPreflight.test_empty_input_retains_none)
Empty or whitespace-only input retains no tokens. ... ok
test_exact_boundary_budget (test_example.TestTokenBudgetPreflight.test_exact_boundary_budget)
Prompt matching exact budget boundary retains all tokens without truncation. ... ok
test_negative_budget_rejected (test_example.TestTokenBudgetPreflight.test_negative_budget_rejected)
Negative budget raises ValueError. ... ok
test_truncation_over_budget (test_example.TestTokenBudgetPreflight.test_truncation_over_budget)
Budget 3 with 'one two three four' retains 3 tokens and removes 1. ... ok
test_within_budget_no_truncation (test_example.TestTokenBudgetPreflight.test_within_budget_no_truncation)
Prompt strictly within budget retains all tokens and removes none. ... ok
test_zero_budget_truncates_all (test_example.TestTokenBudgetPreflight.test_zero_budget_truncates_all)
Zero budget is valid and truncates all tokens. ... ok

----------------------------------------------------------------------
Ran 6 tests in 0.000s

OK
