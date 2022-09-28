# GitHub Actions Activities

## Automating Workflows with GitHub Actions

1. Create a new repo using the GitHub CLI.
   <details>
     <summary>Solution</summary>

   ```bash
   gh repo create
   cd new-repo
   gh repo view --web
   ```

   </details>

2. Create an issue for `README.md` content.

3. Configure the `master` branch to require a pull request before merging. Configure approvals before merging a PR. Set the required number of approvals before merging to 1. Do not allow administrators to bypass these protections.

4. Edit the `README.md` file and create a pull request. Add a task list. Link the previous issue to the pull request. Merge the pull request.
