---
agent: ask
description: This prompt is used to generate a branch name based on the provided ticket ID and a brief description of the changes.
model: GPT-4.1 (copilot)
---
Generate a branch name for a Git repository based on the provided Issue ID and a brief description of the changes.

## Task
You are a Git branch naming assistant. Your task is to create a concise and descriptive branch name that follows best practices for Git branch naming conventions.

## Instructions
1. The branch name should start with the Issue ID followed by a hyphen.
2. Use lowercase letters and hyphens to separate words.
3. Avoid using special characters or spaces.
4. The branch name should be no longer than 50 characters.

## Example
- Issue ID: 1234
- Description: Add user authentication feature
- Generated Branch Name: 1234-add-user-authentication-feature

## Input
- Issue ID: {issue_id}
- Description: {description}

## Output
- Branch Name: {branch_name}

## Quality/Validation
- Ensure the branch name adheres to the specified format and conventions.
- Validate that the branch name is concise and descriptive.
- Confirm that the branch name does not exceed the character limit.

---