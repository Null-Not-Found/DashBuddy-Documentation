# Git Strat

![branch management example](https://user-images.githubusercontent.com/81526735/233993084-f27b300c-e01b-4bfe-ab48-6f764cc31d91.png)

## Main branch rules:
1.	Only merge from hotfix and development, never commit.
2.	Only merge from development at the end of a sprint.
    1.	Before merging run all tests.
## Development branch rules:
1.	Only merge from feature branches, never commit.
    1.	When merging run all tests.
## Feature branch rules:
1.	When the feature originates from a Jira Issue then create it via Jira
2.	When committing to this branch use the Jira issue number in the commit message. For example, “NULL-69”.
3.	If needed it is allowed to merge development into feature, but never feature to feature.
## Hotfix branch rules:
1.	Only create a hotfix branch for small issues like typos or dev-based code.
2.	After merging back to main, delete the hotfix branch.
