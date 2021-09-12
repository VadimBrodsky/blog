---
layout: post
title: Git Grep
tags:
  - git
  - grep
  - unix
date: 2021-09-08 10:38 -0400
---
Git has a pretty useful implementation of Grep that is recursive by default and respects `.gitignore`

## Useful options

- `-i` same as `--ignore-case` ignores the case sensitivity
- `-w` same as `--word-regexp` match patterns at word boundaries
- `-v` same as `--invert-match` selects non-matching lines
- `-h` hides the filename for each match
- `-l` same shows only the file names of files that contain the matches
- `-O` same as `--open-files-in-pager[=<pager>]` opens the matching files in the pager, pager can be configured in `core.pager`
- `-n` same as `--line-number` prefix the line number to matching lines
- `--break` print empty lines between matches from different files
- `--heading` show the filename above the matches instead of the start of each line
- `-<num>` show <num> leading and trailing lines for a match
- `-A <num>` show <num> trailing lines per match
- `-B <num>` show <num> leading lines per match
- `-C <num>` show <num> of context lines before and after the match 
- `--` signals the end of options, the rest of the parameters are <pathspec> limiters


## Examples:

```bash
# Looks for '// todo' (case insensitive) and open files in nvim buffers 
git grep -i -Onvim  '^// todo' .

# Looks for time_t in all tracked .c and .h files in the working directory and its subdirectories.
git grep 'time_t' -- '*.[ch]'

# Looks for solution, excluding files in Documentation.
git grep solution -- :^Documentation
```