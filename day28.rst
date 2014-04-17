===============================
Day 28: Tuesday, April 15, 2014
===============================

0. Read http://debuggable.com/posts/understanding-node-js:4bd98440-45e4-4a9a-8ef7-0f7ecbdd56cb.  See also http://www.nodebeginner.org/#building-the-application-stack.

1. Quiz

2. Discussion

3. Next week's schedule: Tuesday (XSS and Selenium; DB; SIRS);
   Thursday (CTO `NastyGal <http://en.wikipedia.org/wiki/Nasty_Gal>`__, Grig Gheorghiu will speak via teleconf)

4. In class exercise on git merging.

In class exercise: git merging
------------------------------

Brief description: check out cse491-mergez
(https://github.com/ctb/cse491-mergez) and merge the fix_stddev and
listcomp branches into master.

Longer description:

   This code implements the calculation of standard deviation for a
   discrete random variable (see `the Wikipedia page
   <http://en.wikipedia.org/wiki/Standard_deviation#Discrete_random_variable>`__), with values taken from a single column text file.

   Two separate improvements have been made to the codebase.  Please merge
   them into a single branch.

Workflow:

1. Clone the repository::

      git clone https://github.com/ctb/cse491-mergez.git

2. Get all of the branches::

      cd cse491-mergez
      git fetch origin
3. Make sure you're on master::

      git checkout master

4. Get a list of branches, including remote ones::

      git branch -r

5. Make a new merge branch to do the merge on::

      git checkout -b try_merge

6. Merge in one of the two feature branches::

      git merge origin/listcomp

   and resolve merge conflicts, if any (see below).

7. Merge in the other feature branch::

      git merge origin/fix_stddev

   and resolve merge conflicts, if any (see below).

8. Go back to master. ::

      git checkout master

9. Merge the 'merge' branch in::

      git merge try_merge

10. Bask in the warm glow of success.

Resolving merge conflicts
-------------------------

When git merge encounters syntactically unmergeable code -- where one change
directly conflicts with the other branch -- it will annotate the code with
both versions::

   <<<< HEAD

    (one version of conflicting code)

   ====

    (other version of conflicting code)

   >>>> other

To clear this conflict, you need to (a) edit the code so it is
syntactically and semantically correct, which means removing the
``<<<<`` etc annotations; and (b) do a 'git add filename' for each
file you fixed, plus a 'git commit' to commit the changes.  Then
a 'git status' should report no conflicted files.
