# Git Policies

This document outlines how programmers should interact with club Git repositories.

## Repository Structure 

We generally adhere to the [git flow](https://nvie.com/posts/a-successful-git-branching-model/) repository model. While the exact specifics of this can be seen at the link, the basic structure is summarized in [this document](https://nvie.com/files/Git-branching-model.pdf). 

For robot repositories, releases should correspond to a competition, or other relevant deadline (e.g. running skills at a high school event). Hotfixes should only ever be made during competitions. Release names should reflect this, e.g. a release for the 2023 ASU Polytechnic competition, Tussle for the Southwest, should be named Tussle for the Southwest.

For non-robot repositories, release numbers should follow the [Semantic Versioning](https://semver.org) specification.

## Commit Naming 

Commit names should follow [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/). 

## Making Changes

This section outlines the process by which changes to the code should be made. This encompasses all changes, including new features (e.g. code for controlling a new subsystem).

Changes should be made as follows:
1. Create an issue detailing the change, with the relevant label(s)
2. Create a branch off of the relevant branch for the specific issue
3. Work on the changes in the new branch
4. Create a pull request into the relevant branch, including a reference to the issue 
5. Wait for a repository maintainer to accept the pull request

