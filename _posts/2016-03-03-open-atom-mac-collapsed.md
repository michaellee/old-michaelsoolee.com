---
layout: post
title: "Open Atom with project folders collapsed from the Mac Terminal"
category: work
---

Atom has become my text-editor of choice. One of the features that I use the most is Atom's command-line tool available in Terminal. The command-line tool provides the `atom` command which could be used to open files and folders from the command-line into Atom.

I often use `atom .` to open the entire current folder I'm in, usually a project folder with many sub-folders and files. My only complaint with this feature was, Atom would always remember which of the folders were expanded the last time I had the project folder open. This feature definitely has its perks, but I usually like to open up a project and have all folders collapsed.

I haven't been able to find an option in Atom to turn this off permanently, but I did discover by accident, that you can open the current folder from the Terminal and have all folders collapsed. Instead of opening the folder with `atom .`, open it with `atom ,`. What `,` seems to trigger is the action for Atom to launch and have a blank file with the `,` being the name of the file. For this reason, passing in an actual file name like `readme.txt` will have the same effect.

I'm not sure if this is a bug that will get fixed in the future (I'm using version 1.5.4), but it definitely mitigates a behavior I wanted to sometimes avoid with Atom.
