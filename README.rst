Python / Flask - JavaScript Ajax Example
=======================

Demonstrates how to post form data and process a JSON response using
JavaScript. This allows making requests without navigating away from the
page. Demonstrates using |fetch|_, |XMLHttpRequest|_,  and
|jQuery.ajax|_. See the `Flask docs`_ about JavaScript and Ajax.

.. |fetch| replace:: ``fetch``
.. _fetch: https://developer.mozilla.org/en-US/docs/Web/API/WindowOrWorkerGlobalScope/fetch

.. |XMLHttpRequest| replace:: ``XMLHttpRequest``
.. _XMLHttpRequest: https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest

.. |jQuery.ajax| replace:: ``jQuery.ajax``
.. _jQuery.ajax: https://api.jquery.com/jQuery.ajax/

.. _Flask docs: https://flask.palletsprojects.com/patterns/javascript/


Install
-------

.. code-block:: text

    $ python3 -m venv .venv
    $ . .venv/bin/activate
    $ pip install -e .


Run
---

.. code-block:: text

    $ flask --app js_example run

Open http://127.0.0.1:5000 in a browser.


HOST - server
----

.. code-block:: text

Externally Visible Server

If you run the server you will notice that the server is only accessible from your own computer, not from any other in the network. This is the default because in debugging mode a user of the application can execute arbitrary Python code on your computer.

If you have the debugger disabled or trust the users on your network, you can make the server publicly available simply by adding --host=0.0.0.0 to the command line:



$ flask run --host=0.0.0.0

This tells your operating system to listen on all public IPs.


    $ pip install -e '.[test]'
    $ coverage run -m pytest
    $ coverage report
