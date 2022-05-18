---
title: "Research Proposal"
date: 2022-05-17T17:03:08-05:00
description: My research proposal
menu:
    sidebar:
        name: Research Proposal
        identifier: proposal
        parent: starter-posts
        weight: 250
draft: false
---

### Introduction

The area of research that my project deals with is Python naming conventions. Specifically, I aim to evaluate names in Python files based on various criteria. I believe that there are many paths that I can take regarding this subject. As I continue my project, I will determine which direction I wish to go. As of now, I am looking at the area in terms of name length in conjunction with how descriptive that name is. There is no current criteria for this, but in general it can be assumed that longer names are generally more descriptive while shorter names are generally less descriptive. By evaluating this, readability, efficiency and linting problems can potentially be solved in Python programs. There are various issues that can be present in developers' code dealing with naming conventions. In general, there are not many measures in place to keep these conventions error-free and consistent. Rather, they are usually handled with a "common knowledge". This presents a problem for junior developers who may not yet possess this "common knowledge". For these reasons, a project that aids in evaluating these conventions could be largely useful for many developers.

While choosing my area of research and beginning my first assignments for this course, I did not initially land on the topic of naming conventions. Rather, I chose to explore the area of static code analysis in Python programs. This eventually led me to choosing my current topic. Though I did not stick with it, static code analysis directly ties into naming conventions. The project that I will be pursuing consists of a static analyzer itself. Knowing this, I believe that it is important to report the knowledge and the information I gained along the way through my process of researching different topics and ultimately switching them.

### Literature

