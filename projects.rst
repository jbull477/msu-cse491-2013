========
Projects
========

.. image:: _static/2014-cse491-platform-diagram.png
   :width: 80%

Overall goal: implement features for an image
sharing/storage/leaderboard/editing Web site.  (So, please assume that
most features should be implemented on imageapp. ;)

Testing rules: apart from the testing specific projects, do enough
to make sure that your site works.  Heh.

Extension offer, in place next HW: before the homework is due, you can
ask for an extension until next Thursday, for help in solving
technical problems.  I will grant extensions where significant work
and problem solving has been tried but has failed.  I will then choose
another student to help you debug and fix your code via pull request
review; I will evaluate them on their PR comments, and you on your
fixed (or not) code.  Details still a bit fuzzy; ask questions.

0. Propose something that you've always been interested in learning!

1. Reimplement the imageapp functionality (minus the silly JavaScript)
   in your own app.py, or `Django <https://www.djangoproject.com/>`__
   or `flask <http://flask.pocoo.org/docs/>`__.  (5 pts each; app_framework)

2. Write a WSGI middleware component that does recording and playback
   of all WSGI traffic between server and component.  (5 pts; wsgi)

3. Swipe a template from oswd.org and put it in place on your imageapp
   server. (5 pts; browser_app)

4. Change imageapp to support JPEG and TIFF. (5 pts; app_feature)

5. Add a URL that provides a list of images, resized to thumbnails
   (you can just img size, not actual resizing -- that will be a
   separate project ;).  (5 pts; app_feature)

6. Add image "metadata" uploading, storage, and retrieval: image name,
   description, etc. (5 pts; app_feature)

7. Add image metadata search (find image by ...) (5 pts.; app_feature)

8. Add the ability to comment on images. (5 pts.; app_feature)

9. Add username login via cookies and tracking of image by "owner" (the
   person who uploaded it).  Allow the owner to delete it. (5 pts.; app_feature)

10. Implement secure cookies (see #9); use UUID.  (5 pts; app_feature)

11. Write something that prevents denial of services by uploading gigabyte
    files, or "forever" connections that upload things really slowly.
    Be sure to write a client-side test. (5 pts; app_feature)

12. Implement AJAX image upload with JQuery. (5 pts; ajax)

13. Implement a Python client to upload images via a JSON-RPC interface. (5 pts; api)

14. Write down clear instructions for setting up a new Ubuntu machine
    on a cloud service of your choice (I have some documentation for Amazon)
    and installing the imageapp server on port 80. (5 pts; hosting)

15. Add account creation, login, and authentication (5 pts; app_feature)

16. Add data persistence in sqlite or MySQL or PostgreSQL (5 pts; app_feature).  NOTE that you can use the CSE MySQL server, here: http://www.cse.msu.edu/Facility/Services/MySQL.php


17. Implement multithreading in your WSGI server (see http://docs.python.org/2/library/threading.html) and explain how you know it's working.  (5 pts; wsgi)

18. Implement multiprocessing (shared nothing in memory) in your WSGI server (see http://docs.python.org/2/library/multiprocessing.html) and explain how you know it's working (see :doc:`day28` code) (5 pts; wsgi)

19. Implement asynchronous I/O (not multithreading/multiprocessing, but still handling multiple connections) in your WSGI server, and explain how you know it's working. (5 pts; wsgi)

20. After #14, set up a domain name and static IP address for your site. (5 pts; hosting)

21. Write a chef recipe for installing your software from github on a Linux VM/
    cloud computer. (5 pts; hosting)

22. Make a thumbnail list using server-side resizing on the fly (in Python code, using PIL or some other image manipulation library). The distinguishing feature here should be that large images are not downloaded to the browser and resized there (as would happen if you used image attributes; see #5).  (5 pts; app_feature)

23. Write a URL handler so that each image is referred to by its number, e.g. /image_raw/10; make it so that going to the latest image in your imageapp redirects to the right image number. (5 pts; app_feature)

24. Make a generally useful fake data set to support #6 (~10-20 images, names, etc.) for others to use in testing their own server. (5 pts; platform)

25. Implement polling for your chat app. (5 pts; browser_app)

26. Implement Web sockets for chat app updating (5 pts; ajax)

27. Implement starring, ranking, and a simple recommendation system for your image app image list (5 pts; app_feature)

28. Add disqus to your Web site (2.5 pts; browser_app)

29. After #6, implement an RSS feed for new image uploads (2.5 pts; app_feature)

30. Add data persistence in a NoSQL database (5 pts; app_feature)

31. Reimplement the most basic imageapp functionality (uploading and serving images) in the `Scala Play framework <http://www.playframework.com/>`__. (5 pts; app_framework)

32. Reimplement the most basic imageapp functionality in the `Node.js framework <http://nodejs.org/>`__. (5 pts; app_framework)

.. add tests at all levels?

.. Implement error handling for no file, etc.

.. consistent styles

.. write Selenium tests

.. make tiny url
