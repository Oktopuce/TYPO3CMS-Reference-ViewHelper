.. include:: /Includes.rst.txt

.. _typo3-backend-modulelink:

==========
moduleLink
==========


Create internal link within backend.

Examples
========

Default::

    <form action="{be:moduleLink(route:'pages_new', arguments:'{id:pageUid}')}" method="post">
        <!-- form content -->
    </form>

Output::

    <form action="/pages/new" method="post">
        <!-- form content -->
    </form>

Arguments
=========


.. _modulelink_route:

route
-----

:aspect:`DataType`
   string

:aspect:`Required`
   true
:aspect:`Description`
   The route to link to

.. _modulelink_arguments:

arguments
---------

:aspect:`DataType`
   mixed

:aspect:`Default`
   array ()

:aspect:`Required`
   false
:aspect:`Description`
   Additional link arguments

.. _modulelink_query:

query
-----

:aspect:`DataType`
   string

:aspect:`Required`
   false
:aspect:`Description`
   Additional link arguments as string

.. _modulelink_currenturlparametername:

currentUrlParameterName
-----------------------

:aspect:`DataType`
   string

:aspect:`Required`
   false
:aspect:`Description`
   Add current url as given parameter
