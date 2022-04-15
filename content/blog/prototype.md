---
title: "Prototype"
date: 2022-04-14T14:04:29-05:00
description: Developing a prototype to prove the feasibility of my project.
menu:
    sidebar:
        name: Prototype
        identifier: prototype
        parent: starter-posts
        weight: 250
draft: false
---

As I began designing my prototype and thinking about how I would implement it, I ran into blockers that I could not get past. The feasibility of my project idea quickly deteriorated, so I changed it. My new project idea is to create a tool and run experiments with it that deals with Python naming conventions. Namely, I am interesting in looking at the length of names (for instance, variable names) in comparison with the amount of times they are used in the source code. The premise of this idea stems from the fact that names in source code need to be descriptive. When a user is reviewing source code, a name that is used multiple times needs to be more descriptive than a name that may only be used once or twice. In this way, those that attempt to understand the source code have a better chance of understanding it. It is fairly unreasonable to make every name long and descriptive, but it is a good idea to make prevalent names as descriptive as possible. My prototype address this directly by finding names in Python source code and analyzing them based on preset standards (that will likely change with experimentation).

There are two functioning features that lay some of the framework for the software tool. The first feature counts all assignments statements in the specified file(s). The second feature finds the length of each assignment statement tuple. As one would expect, the output for each statement is usually 1. For the feature in mind to be completed, the tuple needs to be separated by characters in order to find the length of the variables. Many other features will be implemented as the project continues.
