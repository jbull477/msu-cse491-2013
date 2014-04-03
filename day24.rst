===============================
Day 24: Thursday, April 3, 2014
===============================

0. Read http://www.aosabook.org/en/integration.html

1. `Fill out the quiz <https://docs.google.com/a/msu.edu/forms/d/1fM7YUDia7xyB0Ge42BmuKUB1y_0-G_8AnOrWcnGpP-c/viewform>`__

2. Discussion.

3. In-class exercises (see below).

----

In-class exercises
~~~~~~~~~~~~~~~~~~

1. In pairs, look at http://jobs.msu.edu.  Try searching for two different
   job postings (4698 and 7617, for example).  Can you communicate these
   to your partner via an e-mailed URL? Try sending each other the URL of
   the different job.

   What is the mechanism the site is using to keep track of what job you're
   looking at?  What's a better way?

2. Check out branch 'day24-ice' of ctb's cse491-serverz, provided by a student::

      git clone https://github.com/ctb/cse491-serverz.git day24-ice -b day24-ice

   and run the imageapp, 'cd day24-ice; python server.py -A image'.

   In pairs, have one person log in to the same server as
   'user1'/'user1' and the other as 'user2'/'user2'.  Now check to see
   who you are logged in as.

   What's the mechanism the site is using to keep track of who you're logged
   in as?  What's a better way to do this?

   Note: if you're all alone, you can do this with two different incognito
   windows opening onto the same server.

3. Check out 'day24-ice' as in #2.

   In imageapp/templates/base.html, check out the two different ways
   of including style sheets in your HTML -- play around with uncommenting,
   and looking at the effect on the output.  Do both work?  Which is
   the "right" way to do this, and why?

4. Check out cse491-textz::

      git clone https://github.com/ctb/cse491-textz.git

   and, using 'git diff', figure out at which commit we lost the white
   rabbit.

   Specifically, you can use 'git log' to see the commit history; 'git
   checkout <commit prefix>' to check out specific versions of the
   repo; 'git diff <commit prefix1>..<commit prefix2>' to diff between
   two repos.  'git checkout master' will get the tip of the master
   branch back.

   Note that the white rabbit is present in the initial git commit,
   '58f7df'::

      cd cse491-textz
      git checkout 58f7df
      grep rabbit cities.txt

   but absent in the tip::

      git checkout master
      grep rabbit cities.txt

5. Check out cse491-textz as in #4; use 'git blame' to figure out at
   what commit the name Defargo was introduced into the text.
