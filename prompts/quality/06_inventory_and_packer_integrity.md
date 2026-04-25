# Jules Objective: Inventory Integrity & Packing Simulation Audit

You are a senior data integrity engineer acting autonomously. Your goal is to identify and resolve exactly 1 or 2 issues related to warehouse stock accuracy, inventory history consistency, or 3D packing simulation precision.

**Scope Restriction:**
Limit your investigation to the following files:
- `views/warehouse/`
- `utils/packer_service.py`
- `utils/geometry_processor.py`
- `models.py` (WarehouseItem and WarehouseHistory models)
- Related unit tests in `tests/` (e.g., `tests/test_warehouse_analytics.py`, `tests/test_packer_service.py`)

**Your Workflow (Do not ask for further instructions):**
1. **Analyze:** Read the files in your scope to find a data consistency or simulation flaw. Look for "off-by-one" errors in stock deductions, history entries that don't match the actual stock change, or voxel-grid collision detection edge cases in the packer.
2. **Reproduce:** Write a failing test or a specific simulation script that triggers the stock discrepancy or packing failure.
3. **Run Tests:** Execute `pytest` to confirm the bug.
4. **Fix:** Implement the fix. Use atomic database updates for stock if possible. If fixing the packer, ensure the 3-tier voxel logic remains performant.
5. **Verify:** Run the tests again to ensure data integrity is preserved and the simulation is accurate.
6. **Finalize:** Provide a concise summary of the inventory or simulation fix.

**Constraints:**
- Fix a maximum of 2 issues.
- Do not change the fundamental 3-tier voxel packing algorithm (L1/L2/L3).
- Ensure all warehouse history operations are correctly linked to item updates.
