# Workflow: Performance Optimization (The Speedster)

This workflow is used to identify and resolve performance bottlenecks, specifically database N+1 queries and slow business logic.

## Stage 1: Profiling (The Scanner)
Dispatch an agent to identify slow endpoints or functions using profiling tools or code analysis.

**Command:**
```bash
cat jules_master_toolbox/prompts/performance/02_database_and_performance_audit.md | jules new --repo <owner/repo>
```

## Stage 2: Benchmarking (The Evidence)
The agent MUST create a standalone benchmark script (e.g., `benchmark_slow_query.py`) that reproduces the bottleneck in isolation.

## Stage 3: Optimization
The agent applies optimizations (e.g., `joinedload`, batch updates, indexing) and runs the benchmark again to prove the speedup.

## Stage 4: Pull Request
The agent submits a PR with both the code fix and the benchmark script as proof of improvement.
