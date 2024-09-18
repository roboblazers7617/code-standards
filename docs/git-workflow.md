---
layout: default
title: Git Workflow
---

# Git Workflow

The git workflow used by 7617 prioritizes stability, ease of collaboration, and ease of debugging. The general steps to contribute are listed below.

1. Create a branch
    * The name MUST be something simple and descriptive. A good example would be something like `vision-point-to-tag` or `shooter-accuracy-improvements`.
2. Make changes on that branch
    * You MUST commit frequently and SHOULD push often to help with collaboration.
3. Open a pull request
    * Add any labels that apply and mention anyone who is relevant to the component being modified.

Once a branch is ready to be merged and a pull request is opened, the pull request should be reviewed by another person and merged according to the steps below.

1. Review the code
    * The steps to do this can be found in the [Review Guidelines]({% link docs/review-guidelines.md %})
2. Once code is ready, merge it into main

# Merge guidelines

The main branch MUST remain stable. Any changes that are made MUST be made on a branch and MUST be tested and reviewed by at least one other person before being merged into main.

# Commit guidelines

Changes to the code MUST be committed frequently and incrementally to make narrowing down problems while testing code easier (reverting commits is easy, reverting changes within a commit is not). You MUST NOT commit once at the end of the day with a message like `End of practice` or `End of day 1`.

Commit messages MUST provide a clear and concise description of everything that the commit does, and commit descriptions MAY be used whenever more description is needed and to explain the reason why changes were made.

When committing from the programming laptop, you SHOULD add yourself as a co-author by appending `Co-Authored By: Name <E-mail>` to the end of your commit message.

# Pull Request guidelines

Pull request titles MUST provide a clear description of what the PR does (a good title should give the reviewer a good idea of what the PR is changing without any other context). Pull request descriptions MUST describe, in detail, the changes made, SHOULD explain the reason why changes are being made, and SHOULD provide any additional context that could be helpful while reviewing the PR (for example, anything that could potentially cause unexpected behavior should be documented).

Pull requests SHOULD be incremental changes in a similar manner to commits. While commits SHOULD be individual changes, PRs SHOULD be larger changes, usually either adding a feature or resolving an issue.

## Draft Pull Requests

If a change is taking a long time to complete, a draft PR SHOULD be created to track progress and aid with collaboration.

# Issue guidelines

When problems are encountered, issues SHOULD be created to track progress and aid with collaboration. If a branch or PR is created that resolves an issue, it SHOULD be linked to the corresponding issue. Any contributors who will be contributing code to resolve the issue SHOULD be marked as assignees in the issue, and any appropriate labels SHOULD be added.

# Issue / PR comments

Comments on issues and PRs SHOULD be used to track progress while working on resolving issues.

When information is needed or someone needs to see a comment for any other reason, relevant people SHOULD be mentioned so they are notified. When referencing commits, issues, PRs, or anything else that can be linked to, the references MUST be formatted such that GitHub will generate a link to their respective pages. Information on how to do this can be found [in the GitHub documentation](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/autolinked-references-and-urls).

# Git tags

Git tags MUST be created at the beginning and the end of every competition and MAY be created for any other large milestones. Tags MUST be named `vX.Y.Z`, in which `X` is incremented for every competition (starting at 0 for pre-competition tags), and `Y` and `Z` are incremented for milestone tags. Whether to increment `Y` or `Z` is at the discretion of the person creating the tag. Tag descriptions MUST include a short description of why the tag is being created (an example would be `v1.0.0` with the description `Start of Plainfield`).
