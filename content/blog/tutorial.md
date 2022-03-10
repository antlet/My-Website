---
title: "Tutorial"
date: 2022-03-08T17:03:08-05:00
description: Tutorial for using Wily
menu:
    sidebar:
        name: Tutorial
        identifier: tutorial
        parent: starter-posts
        weight: 250
draft: false
---

# Wily

## Table of Contents

* [About](#about)

* [Features](#features)

* [Obtaining Wily](#obtaining-wily)

* [Setup](#setup)

* [Execution](#execution)

* [Helpful Resources](#helpful-resources)

### About

Describe the software resource and explain its relevance to your topic. Please include the link to the software resource.

- Wily is a command line tool that measures the complexity of Python source code by various means. It is able to iterate through git repositories and index the complexity of the files using various algorithms. The results of running Wily are able to appear on the console or on a graph in the browser of the user.
- A link to the software resource on GitHub can be found [here](https://github.com/tonybaloney/wily).

---

### Features

Outline the main features of the software. Why is this software necessary for your work?

- Wily is able to look back at a specified number of commits in a branch and analyze them. The first main feature is the ability to report a table of metrics for specified files. The table is displayed via the command line interface. There are various metrics that can be displayed, but the default metrics include the revision number, the author, the date, the number of lines of code, the number of unique operands, the cyclomatic complexity and the maintainability index.
- The second main feature of Wily is the ability to display an HTML graph in a user's browser. These graphs are able to display metrics, trends and date that are in the Wily cache. They are customizable in the sense that one or multiple metrics can be chosen as well as their axis.
- This software is necessary for my work because it directly deals with static Python code analysis. There are various ways to analyze static code, but I wanted to first choose something that analyzes complexity rather than linting or formatting. I think that the creators added a lot of useful features.

---

### Obtaining Wily

Where do you find this software resource? Is it an open source project? an online tool? How do you install it? Are there any libraries that are also necessary to install?

- Wily is an open source project/software resource that can be found on [GitHub](https://github.com/tonybaloney/wily). The tool also has a [documentation website](https://wily.readthedocs.io/en/latest/) that guides users through installation, running, and everything else that is necessary to know.
- It is a command-line tool, so most of its functionality happens in the console, but it also has capabilities of reporting results in browsers.
- It is installed on your machine simply through PyPi using Pip.
- There are not any libraries that are necessary to install in addition to Wily. The only basic things that are needed are Python and Pip (preferably the latest versions).

---

### Setup

Include steps of all necessary steps to get the software to run (for example, installations). Include the commands to run if necessary.

- In order for Wily to run on a user's source code, it is first necessary to install Python. Python's official download page can be found [here](https://www.python.org/downloads/). To ensure that the latest version is installed, users can run the command:

```
python --version
```

or

```
python -V
```

Once the latest version of Python is installed, Pip can be leveraged since it is already installed through Python. The latest version of Pip should also be used. The version can be checked by running:

```
pip --version
```

or

```
pip -V
```

The last step for installation is installing Wily via Pip with the command:

```
pip install wily
```

Once these steps are complete, Wily is ready to be used.

---

### Execution

How do you get the resource ready to use? Are there inputs to know? Please show a step-by-step guide (in a tutorial format) for readying the resource for your work. Include screenshots of successful execution and use of the software.

- To use Wily in the most basic and fundamental way, there is one command that is necessary to build an index in a Git repository. After this command, the tool is ready to be used with various other commands.

The path to the source code that the user wishes to use the tool with needs to be inputted with the `wily build` command:

```
wily build src/
```

Multiple directories can be used at a time if desired:

```
wily build src/ tests/
```

- Once this is completed, the tool is ready to be leveraged with source code. The `report` command takes the path to a file/directory and uses default metrics to display a report in the console. An example is shown below.

```
wily report castanet
```
![Report](/images/report.png)

- The `graph` command takes the path to a file/directory as well as a metric to display an HTML graph in the user's browser. An example is shown below using the `lines of code` metric.

```
wily graph castanet loc
```

![Graph](/images/graph.png)

---

### Helpful Resources

Include some of the relevant resources (links, articles, etc.) that you used to write in your tutorial.

- The GitHub repository that contains the source code as well as basic documentation for Wily can be found [here](https://github.com/tonybaloney/wily)
- THe official documentation website for Wily can be found [here](https://wily.readthedocs.io/en/latest/)
- The latest version of Wily can be found on PyPI [here](https://pypi.org/project/wily/)