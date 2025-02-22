:github_url: hide

.. DO NOT EDIT THIS FILE!!!
.. Generated automatically from GUT Plugin sources.
.. Generator: documentation/godot_make_rst.py.
.. _class_GutHookScript:

GutHookScript
=============

**Inherits:** `RefCounted <https://docs.godotengine.org/en/stable/classes/class_refcounted.html>`_

This script is the base for custom scripts to be used in pre and post run hooks.

.. rst-class:: classref-introduction-group

Description
-----------

GUT Wiki:  `https://gut.readthedocs.io <https://gut.readthedocs.io>`__ 



Creating a hook script requires that you:

- Inherit ``GutHookScript``\ 

- Implement a ``run()`` method

- Configure the path in GUT (gutconfig aand/or editor) as the approparite hook (pre or post).

See `Hooks <../Hooks.html>`__

.. rst-class:: classref-reftable-group

Properties
----------

.. table::
   :widths: auto

   +--------------------------------------------------------------------------------+--------------------------------------------------------------------+---------------+
   | `Variant <https://docs.godotengine.org/en/stable/classes/class_variant.html>`_ | :ref:`JunitXmlExport<class_GutHookScript_property_JunitXmlExport>` | ``load(...)`` |
   +--------------------------------------------------------------------------------+--------------------------------------------------------------------+---------------+
   | `Variant <https://docs.godotengine.org/en/stable/classes/class_variant.html>`_ | :ref:`gut<class_GutHookScript_property_gut>`                       | ``null``      |
   +--------------------------------------------------------------------------------+--------------------------------------------------------------------+---------------+

.. rst-class:: classref-reftable-group

Methods
-------

.. table::
   :widths: auto

   +--------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
   | |void|                                                                         | :ref:`abort<class_GutHookScript_method_abort>`\ (\ )                                                                                                |
   +--------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
   | `Variant <https://docs.godotengine.org/en/stable/classes/class_variant.html>`_ | :ref:`get_exit_code<class_GutHookScript_method_get_exit_code>`\ (\ )                                                                                |
   +--------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
   | |void|                                                                         | :ref:`run<class_GutHookScript_method_run>`\ (\ )                                                                                                    |
   +--------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
   | |void|                                                                         | :ref:`set_exit_code<class_GutHookScript_method_set_exit_code>`\ (\ code\: `int <https://docs.godotengine.org/en/stable/classes/class_int.html>`_\ ) |
   +--------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
   | `Variant <https://docs.godotengine.org/en/stable/classes/class_variant.html>`_ | :ref:`should_abort<class_GutHookScript_method_should_abort>`\ (\ )                                                                                  |
   +--------------------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+

.. rst-class:: classref-section-separator

----

.. rst-class:: classref-descriptions-group

Property Descriptions
---------------------

.. _class_GutHookScript_property_JunitXmlExport:

.. rst-class:: classref-property

`Variant <https://docs.godotengine.org/en/stable/classes/class_variant.html>`_ **JunitXmlExport** = ``load(...)`` :ref:`🔗<class_GutHookScript_property_JunitXmlExport>`

Class responsible for generating xml.  You could use this to generate XML yourself instead of using the built in GUT xml generation options.  See :ref:`addons/gut/junit_xml_export.gd<class_addons/gut/junit_xml_export.gd>`

.. rst-class:: classref-item-separator

----

.. _class_GutHookScript_property_gut:

.. rst-class:: classref-property

`Variant <https://docs.godotengine.org/en/stable/classes/class_variant.html>`_ **gut** = ``null`` :ref:`🔗<class_GutHookScript_property_gut>`

This is the instance of :ref:`GutMain<class_GutMain>` that is running the tests.  You can get information about the run from this object.  This is set by GUT when the script is instantiated.

.. rst-class:: classref-section-separator

----

.. rst-class:: classref-descriptions-group

Method Descriptions
-------------------

.. _class_GutHookScript_method_run:

.. rst-class:: classref-method

|void| **run**\ (\ ) :ref:`🔗<class_GutHookScript_method_run>`

Virtual method that will be called by GUT after instantiating this script. This is where you put all of your logic.

.. rst-class:: classref-item-separator

----

.. _class_GutHookScript_method_set_exit_code:

.. rst-class:: classref-method

|void| **set_exit_code**\ (\ code\: `int <https://docs.godotengine.org/en/stable/classes/class_int.html>`_\ ) :ref:`🔗<class_GutHookScript_method_set_exit_code>`

Set the exit code when running from the command line.  If not set then the default exit code will be returned (0 when no tests fail, 1 when any tests fail).

.. rst-class:: classref-item-separator

----

.. _class_GutHookScript_method_get_exit_code:

.. rst-class:: classref-method

`Variant <https://docs.godotengine.org/en/stable/classes/class_variant.html>`_ **get_exit_code**\ (\ ) :ref:`🔗<class_GutHookScript_method_get_exit_code>`

Returns the exit code set with ``set_exit_code``

.. rst-class:: classref-item-separator

----

.. _class_GutHookScript_method_abort:

.. rst-class:: classref-method

|void| **abort**\ (\ ) :ref:`🔗<class_GutHookScript_method_abort>`

Usable by pre-run script to cause the run to end AFTER the run() method finishes.  GUT will quit and post-run script will not be ran.

.. rst-class:: classref-item-separator

----

.. _class_GutHookScript_method_should_abort:

.. rst-class:: classref-method

`Variant <https://docs.godotengine.org/en/stable/classes/class_variant.html>`_ **should_abort**\ (\ ) :ref:`🔗<class_GutHookScript_method_should_abort>`

Returns if ``abort`` was called.

.. |virtual| replace:: :abbr:`virtual (This method should typically be overridden by the user to have any effect.)`
.. |const| replace:: :abbr:`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
.. |vararg| replace:: :abbr:`vararg (This method accepts any number of arguments after the ones described here.)`
.. |constructor| replace:: :abbr:`constructor (This method is used to construct a type.)`
.. |static| replace:: :abbr:`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
.. |operator| replace:: :abbr:`operator (This method describes a valid operator to use with this type as left-hand operand.)`
.. |bitfield| replace:: :abbr:`BitField (This value is an integer composed as a bitmask of the following flags.)`
.. |void| replace:: :abbr:`void (No return value.)`
