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

5. Trigger a workflow which deletes worflow runs in the repository using a scheduled event.

6. Manually trigger a workflow (`workflow_dispatch`) which sets up Python (version is retrieved using an input) and prints the Python version.

7. Manually trigger a workflow (`repository_dispatch`) and show the content of the client payload.
   <details>
     <summary>Solution</summary>

   ```bash
   curl \
   -X POST \
     -H "Accept: application/vnd.github+json" \
     -H "Authorization: Bearer <YOUR-TOKEN>" \
     https://api.github.com/repos/SoheilSalmani/github-actions-activities/dispatches \
     -d '{"event_type": "show_payload", "client_payload": {}'
   ```

   </details>

8. Create a workflow to auto-assign issues to you on creation.

9. Create a workflow (triggered manually) to show details of the runner workspace.

10. Create a secret at the repository level and another at the environment level with the same name but with a different value. Create a workflow to print the secret value.

11. Create a Slack workspace, a Slack App, and a workflow to notify a new release version on tag creation. Delete the workspace, and Slack App when you check that everything is working.

12. Create a workflow to translate non-English issues content to English.

13. Create a new repo and a workflow to lint all commit messages on pull requests.
