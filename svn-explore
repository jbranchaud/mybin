#/bin/sh

# This is a collection of quick and dirty unix commands for exploring
# local SVN repositories. Read the description of each to see what it
# does.

# Get the number of authors for this svn repo
svn log -v --xml | grep '<author.*/author>' | sort $* | uniq | wc -l

# Get a list of the authors for this svn repo along with the number of
# commits they have made, sorted in decreasing order by commit count
svn log -v --xml | grep '<author.*/author>' | sort $* | uniq -c | sort -rn
