# Git Policies

This document outlines how programmers should interact with club Git
repositories.

## Repository Structure 

The primary branch of any repository should be named `main`.

`main` should be the only permanent branch in the repository.
Other branches should be created to address specific issues, and branch names
should describe the purpose of the fix.
In general, branches should only be merged into `main` by a programming lead.
For ordinary software team members or external developers, this must be through
a pull-request in Github.
Programming leads are allowed to merge their own code directly on the assumption
that they know what they're doing and have tested their changes.

## Commit Messages 

Commit messages should follow
[Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/).

The following commit types will be used most often, so new programmers should be
aware of these types especially:
- `fix`:
  Fixing a bug
- `feat`:
  Adding a feature
- `docs`:
  Editing or adding documentation, whether as comments in the code or in a
  separate file
- `refactor`:
  Changes to code that don't impact functionality e.g. changing a block of math
  to be more readable
- `chore`:
  Changes to files that don't actually change any code, e.g. changes caused by a
  change in how code is formatted.

Scope tags should be used liberally in order to specify where changes were made.
For example, for a bug fix for an intake on a robot named `jim`, the correct
commit tag should be `fix(jim-intake):
`.
This would be followed by a description of the fix.

For a more involved example, let's use the robot name `jim`, subsystem named
`catapault`, and let's say that we just fixed an issue where the catapault
motors weren't spinning in the same direction.
A good commit message for this scenario would be the following:
```
fix(jim-catapault): Fixed motors spinning in wrong direction

Previously, the motors were initialized such that the motors were both
reversed.
It turns out that in reality the lower of the two motors shouldn't be
reversed.
```
Note that each line should be limited to 72 characters in length, to ensure the
message can be easily read regardless of viewing method.

This repository is an exception to the commit message format, as all changes
could be considered `docs`.
Instead, all commits should start with the file being changed, e.g. Git
Policies: \<insert commit description\>

## Making Changes

This section outlines the process by which changes to the code should be made.
This encompasses all changes, including new features (e.g. code for controlling
a new subsystem).

Changes should be made as follows:
1. Create an issue detailing the change, with the relevant label(s)
2. Create a branch off of the relevant branch for the specific issue
3. Work on the changes in the new branch
4. Create a pull request into the relevant branch, including a reference to the
   issue
5. Wait for a repository maintainer to accept the pull request
