.. include:: /Includes.rst.txt

.. _typo3-backend-link-editrecord:

===============
link.editRecord
===============


Use this ViewHelper to provide edit links to records. The ViewHelper will
pass the uid and table to FormEngine.

The uid must be given as a positive integer.
For new records, use the :ref:`<be:link.newRecordViewHelper> <typo3-backend-link-newrecord>`.

Examples
========

Link to the record-edit action passed to FormEngine::

   <be:link.editRecord uid="42" table="a_table" returnUrl="foo/bar" />

Output::

   <a href="/typo3/record/edit?edit[a_table][42]=edit&returnUrl=foo/bar">
       Edit record
   </a>

Link to edit page uid=3 and then return back to the BE module "web_MyextensionList"::

   <be:link.editRecord uid="3" table="pages" returnUrl="{f:be.uri(route: 'web_MyextensionList')}">

Link to edit only the fields title and subtitle of page uid=42 and return to foo/bar::

   <be:link.editRecord uid="42" table="pages" fields="title,subtitle" returnUrl="foo/bar">
       Edit record
   </be:link.editRecord>

Output::

   <a href="/typo3/record/edit?edit[pages][42]=edit&returnUrl=foo/bar&columnsOnly=title,subtitle">
       Edit record
   </a>

Arguments
=========


.. _link.editrecord_additionalattributes:

additionalAttributes
--------------------

:aspect:`DataType`
   mixed

:aspect:`Required`
   false
:aspect:`Description`
   Additional tag attributes. They will be added directly to the resulting HTML tag.

.. _link.editrecord_data:

data
----

:aspect:`DataType`
   mixed

:aspect:`Required`
   false
:aspect:`Description`
   Additional data-* attributes. They will each be added with a "data-" prefix.

.. _link.editrecord_aria:

aria
----

:aspect:`DataType`
   mixed

:aspect:`Required`
   false
:aspect:`Description`
   Additional aria-* attributes. They will each be added with a "aria-" prefix.

.. _link.editrecord_class:

class
-----

:aspect:`DataType`
   string

:aspect:`Required`
   false
:aspect:`Description`
   CSS class(es) for this element

.. _link.editrecord_dir:

dir
---

:aspect:`DataType`
   string

:aspect:`Required`
   false
:aspect:`Description`
   Text direction for this HTML element. Allowed strings: "ltr" (left to right), "rtl" (right to left)

.. _link.editrecord_id:

id
--

:aspect:`DataType`
   string

:aspect:`Required`
   false
:aspect:`Description`
   Unique (in this file) identifier for this HTML element.

.. _link.editrecord_lang:

lang
----

:aspect:`DataType`
   string

:aspect:`Required`
   false
:aspect:`Description`
   Language for this element. Use short names specified in RFC 1766

.. _link.editrecord_style:

style
-----

:aspect:`DataType`
   string

:aspect:`Required`
   false
:aspect:`Description`
   Individual CSS styles for this element

.. _link.editrecord_title:

title
-----

:aspect:`DataType`
   string

:aspect:`Required`
   false
:aspect:`Description`
   Tooltip text of element

.. _link.editrecord_accesskey:

accesskey
---------

:aspect:`DataType`
   string

:aspect:`Required`
   false
:aspect:`Description`
   Keyboard shortcut to access this element

.. _link.editrecord_tabindex:

tabindex
--------

:aspect:`DataType`
   integer

:aspect:`Required`
   false
:aspect:`Description`
   Specifies the tab order of this element

.. _link.editrecord_onclick:

onclick
-------

:aspect:`DataType`
   string

:aspect:`Required`
   false
:aspect:`Description`
   JavaScript evaluated for the onclick event

.. _link.editrecord_uid:

uid
---

:aspect:`DataType`
   mixed

:aspect:`Required`
   true
:aspect:`Description`
   Uid of record to be edited

.. _link.editrecord_table:

table
-----

:aspect:`DataType`
   string

:aspect:`Required`
   true
:aspect:`Description`
   Target database table

.. _link.editrecord_fields:

fields
------

:aspect:`DataType`
   string

:aspect:`Required`
   false
:aspect:`Description`
   Edit only these fields (comma separated list)

.. _link.editrecord_returnurl:

returnUrl
---------

:aspect:`DataType`
   string

:aspect:`Required`
   false
:aspect:`Description`
   Return to this URL after closing the edit dialog
