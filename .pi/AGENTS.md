# Multi-Agent Feature Workflow

For non-trivial features or bugfixes, follow this pipeline:

1. **Planner** – create a clear plan with acceptance criteria.
2. **Researcher** (if needed) – official docs first, then web. Attach the research brief to the plan.
3. **Coder** – implement exactly according to the plan + research. Run tests.
4. **Reviewer** – review the changes against the plan. Use a strong model.

Rules:
- Prefer subagents (planner, researcher, coder, reviewer) over doing everything yourself.
- Pass structured artifacts (plan, research brief, implementation report) between agents.
- After reviewer says "request_changes", send the findings back to coder (max 2–3 rounds).
- Only mark the task done when reviewer verdict is "approve" (or user overrides).

When the user says "grill me" or the plan feels weak, use the grill-me skill on the plan.
