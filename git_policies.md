# Git Policies

This document outlines how programmers should use git to manage the code base.

## General Rules

A universal set of policies, no matter the repository's purpose

1. The default branch for all repositories is `master` (aligns with the git default).
2. Code should NEVER be committed to the `master` branch. Code should be committed to a separate branch, pushed to GitHub, and a pull request should be opened to pull code into the `master` branch.
3. The `master` branch should only contain code that FOR SURE works. In other words, the master branch should be treated as a "release" branch, even though we won't have releases.

## Commit Rules

1. Git commit messages should be a complete description of what changes have been made in a commit.
2. Files included in a commit should all pertain to a single subsystem/change. For example, if there are changes made to both code for the drivetrain and code for an intake, two separate commits should be made, one containing the drivetrain changes and the other containing the intake changes.
3. In general, all commits should include more than one line. The first line is limited to 50 characters, while all other lines are limited to 72 characters.
    - The first line of the commit should summarize the changes made. Using the above example, a valid commit message for the drivetrain could be `Added various drivetrain autonomous functions`. While summarizing a change may be difficult in 50 characters, this ensures that commits are easy to understand
    - The following lines should go into more depth as to the specifics of the change. Using the above example, a second line in the hypothetical commit could be `Implemented drive_turn_angle function`. 

## Robot Repository Rules

Rules applying to repositories for robot code. These modify and extend the general rules

1. In addition to a `master` branch, all robot repositories should have a `dev` branch.
2. The `dev` branch serves a staging/testing ground for new code. Any code that needs to be tested should be merged into the `dev` branch and tested. Once the code is confirmed to have worked, the `dev` branch can be merged into `master`.
3. Code normally should not be committed to the `dev` branch. Code should be committed to a separate branch, pushed to GitHub, and a pull request should be opened to pull code into the `dev` branch.
4. Code may be committed to the `dev` branch in the case of very small changes, e.g. changing a motor port. In addition, changes made during a competition should be made in `dev`.
3. The first line of a commit should include which robot the commit is for, using the robot's name.
