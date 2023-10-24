# Git Policies

This document outlines how programmers should interact with club Git repositories.

## Repository Structure 

Repository structure should be determined by the use case for the repository. There are two main options, [git flow](https://nvie.com/posts/a-successful-git-branching-model/) and [GitHub flow](https://docs.github.com/en/get-started/quickstart/github-flow).

The [git flow](https://nvie.com/posts/a-successful-git-branching-model/) repository model should be used for repositories where having specific versions makes sense. While the exact specifics of the model can be seen at the link, the author of the model also provides a [diagram](https://nvie.com/files/Git-branching-model.pdf) that outlines how the model works. Version numbers should follow the [Semantic Versioning](https://semver.org) specification.

On the other hand [GitHub flow](https://docs.github.com/en/get-started/quickstart/github-flow) should be used in repositories where having specific versions doesn't make sense. For example, this repository doesn't need versions, so GitHub flow makes sense. Similarly, robot repositories will not have dedicated versions, so Github flow makes more sense.

## Commit Naming 

Commit names should follow [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/). Scope tags should be used liberally in order to specify where changes were made.

The following commit types will be used most often, so new programmers should be aware of these types especially:
- `fix`: Fixing a bug
- `feat`: Adding a feature
- `docs`: Editing or adding documentation, whether as comments in the code or in a separate file
- `chore`: Changes to files that don't actually change any code, e.g. changes caused by a change in how code is formatted.

This repository is an exception, as all changes could be considered `docs`. Instead, all commits should start with the file being changed, e.g. Git Policies: \<insert commit description>

## Making Changes

This section outlines the process by which changes to the code should be made. This encompasses all changes, including new features (e.g. code for controlling a new subsystem).

Changes should be made as follows:
1. Create an issue detailing the change, with the relevant label(s)
2. Create a branch off of the relevant branch for the specific issue
3. Work on the changes in the new branch
4. Create a pull request into the relevant branch, including a reference to the issue 
5. Wait for a repository maintainer to accept the pull request

