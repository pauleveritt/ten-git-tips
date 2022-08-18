# Repo for August 2022 Git webinar

## Intro
- “Ten” was a lie, we have some warm-up tips first
- Refer to related material
- Marco’s [Git and IntelliJ IDEA 5 tricks you should know](https://www.youtube.com/watch?v=Ase_X9p6exw)
- Michael’s [Up and Running with Git Course](https://training.talkpython.fm/courses/up-and-running-with-git-a-pragmatic-ui-based-introduction)
- Michael Kennedy's [PyCharm webinar from June](https://www.youtube.com/watch?v=2aqFz5p1Jdg)
  - You should use VCS and in a GUI, color coding, diff compare, visualize branches, commit/merge
  - Clone, add to git
  - Status
  - Merging changes
  - Check out branches
  - Creating branches
  - Local history
  - PR management
  - Merging branches
  - Create Gist
  - Casual blame discovery
- [VCS tips](https://www.jetbrains.com/pycharm/guide/topics/vcs/) in the [PyCharm Guide](https://www.jetbrains.com/pycharm/guide/)
- Marit’s [interactive rebase video](https://www.jetbrains.com/idea/guide/tutorials/git-interactive-rebase/) 

## Local History

First Git tip? Don’t use Git! This one is fast, I can point them at the Guide page as well as Michael Kennedy’s June webinar.

- Start in our ten-git repo
- Add two Markdown files
- Go to delete one, but accidentally delete the other.
- Show Commit window…nothing git can do to help you.
- Use local history to restore it.
- Learn your lesson, add them both.
- Make a change to one.
- Uh-oh, the previous text, I need it back.
- Git can’t help you.
- Use Local History to get it back.

## Git Console

Pre-start of Marco’s. I want to show this one, then use the console all along the way.

## Reword Message

This one is fast, I can point them at the Guide page.

- Scenario: Just used a crappy commit message
- Reword the commit
- Show console to see what was done behind the scenes

## Undo Last Commit

This one is fast, I can point them at the Guide page.

- Scenario: The last commit was wrong, I don’t want punctuation
- Have commit window open
- I could edit all the files, do a new commit
- I haven’t pushed yet
  - Sidebar: Marco explain the “haven’t pushed to a protected branch”
- Undo last commit
  - Explain changelist
- Show the resulting commit window
- Show console to see what was done behind the scenes

## Amend Commit

This one is fast, I can point them at the Guide page.

- Scenario: change the title punctuation to have a period, in all files
- Do for first one, commit
- Use a crappy commit message
- But really, we should do it for all, then commit
- Do for the rest
- Amend commit
- Show console to see what was done behind the scenes

## Partial Commit (file, section of a file)

- This one is fast, I can point them at the Guide page.
- Scenario: The set of changes has some things I like, some that I’m not done with yet
- Change title in three Markdown files, to add back the punctuation
- Edit the body in two of the files, delete one of the files
- I want to commit, but just the title-oriented changes
- Let’s me show partial commit both in file contents (only title) and a file (don’t commit the delete)
- Show console to see what was done behind the scenes

## See Changes in Gutter

This one is fast, I can point them at the Guide page.

- Scenario: Visually see what’s different in a file, perhaps do some operations
- Start with a longer file
- Do some add/edit/delete
- Show the coloring
- Click on the coloring
- Show the various operations

## Rebase Feature Branch

Start of Marco’s tips. We’ll consider this a transition into “intermediate”.

- Scenario: Feature branch and main gets updated
- Your video explains the scenario, let’s just do it
- I’m on a feature branch here
- Marco, while we’re talking, makes a change and pushes it to main
  - In this case, not in a file I’m changing
- I come back to work today, how do I know?
- The branch window has a blue down arrow
- Open Git tool window
- Make a good habit of doing “Update”...do so now
- The swimlanes changed
- Marco explain what it is saying
- We want those changes, in our feature branch….without a merge
- Marco: explain the idea behind rebasing
- Marco’s video has two ways to get those changes: fetch, then rebase…vs. In one step. We’ll do the latter.
- Remote branch | Main | Pull into (current branch)
- Show the Git Log to see what the swimlanes look like
- Show console to see what was done behind the scenes

## Squash

- Very similar to Marco’s video
- Edit a Markdown file
- Make a wording change, commit, repeat 3 times
- Git Log, select the 3 commits
- Right-click, Squash
- Show console to see what was done behind the scenes
- Repeat the changes and commits
- Launch interactive rebase and quick explanation
- Mention Marit’s video

## Compare with Branch

- Scenario: Been on the feature branch a while, 
- Prep: Have a feature branch at the beginning that gets out of sync with all the work done here
- Make a change on this branch, commit, push the branch to remote
- Then, switch to that “at-the-start” branch
- I forget to get up to date
- Instead, I make some changes and commits on “at-the-start”
- Show and discuss the git log:
- Main has had some commits from Marco
- The branch we were just working on, goes further
- This feature branch is out of date
- How can I see?
- Branch menu | Main | Compare with at-the-start
- Explain top and bottom
- Select a commit, double click on one of the changes
- Explain diff view
- Bonus tip: discuss forks and upstreams


## Merged Commit View

Scenario: Similar idea, but you want to see changes in lots of commits instead of branches
Go to Git Log
Select a few commits
Right-hand side now shows the combined changes

## Pull Request Review

Reference Michaels’ video for list open/closed, conversation, local checkout
Scenario: Dependabot housekeeping
Open one of my projects
Choose a PR
Merge it
OPTIONALLY: Marco and I actually do a PR interaction in the Guide
