---
layout: post
title: "Create a new Jekyll project in an existing folder"
category: work
---

Creating a new Jekyll project without an existing project folder is simple. Just run `jekyll new project_name` and the Jekyll command line tool will automatically create a new folder called `project_name` and scaffold all the files you new for a new Jekyll project.

But let's say you've got an existing folder that you wanted to use for a new Jekyll project. There are a couple of ways to achieve this.

The first method is by first entering into the existing folder by using `cd existing_folder` replacing `existing_folder` with the name of the folder you desire to use for your new Jekyll project. Once you're in the project folder, type in this Jekyll command `jekyll new . --force`. Like before we're telling the Jekyll command line tool to generate a new Jekyll project. `.` indicates that we want to create the new project in the current folder we're in and the `--force` option is to tell Jekyll to force this command. The force option is needed because by default, the Jekyll tool won't run the `new .` command in an existing, non-empty folder.

The second method, you don't have to be in the existing folder; simply run this command `jekyll new existing_folder --force`. Like the command run in the first method, this will create a new Jekyll project in the non-empty folder called `existing_folder`.

Creating a new Jekyll project in an existing folder also doesn't replace any existing files, it just adds the Jekyll specific files. This is a good benefit if you've already versioned the folder. In your next commit all you have to do is push up the new Jekyll specific files.
