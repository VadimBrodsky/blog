---
layout: post
title: Ruby Command Line Switches
tags: ruby
date: 2021-04-25 06:26 -0400
---
Common command line switches for the `ruby` command:

`-c` switch
: Check the syntax of a program without executing it

`-w` switch
: Gives warning messages during program execution

`-e` switch
: Executes the code provided in quotation marks

```bash
ruby -e 'puts "code demo!"'
```

`-l` switch
: Line mode, prints a newline after every line of output

`-rname` switch
: Requires the named feature

```bash
ruby -rprofile
```

`-v` switch
: Shows the ruby version and executes the code in verbose mode

`--version` switch
: Shows ruby version information

`-h` switch
: Shows information about all command-line switches for the interpreter
