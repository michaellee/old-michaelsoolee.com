---
layout: post
title: "Git Submodules: How to Deal with a Project within a Project"
category: programming
---

I'm currently working on a project that contains code from another project. Both projects are versioned with Git pulling in from their respective repos. Both projects are worked on simultaneously and so I've run into instances where the main project complains about the sub-project.

When trying to commit changes, I kept getting errors that the project wasn't in .gitmodules. So I went snooping around and came across [this article](http://git-scm.com/book/en/Git-Tools-Submodules) on submodules within Git. Turns out submodules was made exactly for my scenario.

> It often happens that while working on one project, you need to use another project from within it. Perhaps it’s a library that a third party developed or that you’re developing separately and using in multiple parent projects. A common issue arises in these scenarios: you want to be able to treat the two projects as separate yet still be able to use one from within the other.

Excellent! To mitigate the complaints that Git had, all I had to do was create a `.gitmodules` file at the root of the top-level project. Then within it you define your submodule like:

```javascript
[submodule "projectname"]
  path = path/to/project
  url = https://github.com/michaellee/project.git
```

If you ever pull in different projects to use in your next project, be sure to look into Git submodules to avoid running into Git errors.
