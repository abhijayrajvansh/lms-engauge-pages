# GitOps Workflow

## Post-Completion Checklist

After every agent task completion, perform these exact steps:

1. **Type check** – run `bunx tsc --noEmit` and fix any reported errors before proceeding.
2. **Stage changes** – add each modified file explicitly with `git add <file>`. Do not use `git add -a`.
3. **Commit** – create a commit message using the required format and length, e.g. `git commit -m "feat: describe 6-7 word change"` (replace the prefix with the correct type such as feat/fix/docs/style/refactor/perf/test).
4. **Push** – push the new commit to the current working branch with `git push origin <CURRENT_BRANCH_NAME>`.

These operations must be executed after every agent completion to keep the branch history synchronized with remote and to ensure the shared type-safe workflow remains intact.