Literature about Python static analysis is interesting because Python is not a static language. There are various static analyzers for it, but discussion begins at the idea of finding better ways to analyze its code statically like with C, C++ and Java. One [survey article](http://ceur-ws.org/Vol-2508/paper-gul.pdf) discusses this very idea. It looks at various static analysis methods and compares the advantages and limitations of each method. A lot of information can be gathered from the article's tasks that were addressed. Another [article](https://dl.acm.org/doi/pdf/10.1145/3238147.3240484) discusses the fact that there is a lack of software tools that can automatically analyze static Python code and create a static call graph from it. While I am not interested in the specific topic of the article, it emphasizes a commonality that is seen about Python static analyzers. The commonality with the analyzers is the lack of them. A third [article](https://dl.acm.org/doi/pdf/10.1145/3394451.3397205) once again emphasizes the same idea. It discusses how static analysis is widespread with static programming languages, but is still a challenge with dynamic languages such as Python.

I initially chose to focus on Python static analysis because I had previously completed a project that leveraged it. After seeing the information that many articles discussed, my interest grew further on the thought that I could create something to add into the realm of the area. With this thought process, I continued on to locate a knowledge gap that I could potentially fill with a project.

### Knowledge Gap

The knowledge gap that emerges from the area of static Python code analysis has to do with choosing analyzers to leverage in the CI of programs. As more analyzing tools are created, researched and experimented with, there is more of a "need" to implement them in addition to the existing tools. There are many great tools with great abilities, but a new challenge arises when too many tools are implemented for analysis: too much expense. Too many or too big of tools being run can be too expensive in terms of time and memory usage. This is not optimal in continuous integration to test software. There is not a definite fix to this gap/problem, but it is possible to analyze and experiment with various analysis tools to yield conclusions about it.

My thought process for this gap began by learning about symbolic execution in [this](http://ceur-ws.org/Vol-2508/paper-gul.pdf) article. The article mentioned how it could greatly improve error detection where most other tools are lacking. It is said to be very powerful, but the downside is that it is very expensive. This made me think of the gap in a more generalized way. From the way the author discusses symbolic execution, it is an essential tool that is needed to detect a specific type of error in many instances. Knowing this and knowing that it is also very expensive, I thought that there must be a way to look at tool-choice in terms of efficiency. Following the topic of symbolic execution, I looked into it more for Python and found [this](https://www.google.com/books/edition/Dependable_Software_Systems_Engineering/rykxCgAAQBAJ?hl=en&gbpv=1&dq=symbolic+execution+python&pg=PA26&printsec=frontcover) article that discusses dynamic symbolic execution (it is dynamic because Python is a dynamic language) with a tool that was created to handle it. This article was beneficial because it shows the recognition of the type of analysis and the creation of an easy and efficient tool for it. It breaks down an expensive process so that it can be better understood and implemented into developers' CI models. Another article that was interesting can be found [here](https://ieeexplore.ieee.org/abstract/document/8812141). It discusses reproducible failures and fixes, including things like TRAVIS-CI in the discussion. A toolkit is mentioned that deals with these failures and fixes, but what I got out of this article was that there are limitations in regard to expense in error detection. Lastly, a good resource that shows the existence of this gap is the comprehensive list of static analysis tools on GitHub found [here](https://github.com/analysis-tools-dev/static-analysis). The sheer amount of tools that are listed here for every programming language proves that there are too many analyzers to use all of them. They are all at developers' disposal, but a select few must be chosen to ensure an ideal efficiency.

A research question that I believed would have the ability to fill the knowledge gap is: How can a developer determine which static analyzers to use and when to stop adding more, specifically in the Python language? To answer this question, it is necessary to analyze analysis tools. I want to find out which analyzers offer the highest percentage of error detection in relation to each other as well as by themselves. I also want to find out how expensive various tools are. Identifying the main types of errors in Python programs will help to give me a list of which types of tools are necessary for any CI to be efficient and beneficial. From there, I can experiment to find out a good stopping point for adding tools based on the percentage of error detection and the expense. While static analysis is great, compilers also catch errors, so it can possibly be more efficient to skip static analysis steps in order to save time and memory when the compiler can do the job.

### Feasibility

In terms of feasibility, I thought that my initial project idea was adequate based on the information I had found thus far and the plan that I created to move forward. The tool that I wanted to create required only very basic hardware that every developer possesses. I would have also needed access to all of the Python static analysis tools that I deemed useful for my purpose, which are all accessible on GitHub. Besides those things, I believed that I had the necessary knowledge of the Python programming language, static analyzers and the ability to learn about libraries as needed. My idea also would have required data in the form of files in Python repositories. I planned to look at different file types in order to determine which particular set of analyzers would be best for a given project. The data retrieval for that purpose would have been feasible as well. Finally, the anticipated time to complete the project as well as running experiments to analyze results both looked very doable to me. While I still think that my initial project idea is feasible, I ran into trouble in the next step. My solution to fix the problem was to change my project idea.

### Prototype

As I began designing my prototype and thinking about how I would implement it, I ran into blockers that I could not get past. The feasibility of my project idea quickly deteriorated, so I changed it. As I mentioned in the introduction, my new project idea is to create a tool and run experiments with it that deal with Python naming conventions. Namely, I am interesting in looking at the length of names (for instance, variable names) in comparison with the amount of times they are used in the source code. The premise of this idea stems from the fact that names in source code need to be descriptive. When a user is reviewing source code, a name that is used multiple times needs to be more descriptive than a name that may only be used once or twice. In this way, those that attempt to understand the source code have a better chance of understanding it. It is fairly unreasonable to make every name long and descriptive, but it is a good idea to make prevalent names as descriptive as possible. My prototype address this directly by finding names in Python source code and measuring their character length.

There are two functioning features of my prototype that lay some of the framework for the future of the software tool. The first feature counts all assignments statements in the specified file(s). The second feature finds the length of each assignment statement name. Of course, as the project continues many other features will be implemented, but the two that exist are necessary in order to analyze names in more complex ways.

A basic design of my prototype was laid out ahead of time. It can be seen below.

![graphic](prototype-chart.jpg)

I was not able to implement a Poetry environment given the amount of time that I had, but the rest of the flowchart is accurate to the final product.

To develop this prototype, I leveraged a library called LibCST that I used in a previous project. I was familiar with using it for a similar purpose to find instances of various things in Python files. I was able to leverage some source code from the previous project and work off of it to create new functions.

The prototype that I created will provide a large amount of support for my project. I believe that I will be able to directly continue implementation on it to create a good sized tool. The main purpose of my prototype was to build the framework that would allow me to add further functions to accomplish new goals. Seeing as I accomplished that, I believe that I can move forward and expand.

### Experimentation

My main question that I aimed to answer with my experiment is: How descriptive are the assigned variables of Python programs? Though this is my research question, I was not able to answer it fully with the limited functionality of my prototype. Rather, I used the results that I was able to produce to draw conclusions about the descriptiveness of assigned variables.

My experiment began with choosing three datasets to run through my prototype tool. I chose to use three Python projects in the GatorEducator GitHub organization. I extracted all of the Python files from the main source directories of each project. This manual extraction made me realize that it is a very inefficient way to gather data. With all of the Python files in a separate folder in my prototype repository I was able to first run the `find-variables` command on each folder. I then ran the `find-variable-lengths` command on each file in each of the folders. I also realized that this method of running the tool on a large amount of data is inefficient and tedious.

In terms of the results that I obtained from my experiment, I ran the `find-variables` command to output a basic visualization of how many assignment statements were in each file of each directory. It is important to note that these are the found assignment statements, not necessarily standard variables. Upon running the command to output the lengths of the variable names, there were many instances of non-standard assignment statements. I implemented a feature in my prototype to catch these instances and return an error. So, I was able to look past these errors to analyze the data of all the standard variables.

In relation to the completion of my project, this experimentation has taught me a few important things. Firstly, it gave me experience with experimentation that will allow me to more easily create and complete new experiments. It also taught me that in order to set up an experiment properly, a strategic way of collecting data is necessary. Lastly, I learned that experiments may result in some data that I was not expecting, so I can be expected to handle such data. I will use these learning experiences as I run other experiments.

For a basic analysis I calculated the averages of the lengths of all the variable names in each file. I put the averages on bar graphs to visualize them.

![gatorgrader graph](gatorgrader_graph.jpg)
GatorGrader Averages

![gatorminer graph](gatorminer_graph.jpg)
GatorMiner Averages

![sheetshuttle graph](sheetshuttle_graph.jpg)
SheetShuttle Averages

These results showed a basic depiction of how descriptive the variable names are for the various files in the three projects shown. Though, there is no real basis to leverage this information off of. So, it is more beneficial in this case to compare the length or variable names between files in the projects as well as the overall averages between them. It can be seen that there is a lot of variation in the GatorGrader project whereas there is not much in the other two. This shows that GatorGrader may lack consistency in this way. Looking at overall averages, GatorGrader has a value of 13.6980057, GatorMiner has 9.126903553 and SheetShuttle has 9.105882353. From this information it can be determined that the variable names used in GatorGrader are (on average) the most descriptive of the three projects. There are some things in this analysis that skew the results such as accounting for files with no assigned variables. Things like this should be looked at more carefully in future experimentation for more accurate results.

I decided to use the above visualizations because they are very basic and easy to understand for a wide audience. Also, the results of my experiment were not very complex to begin with, so a simple visualization was all that was necessary. In addition, these graphs can be used as a baseline when further results are yielded in the future.

### Ethics

On the surface I do not see any ethical concerns with my research. Naming conventions in the Python language is a very straightforward topic that does not contain much room for unethical behavior. Though, if any concerns arise, it is important that I recognize them. To deal with this, I will overview my work consistently with ethics in mind to ensure that I catch any potential concerns. If I do catch any problems, I will make it a priority to either change the way I continue my project or implement a strategy to resolve the it.

### Conclusion

The next steps to develop and complete my research project will start with backtracking to the initial few assignments of this course. I will complete more thorough research about Python naming conventions in order to see what other information exists. From there, I will continue to expand my tool so that it is more capable to run experiments with. With more research, implementation and experimentation, I believe I will be able to thoroughly complete my research project.