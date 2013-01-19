mybin
=====

this is a collection of random scripts that I have written and put on my path
to save time or do cool things.

It is assumed that if you want to run any of these scripts that you will stick
them somewhere that is on your system's path.

pyv
---

This is a small python script to get the version of a python module. It was
inspired both by me wrestling to find version numbers for various modules and
by this [StackOverflow answer](http://stackoverflow.com/a/4939465/535590) that
showed me how.

To run: `pyv [-v] name`

Example 1: `pyv lxml` -> `3.0.2``

Example 2: `pyv -v lxml` -> `lxml 3.0.2 (/Library/Python/2.7/site-packages)`

Example 3: `pyv not_a_module` -> `No distribution named not_a_module`

jekyll-post
-----------

This is a python script that creates and initializes a Jekyll post file. This
eliminates the need to remember all the yaml options that need to go into a
Jekyll post when most of them are pretty standard in the first place. Once I
got to having 4 or 5 yaml options, I figured I would create this to save time
on starting a new post.

To run: `jekyll-post [-D Dir] [-d date] [-w] title`

- `title` - the title of the post wrapped in quotes
- `-D`/`--Dir` - specify the directory (absolute or relative) in which the new file should be written
- `-d`/`--date` - specify a date in the format YYYY-MM-DD or leave out to default to today's date
- `-t`/`--tags` - specify a set of tags for the past separated by spaces with the whole thing wrapped in quotes
- `-w` - this flag signals to open the new file in an editor (default is vi)

The `title` option in the yaml will be initialized to the given title.

The default file extension is `md` which is markdown.

The rest of the yaml options will be initialized as specified in the script. If
you need different yaml options, just modify the portion of the script where
these lines are written to the file.

Example 1: `jekyll-post "First Jekyll Post"` which will generate a file in the
current directory with a name like 2013-01-01-First-Jekyll-Post.md.

Example 2: `jekyll-post -D _posts "How to Shotgun a Beer"` which will generate
a file in the _posts directory (relative to the current directory) with a name
like 2013-01-01-How-to-Shotgun-a-Beer.md.

Example 3: `jekyll-post -d 2012-12-31 "Happy New Year"` will generate a file in
the current directory with the name 2012-12-31-Happy-New-Year.md.

autotex
-------

This script can be run in the background for a LaTeX project to auto-compile
the tex files to PDF whenever they are modified. The initial implementation
is a bit hacked together because of some issues working with the Watchdog
script, but it gets the job done.

To run: `autotex main`

- `main` - the main tex file that needs to be called with pdflatex

Example 1: `autotex paper.tex` which will start the Watchdog-powered script
to start monitoring the directory where that tex file is located.

licenseme
---------

This python script is to be run from inside a project to generate a file called
README that contains license information. Currently, only the MIT license is
supported, but other open source licenses will be supported soon. The persons
name and the copyright year need to be hardcoded in the existing template
LICENSE file for now. Options for specifying this info as well as a config file
will be added soon.

To run: `licenseme [-n Name]`

- `-n` - optional tag to specify the name of the license that you want to use.

Example 1: `licenseme` which will generate a file named LICENSE in the current
directory.

Some useful links:

- [Open Source Initiative](http://opensource.org/licenses/)
- [Pick a License, Any License](http://www.codinghorror.com/blog/2007/04/pick-a-license-any-license.html) - [Coding Horror](http://www.codinghorror.com/blog/)

License
-------

Copyright (c) 2012 Josh Branchaud

License under the MIT License

