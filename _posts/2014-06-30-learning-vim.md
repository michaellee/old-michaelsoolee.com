---
layout: post
title:  "Learning Vim"
link: http://csswizardry.com/2014/06/vim-for-people-who-think-things-like-vim-are-weird-and-hard/
categories: programming
---

I've tried learning how to use Vim in the past but like many folks who've attempted to learn it, I've given up out of frustration and what felt like an impossible feat to make Vim my primary text-editor.

After reading Harry's excellent blog post I'm excited to give Vim another shot and hopefully stick with Vim this time around.

Harry lays out some really great reasons as to why learning how to use Vim is useful. There were 3 points that pretty much drove it home for me.

> [Widely available] This is great for people who pair program a lot—you can use Vim on anyone’s machine. The amount of times I’ve been working on someone’s computer and been able to fire open Vim and be at home with it right away is really great.

Though two developers may use the same development environment, no two configurations are exactly the same. Being able to hop onto someone else's machine and be able to help the right away is a huge timesaver.

> Another huge benefit of Vim’s ubiquitous nature is, to put it bluntly, money.

There's nothing wrong with purchasing software. You should invest in software that will enhance your craft. But when a price tag gets in the way of your craft, I think that's a bummer.

Thanks to the Internet, learning to program has become very accessible. Having access to great software to program and create software should also be just as accessible. If you're working on a linux machine or a Mac, you already have Vim available to you.

> This level of composability yields fantastic results. Think about Subway for a moment. Subway, the sandwich place. They offer an array of ingredients, all laid out in front of you. These ingredients are very versatile, because they’re very easily combinable. You can make over a million different sandwiches at Subway out of the same common set of ingredients. Offering up these much smaller component-parts allows people to combine and compose an almost limitless amount of variations.

Growing up I loved playing fighting games such as _Street Fighter_ and _Tekken_ because beating your opponent was never linear. You have a set of moves your character can perform and you'd chain them together to defeat your opponent. In the same spirit, since Vim is based on single responsibility commands, you can chain together an endless combination of "moves" to accomplish your tasks.

Since I'm new to Vim, it's quite rewarding when I discover a new combination to improve my workflow.

## Give Vim a (another) chance

If you're like me and have attempted to learn how to use Vim before but gave up, check out Harry's blog post. It might convince you, like it has me to have another look at Vim.

If you're learning Vim for the first time, here are tips to help you:

- Endure through the pain - Using Vim is painful to my fingers since they aren't use to the new moves they are learning to perform, but it gets better. You're also trying to build muscle memory so it takes a little time but you'll get there.
- Disable your arrow keys - If your keyboard has arrow keys, check out <a href="https://github.com/csswizardry/dotfiles/blob/master/.vimrc#L110-L117" target="_blank">Harry's .vimrc file</a> to disable them. At first, you'll be reaching to use them, but having them unavailable will force you to use `hjkl` to navigate your document.
- Practice - No need to go cold turkey and replace your primary text-editor with Vim. I still use Sublime Text for most of my development but have tried to dedicate an hour or so a day in using Vim. I'm writing this post right now in Vim. This incremental shift is a lot easier then completely switching and has made the learning experience better.
- `vimtutor` - Before scouring the Internet for tutorials on how to use Vim, open up a terminal window and run `vimtutor`. I was surprised how good this little guide is in learning Vim.

Happy Vim-ing!
