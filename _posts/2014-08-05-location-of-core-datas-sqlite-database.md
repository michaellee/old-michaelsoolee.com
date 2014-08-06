---
layout: post
title: "Location of Core Data's SQLite Database"
categories: programming
---

When creating an iOS application with Core Data, an SQLite database is created to store all the persistent data for the application. I've found that when the data model is changed, the app will crash because the database doesn't reflect the model.

An easy way to mitigate this is to delete the SQLite database that Core Data creates and just have Xcode recreate the database for you.

To locate the SQLite database, in __Finder__, select __Go__ from the menu, then select __Go to Folder...__ and type in `/Users/username/Library/Application Support/iPhone Simulator/` where username is your home directory.
