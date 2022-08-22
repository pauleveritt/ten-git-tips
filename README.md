# Repo for August 2022 Git webinar

## Before Webinar

- Browser tab
  - https://github.com/pauleveritt/antidote-book/pulls 
- IDE
  - This repo (duh)
  - antidote-book project

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

First Git tip? Don’t use Git! This was in Michael Kennedy’s June webinar. 
Also, see the [Guide Tip](https://www.jetbrains.com/pycharm/guide/tips/local-history/).

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
- Fix the titles, do a (bad message) commit. 
- Marco: Discuss local history's policies (how far back, change boundaries) 

## Git Console

Pre-start of Marco’s. I want to show this one, then use the console all along the way.

- Marco: Give your pitch for why the Git console matters
- Open it, show the last couple of git commands
- 
## Reword Message

Just used a crappy commit message. What now? Easy -- let the IDE help you clean it up.

This one is fast, for more detail, check out the [Guide Tip](https://www.jetbrains.com/pycharm/guide/tips/reword-commit-message/).

- Reword the commit
- Show console to see what was done behind the scenes
- Note the "Undo" in notification
- Marco: Implications if you have pushed 

## Undo Last Commit

The last commit was wrong, I didn't change the body to match the page number!

This one is fast, for more detail, check out the [Guide Tip](https://www.jetbrains.com/pycharm/guide/tips/undo-last-commit/).

- Have commit window open
- I could edit all the two files, do a new commit
- I haven’t pushed yet
  - Sidebar: Marco explain the “haven’t pushed to a protected branch”
- Undo last commit
  - Explain changelist
- Show the resulting commit window
- Fix those two Markdown bodies and commit
- Show console to see what was done behind the scenes

## Amend Commit

Committed too fast, have a little more work to do.

- Scenario: change the title punctuation to have a period, in all files
- Amend commit
- Click the commit in the log, show the files changed in that commit
- Show console to see what was done behind the scenes

## Partial Commit (file, section of a file)

The set of changes has some things I like, but also -- some that I’m not done with yet.

This tip is fast, for more, see the [Guide Tip](https://www.jetbrains.com/pycharm/guide/tips/partial-commit/).

- Change title in three Markdown files, to remove the punctuation
- Edit the body in two of those same files
- Delete one of the files
- I want to commit, but just the title-oriented changes
- Let’s show partial commit both in file contents (only title) and a file (don’t commit the deletion)
- Show console to see what was done behind the scenes

## See Changes in Gutter

Visually see what’s different in a file, perhaps do some operations.

This one is fast, for more detail, see the [Guide Tip](https://www.jetbrains.com/pycharm/guide/tips/see-changes-in-gutter/).

- Start with a longer file (this README)
- Do some add/edit/delete
- Show the coloring
- Click on the coloring
- Show the various operations

## Rebase Feature Branch

You're on a feature branch and main gets updated.

Start of Marco’s tips. We’ll consider this a transition into “intermediate”.

- I’m on a feature branch here
- Marco: Make a change to `page4.md` and push it to main
  - In this case, not in a file I’m changing
- I come back to work today, how do I know?
- The branch window has a blue down arrow
- Open Git tool window
- Make a good habit of doing “Update”...do so now
- The swimlanes changed
- Marco: Explain what the Git Log swim lane view is saying
- We want those changes, in our feature branch….without a merge
- Marco: explain the idea behind rebasing
- Marco’s video has two ways to get those changes: fetch, then rebase vs. In one step. We’ll do the latter.
- Remote branch | Main | Pull into (current branch)
- Show the Git Log to see what the swim lanes look like
- Show console to see what was done behind the scenes

## Squash

Messy commit history? Clean it up!

- Very similar to Marco’s video
- Edit a Markdown file
- Make a wording change, commit, repeat 3 times
- Git Log, select the 3 commits
- Right-click, Squash
- Show console to see what was done behind the scenes
- Repeat the changes and commits

## Compare with Branch

We have a feature branch `at-the-start` from before the webinar. It has gotten 
out of sync with all the work done here. But how exactly?

- Make a change on a feature branch, commit, push the branch to remote
- Then, switch to that “at-the-start” branch
- I forget to get up to date
- Instead, I make some changes and commits on “at-the-start”
- Show and discuss the git log's swim lanes
- Marco: Add a commit to main and push
  * I don't yet see them 
  * Need to update to fetch 
- The branch we were just working on, goes further
- This feature branch is out of date
- How can I see?
- Branch menu | Main | Compare with at-the-start
- Explain top and bottom
- Select a commit, double-click on one of the changes
- Explain diff view
- Marco bonus tip: discuss forks and upstreams

## Merged Commit View

Similar idea, but you want to see changes in lots of commits instead of branches.

- Go to Git Log
- Select a few commits
- Right-hand side now shows the combined changes

## Pull Request Review

Reference Michael's video for list open/closed, conversation, local checkout.

It can be a lot of work to handle pull requests: reviews, checking code locally. For 
example, dependabot PRs. The IDE can help.

- Show antidote-book in browser
- Switch to antidote-book in PyCharm
- Choose a PR
- Merge it
