# New Feature Flow 1: TDD Feature Scaffolding

This workflow integrates Jules at the very beginning of the feature creation process, using Test-Driven Development (TDD).

## Stage 1: The Spec (Human)
The human developer writes a detailed Markdown specification for the new feature (e.g., `specs/new_payment_gateway.md`), detailing the expected inputs, outputs, and edge cases.

## Stage 2: The Test Builder (Jules)
Dispatch Jules to read the spec and generate the complete, failing test suite.
**Command:**
```bash
jules new "Read specs/new_payment_gateway.md and write a comprehensive, failing test suite in tests/test_payment_gateway.py that covers all specified requirements and edge cases. Do not implement the feature itself."
```

## Stage 3: The Implementer (Human or Jules)
Now that the contract is defined by the failing tests, the human developer (or another Jules agent) implements the actual feature code until all tests pass. This ensures the feature exactly matches the initial specification.