===============================
Day 25: Tuesday, April 8, 2014
===============================

0. Read https://httpd.apache.org/docs/2.2/ssl/ssl_intro.html and 
   http://blog.hartleybrody.com/https-certificates/

1. `Fill out the quiz <https://docs.google.com/a/msu.edu/forms/d/1gCxIzWO9atp6787FFyBFrxDSuK-vMOuX6BAhEQ4LKPs/viewform>`__

2. Discussion.

3. Git exercises from :doc:`day24`.

4. Other stuff

   SQL loading & Python modules.

       1. See setup() in imageapp/__init__.py `(link) <https://github.com/ctb/cse491-serverz/blob/day24-ice/imageapp/__init__.py#L14>`__; this contains stuff that you only run once an app. It's in a function so you can choose to run it or not to run it (e.g. for tests)

       2. See imageapp/image.py `(link) <https://github.com/ctb/cse491-serverz/blob/day24-ice/imageapp/image.py>`__.  The 'images = {}' will be run on import, no matter what you do.  There's no way to disable it, in particular.

       tl;dr? Almost always put code in a function.

       Q: where should you put database creation/data model definition code? (See sqlite/create.py `(link on day23 branch) <https://github.com/ctb/cse491-serverz/blob/day23/sqlite/create.py>`__

   More git reading: http://who-t.blogspot.com/2014/03/using-git-next-level.html

   A quest for understanding Web stuff: http://jakearchibald.github.io/request-quest/


.. Check everything out.  Can you run it?

.. Web testing/selenium.

.. Parallel foo.
