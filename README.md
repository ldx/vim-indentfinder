# IndentFinder - vim plugin for automatically detecting indentation.

## Introduction

Indentation of external sources is a common problem. Some people use two
spaces, some four spaces, some tabulations, some mix tab and spaces. As soon as
you start editing external sources, you are likely to face a different
indentation. Then your careful editor setting will simply mess up the file you
edit unless the guy did use the same indentation as yours. And you may not
notice it. For example, if I indent with tabs, setting them to be displayed as
four columns and I edit a file indented with 4 spaces, all the lines I create
will be indented with tabs. They will render fine on my editor, but probably
not on someone else's editor. It is especially annoying when programming in
python as the indentation is part of the program structure.

Indent Finder is a python script that analyzes the text and tells you what
indentation is used inside it. The indentation analysis works on any
language. It was tested successfully with C, C++, python and Java code. This
plugin uses Indent Finder to find out the indentation type and automatically
adjust 'tabstop', 'softtabstop', 'shiftwidth' and 'expandtab' when a file is
opened.

## Requirements

To use indentfinder, vim must be compiled with *+python* enabled.

## Installation

Place `indent_finder.vim` in `~/.vim/plugin` and `indentfinder.txt` in
`~/.vim/doc`.

## Commands

### :FindIndent

The `:FindIndent` command detects the indentation used in the current buffer and
set the `tabstop`, `softtabstop`, `shiftwidth` and `expandtab` options
automatically. In case Indent Finder can't obtain information from the buffer,
the original indentation settings will be left unchanged. Note that the
detection will be performed automatically whenever a new file is read, so you
don't have to call `:FindIndent` unless you want to adjust the indentation
settings.

## About

This document was written by Timothy Lin (lzh9102@gmail.com).

Indent Finder was written by Philippe Fremy (phil@freehackers.org).

Copyright 2002 Philippe Fremy, All rights reserved.

Redistribution and use in source and binary forms, with or without
modification, are permitted provided that the following conditions are met:

- Redistributions of source code must retain the above copyright notice, this
  list of conditions and the following disclaimer.

- Redistributions in binary form must reproduce the above copyright notice,
  this list of conditions and the following disclaimer in the documentation
  and/or other materials provided with the distribution.

THIS SOFTWARE IS PROVIDED "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES,
INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND
FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE AUTHOR
BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR
CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE
GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION)
HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT
LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT
OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.

