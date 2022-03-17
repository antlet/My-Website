---
title: "Exploring Peer-Reviewed Articles of the Literature"
date: 2022-03-16T14:04:29-05:00
description: Exploring Peer-Reviewed Articles of the Literature
menu:
    sidebar:
        name: Articles
        identifier: articles
        parent: starter-posts
        weight: 250
draft: false
---

### Survey Article from the literature


 - Citation of the article

 Gulabovska, Hristina, and Zoltán Porkoláb. "Survey on Static Analysis Tools of Python Programs." SQAMIA. 2019.

 http://ceur-ws.org/Vol-2508/paper-gul.pdf

 - In two or three sentences, discuss the goals of this article.

 The main goal of this article is to find ways in which static code analysis methods could be adapted for Python. This is the goal because static analysis is largely used for static-type languages such as C, C++ and Java.


 - What is /are the general task(s) that all the methods address in the article?

 The general task in the article is to compare the advantages and the limitations of each method. This consists of various static analysis methods.


 - What are some of the leading methods introduced and discussed in this paper?

 Some of the leading methods introduced and discussed in this paper are pattern matching, AST matchers and symbolic execution.


 - What is the context of the discussion of these methods? For instance, are there demonstrations in light of some task that they address?

 The methods that are discussed in this article are not highly technical, they are more-so explanatory. The basic way each analysis method works as well as the advantages and disadvantages are discussed.


 - How can some of these methods be used in your own work? What purpose would the method serve in your work?


 Because I have not yet narrowed down my research area, any of the methods discussed can be used in my own work. The article goes into many different analyzers form various different angles. I would be able to choose an angle and possibly look at various analyzers from there.


---

### First article from the literature

 - Citation of the article

 https://dl.acm.org/doi/pdf/10.1145/3238147.3240484

 - What is the goal of this article?

 This article discusses the fact that there is a lack of software tools that can automatically analyze static Python code and create a static call graph from it. A prototype Python tool named code2graph is introduced.

 - In about 100 words, please summarize the main goal of the article.

 The creators' goals for the article are described as twofold. The first goal is to help developers to understand the structure of a system. Secondly, their goal is to provide a way that readers/developers can use the tool in their own applications. They wish to provide a medium to aid them in furthering research and utilizing the tool.

---

### Second article from the literature

 - Citation of the article

 https://dl.acm.org/doi/pdf/10.1145/3394451.3397205

 - What is the goal of this article?

 This article discusses how static analysis is widespread with static programming languages, but is still a challenge with dynamic languages such as Python. It's goal is to look at a variety of static analysis in Python in regards to precision, time and memory usage.

 - In about 100 words, please summarize the main goal of the article.

 The goal of the article is to adapt three parameters: the value sensitivity, the allocation sensitivity and the activation of an abstract garbage collector. The adaptation of these parameters is done in order to examine the variation of Python static analysis. The creators do this in order to determine the level of sensitivity that is necessary to achieve meaningful Python analysis.

---

### Software Tools

 - code2graph
 - https://pypi.org/project/code2graph/

 This tool is the main topic of the second article that I found. It automates the tasks of: analyzing source code and extracting its structure, constructing static call graphs from it, and generating a similarity matrix of all the possible execution paths in the system.

 - PySym
 - https://pypi.org/project/pysym/

 This is a Python package that performs symbolic manipulation on a minimal scope. It is not a well-known package and it is not used in addition to other common analysis tools, but it is something worth looking into.

---
