# The Hunt for the Maltese Python

![The Maltese Python](https://camo.githubusercontent.com/b8aee1312eb314c5146ba9fe39b137bbae8219df15685384d93545537736082e/68747470733a2f2f63732e616c6c656768656e792e6564752f73697465732f646c756d616e2f636d7073633130302f636d7073632d3130302d6d616c746573652d707974686f6e2e706e67)

|Date |       |
|:----|:------|
|16 January 2026 |Assigned |
|23 January 2026 |Due |
|Progress        |[![Grade](../../actions/workflows/main.yml/badge.svg?branch=main)](../../actions/workflows/main.yml) |

![](https://img.shields.io/badge/assignment-lab-yellow.svg?logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABAAAAAQCAYAAAAf8/9hAAAACXBIWXMAAAB2AAAAdgFOeyYIAAAAGXRFWHRTb2Z0d2FyZQB3d3cuaW5rc2NhcGUub3Jnm+48GgAAAa9JREFUOI2Vkk1IVGEUhp9zvd7bfKNz51JojQWZkARmI2qCULjrbxkTs4nCVRC0LHeuZhGzDFqEKzcGs2vXxhatAxUhUTQt1I0mNkzZ/NzjYrBmplFu7+bjvOfl4ZyPIzTRtZR2BcKVWs9SPs/nZLMxazcDBBajmQkyXowYwMY2X7OvyAK5UADH4kM0gokbOksBurnNSslltlnWamZ+mpGdwk+KAEGF8uo67tK07IYGAKhU37Ly67jMiYA/ASGSL3DqvwDJxxp3bVoAygE/oobiYEq90AD9TV+snXYAxybm+5QqQl9oQOIs48bBB3BbaL1/iyHP51EoQDKtYy+eckfkrxe1sZ+Mk0ymdexEwEBaEw9TvPQMHVrbELh8nuF7t3k+kNZEbavukEau87q3hzNbu2zs7JH/vkf+XAfexS4uWBbujREuvZ9lCrhbw67q6gO9+SbLO+NQ99sKWiiyXzzgwEQwW/usTWZ4tvBWPtZPYDFoWqu33zC9tDnEcaq130avwhBQDxBhfnGduc7TxBshR6oowfIa36yAuX9WAOhPabcKPccBAERZXcjJl6P6EOkCeLyZu19AAAAAAElFTkSuQmCC)

> My way of learning is to heave a wild and unpredictable monkey-wrench into the machinery.
>
> Dashiell Hammett, _The Maltese Falcon_

In 2021, a professor attempted to boggle their students' minds by sending them a game 
in which there is hidden a **Golden Python**, a totem of unbelievable power and wealth. Being 
the forgetful professor they are, they forgot where they put it! The location of the Maltese 
Python remains a mystery to this day...

Can _you_ find it in the maze of directories where the computer system took it? _Enter to test your worth..._

## Learning Objectives

This assignment addresses the following course learning objective(s):

2. Implement code consistent with industry-standard practices using professional-grade integrated 
development environments (IDEs), command-line tools, and version control systems.

In addition to this goal, this assignment serves as your introduction to several of the tools 
that we will use throughout the course. Practice moving around a _file system_ and using 
_terminal commands_, while part of the above learning objective constitutes more than just a benchmark: 
it's a fundamental skill that you can get better at _very quickly_ (just ask your TLs).

## Helpful Commands

Don't forget your terminal commands!

|Command |Purpose                    |
|:-------|:--------------------------|
|`cd`    |`C`hange `D`irectory       |
|`ls` or `dir`|`l`i`s`t a `dir`ectory|

> ![NOTE]
> To run these terminal commands, you can type them directly in the terminal!

In addition, you've been given some sleuthy commands:

|Command |Purpose                    |
|:-------|:--------------------------|
|`uv run detect`|Detect hidden doors        |
|`uv run capture`|Capture the python!       | 

>![NOTE]
> To run these commands, you need to use `uv`. Run either command using the following
> terminal format:
> ```bash
> uv run NAME_OF_PROGRAM
> ```bash
> To run `detect`, for example, type: `uv run detect`

### `capture`

Capture requires an additional _argument_:
```bash
uv run capture NAME_OF_FILE
```
The program will only indicate success if you've found the `maltese-python`!

### `detect`

Detect finds secret doors. If you find a door in a "room" (folder), the terminal will respond:
```bash
This room seems a bit drafty...
```
If you see the above message, there's a `.hidden-passage` in the directory. Try to `cd` to it!
