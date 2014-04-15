===============================
Day 27: Tuesday, April 15, 2014
===============================

.. 0. Read http://debuggable.com/posts/understanding-node-js:4bd98440-45e4-4a9a-8ef7-0f7ecbdd56cb.  See also http://www.nodebeginner.org/#building-the-application-stack.

0. Read http://en.wikipedia.org/wiki/Asynchronous_I/O

----

On branch day27, I've changed image.py `(link) <https://github.com/ctb/cse491-serverz/blob/e7d764c23d432f4d8cd96384f788dc27167d0421/imageapp/image.py>`__ to do SQLite saving/loading of images.

Look at the changes to server.py on day27-threading `(link)
<https://github.com/ctb/cse491-serverz/commit/99d75eb7f6573957d1b8c6624075e77a4d3a4271>`__
and day27-async `(link)
<https://github.com/ctb/cse491-serverz/commit/a6b65dd37b340afa03e0a0cb2ad8012fa7f39dc6>`__.

Question -- does the 'add_image' function (lines 35-54) in `image.py
<https://github.com/ctb/cse491-serverz/blob/e7d764c23d432f4d8cd96384f788dc27167d0421/imageapp/image.py>`__
need to be protected from concurrent execution in (a) threading and (b) async?

If (a) threading is YES and (b) threading is YES, choose pink.

If (a) threading is YES and (b) threading is NO, choose green.

If (a) threading is NO and (b) threading is YES, choose yellow.

If (a) threading is NO and (b) threading is NO, choose blue.


----


.. ---

.. presentation on no parallel processing, shared process space, non-shared
.. process space.

.. in web stuff: i/o is the biggest deal.  can I find that article on critical
.. times? use stuff from NGS course?

.. discuss critical sections; global interpreter lock, +=, modules/globals

.. none, async (tulip), multithreading, multiprocessing.inside of sqlite-enabled
.. imageapp.

.. for each approach
.. - which ones have shared process space
.. - mark where potential critical sections are
.. - mark where non-Python locking is needed

.. how would you figure this out?
