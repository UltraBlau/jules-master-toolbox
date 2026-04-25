# New Feature Flow 2: Subagent Parallel Implementation

This workflow uses Jules to accelerate feature development by parallelizing the frontend and backend work based on an agreed-upon API contract.

## Stage 1: The Contract (Human)
The human developer defines the API contract (e.g., a Swagger/OpenAPI spec or a simple JSON schema in a Markdown file like `specs/api_contract_user_profile.md`).

## Stage 2: Parallel Dispatch (Jules)
Dispatch two Jules agents simultaneously to build both sides of the feature.

**Backend Agent:**
```bash
jules new "Read specs/api_contract_user_profile.md. Implement the Flask route and SQLAlchemy database models to fulfill this contract. Ensure the endpoint returns exactly the specified JSON structure."
```

**Frontend Agent:**
```bash
jules new "Read specs/api_contract_user_profile.md. Build a React component in frontend/src/components/UserProfile.jsx that fetches data from this endpoint and displays it. Handle loading and error states."
```

## Stage 3: Integration (Human)
The human developer reviews both PRs, merges them, and verifies the end-to-end integration. Jules handled the boilerplate and isolated implementation, saving hours of context-switching.