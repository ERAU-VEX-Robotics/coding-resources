# Git Policies

This document outlines how programmers should use git to manage the code base.

## General Rules

A universal set of policies, no matter the repository's purpose

1. The default branch for all repositories is `master` (aligns with the git default).
2. Code should NEVER be committed to the `master` branch. Code should be committed to a separate branch, pushed to GitHub, and a pull request should be opened to pull code into the `master` branch.
3. The `master` branch should only contain code that FOR SURE works. In other words, the master branch should be treated as a "release" branch, even though we won't have releases.

## Robot Repository Rules

Rules applying to repositories for robot code. These modify and extend the general rules

1. In addition to a `master` branch, all robot repositories should have a `dev` branch.
2. The `dev` branch serves a staging/testing ground for new code. Any code that needs to be tested should be merged into the `dev` branch and tested. Once the code is confirmed to have worked, the `dev` branch can be merged into `master`.
3. Code normally should not be committed to the `dev` branch. Code should be committed to a separate branch, pushed to GitHub, and a pull request should be opened to pull code into the `dev` branch.
4. Code may be committed to the `dev` branch in the case of very small changes, e.g. changing a motor port. In addition, changes made during a competition should be made in `dev`.
