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

License
-------

Copyright (c) 2012 Josh Branchaud

License under the MIT License

