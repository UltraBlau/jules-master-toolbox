# New Feature Flow 3: The "Finish My Thought" (Code Review & Polish)

This workflow uses Jules as a senior pair-programmer to polish a "rough draft" feature built by a human developer before it is merged.

## Stage 1: The Draft (Human)
The human developer writes the "happy path" implementation of a new feature. The code works, but it might lack error handling, logging, or unit tests. The developer opens a Draft PR.

## Stage 2: The Polisher (Jules)
Dispatch Jules to target the specific files modified in the Draft PR.

**Command:**
```bash
jules new "Review the recent changes in views/orders/routes.py. The happy path is implemented, but it needs production hardening. Add robust error handling (try/except blocks), structured logging for failures, and write a unit test in tests/test_orders_routes.py to cover the new logic."
```

## Stage 3: The Final Polish
Jules submits a patch adding the missing professional touches. The human developer reviews the hardened code and merges the complete, production-ready feature.