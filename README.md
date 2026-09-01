# Activity 1: The Hunt for the Maltese Python

|Item |       |
|:----|:------|
|Week |Week 2, Monday |
|Type |In-class activity |
|Due  |End of the class session |
|Progress |[![Grade](../../actions/workflows/main.yml/badge.svg?branch=main)](../../actions/workflows/main.yml) |

> My way of learning is to heave a wild and unpredictable monkey-wrench into the machinery.
>
> Dashiell Hammett, *The Maltese Falcon*

A professor once hid a **Maltese Python**, a totem of unbelievable power, somewhere in a maze
of directories. Being forgetful, they lost track of where they put it. Your job is to find it
and bring it back to the cage.

You will not write any Python code in this activity. You will move around a file system using
a terminal, which is the skill everything else this semester sits on top of.

## Course learning outcomes

This activity addresses the following course learning outcome:

**CLO 2.** Implement code consistent with industry-standard practices using professional-grade
integrated development environments (IDEs), command-line tools, and version control systems.

Specifically, by the end of this activity you should be able to:

* describe what a working directory is, and say which one you are in at any moment
* move up and down a directory tree with `cd`, including using `..`
* list the contents of a directory with `ls`, including entries that begin with a dot
* run a program from the terminal and pass it an argument
* explain why a file being "hidden" is a convention rather than a security feature

## Commands you will need

|Command |Purpose |
|:-------|:-------|
|`pwd`   |**P**rint **W**orking **D**irectory: where am I right now |
|`ls`    |**L**i**s**t what is in this directory |
|`ls -a` |List **a**ll entries, including hidden ones that start with a dot |
|`cd NAME` |**C**hange **D**irectory into `NAME` |
|`cd ..` |Go up one directory, toward the root |

Two more commands come with this repository:

|Command |Purpose |
|:-------|:-------|
|`uv run detect` |Check the room you are standing in for a hidden passage |
|`uv run capture FILENAME` |Try to capture the python |

`detect` takes no arguments. Run it from inside a directory. If that directory contains no
hidden passage, it answers `Nothing to see here. Might move on...`. If it does contain one:

```text
This room seems a bit drafty...
```

When you see that, there is a `.hidden-passage` in the room. It starts with a dot, so plain
`ls` will not show it. Use `ls -a`, then `cd` into it.

`capture` takes one argument: the name of the file you think is the python. Run it from
inside the directory that holds the file, not from somewhere else:

```text
uv run capture maltese-python.png
```

It will only report success if you have actually found the right file.

## What to do

1. Clone this repository and open a terminal in its folder.
2. Run `pwd` first. Read the output. That is where you are.
3. Explore. The house starts in `src/`. Use `ls`, `cd`, and `cd ..` to move around.
4. Use `uv run detect` in rooms that look like dead ends.
5. When you find the python, `cd` into the room it is in and capture it. `capture` puts a
   copy in the `cage/` directory for you.

> [!TIP]
> If you get lost, `cd` with no argument returns you to your home directory, which is
> probably not where you want to be. Better: run `pwd`, read it, and walk back up with
> `cd ..` until you recognize where you are. Getting lost and recovering is the actual
> skill here.

## Evaluation

In-class activities are graded on completion and contribute to the **In-Class Activities**
category on the syllabus (10 points, averaged across the semester). This activity is worth one
activity grade.

|Level |What it looks like |
|:-----|:------------------|
|**Complete** |`capture` reported success, so `cage/maltese-python.png` exists, and you can retrace how you got there |
|**Partial** |You navigated the maze and found the hidden passage, but did not finish the capture |
|**Incomplete** |No meaningful navigation attempted |

The automated check confirms one thing only: that `cage/maltese-python.png` exists. Run it
yourself with:

```text
uv run gatorgrade --config .gatorgrade.yml
```

> [!NOTE]
> Automated results are preliminary. Your instructor sets the final grade.

## Why this activity exists

Every lab after this one asks you to run commands in a terminal, in a specific directory, on
files you have to find. Students who are shaky on `cd` and `ls` spend the rest of the semester
fighting their tools instead of the actual problem. One class session spent getting genuinely
comfortable here pays for itself many times over.
