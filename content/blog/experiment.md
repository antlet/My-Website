---
title: "Experiment"
date: 2022-04-27T14:04:29-05:00
description: My prototype experiment
menu:
    sidebar:
        name: Experiment
        identifier: experiment
        parent: starter-posts
        weight: 250
draft: false
---

My main research question or central goal is not something that is achievable with the limited functionality of my prototype alone. With the current functionality of it (after I finish the function to count characters in variables) I will attempt to answer a much smaller question that relates to what I will ultimately try to answer. This research question is: How descriptive are the assigned variables of Python programs?

The experimental findings that will answer my research question are the lengths of the assigned variables in given Python programs. My experiment will produce this data directly. It will output the amount of assignment statements and the character length of each assigned variable.

My experiment will begin by gathering multiple Python files from random Python projects on GitHub. I will then run my prototype with each file. Each time I run the prototype it will output the amount of variables in the file and the length of each variable. Based on these lengths, a basic insight as to how descriptive a Python file is based on the variables will be seen.

My experiment began with choosing three datasets to run through my prototype tool. I chose to use three Python projects in the GatorEducator GitHub organization. I extracted all of the Python files from the main source directories of each project. This manual extraction made me realize that it is a very inefficient way to gather data.

With all of the Python files in a separate folder in my prototype repository I was able to first run the `find-variables` command on each folder. I then ran the `find-variable-lengths` command on each file in each of the folders. I also realized that this method of running the tool on a large amount of data is inefficient and tedious.

I ran the `find-variables` command to output a basic visualization of how many assignment statements were in each file of each directory. It is important to note that these are the found assignment statements, not necessarily standard variables. Upon running the command to output the lengths of the variable names, there were many instances of non-standard assignment statements. I implemented a feature in my prototype to catch these instances and return an error. So, I was able to look past these errors to analyze the data of all the standard variables.

For a basic analysis I calculated the averages of the lengths of all the variable names in each file. I put the averages on bar graphs to visualize them. These results showed a basic depiction of how descriptive the variable names are for the various files in the three projects shown. Though, there is no real basis to leverage this information off of. So, it is more beneficial in this case to compare the length or variable names between files in the projects as well as the overall averages between them. It can be seen that there is a lot of variation in the GatorGrader project whereas there is not much in the other two. This shows that GatorGrader may lack consistency in this way. Looking at overall averages, GatorGrader has a value of 13.6980057, GatorMiner has 9.126903553 and SheetShuttle has 9.105882353. From this information it can be determined that the variable names used in GatorGrader are (on average) the most descriptive of the three projects. There are some things in this analysis that skew the results such as accounting for files with no assigned variables. Things like this should be looked at more carefully in future experimentation for more accurate results.