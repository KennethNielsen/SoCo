.. _examples:

Examples
========

This page contains collection of small examples to show of the features of
*SoCo* and hopefully get you well started with the library.

All examples are shown as if entered in the Python interpreter (as apposed to
executed from a file) because that makes it easy to incoorporate output in the
code listings.

All the examples from :ref:`examples_playback_control` and forward assume that
you have followed one of the examples in
:ref:`examples_gettings_to_your_devices` and therefore already have a variable
``device`` point to a :class:`soco.SoCo` instance.

.. _examples_gettings_to_your_devices:

Getting to your devices
-----------------------

Getting all you devices
^^^^^^^^^^^^^^^^^^^^^^^

To get all your devices use the :func:`soco.discover` function.

.. code-block::
   >>> import soco
   >>> devices = soco.discover()
   >>> devices
   set([SoCo("192.168.0.10"), SoCo("192.168.0.30"), SoCo("192.168.0.17")])
   >>> device = devices.pop()
   >>> device
   SoCo("192.168.0.16")

Getting any device
^^^^^^^^^^^^^^^^^^

To get any device use the :func:`soco.discovery.any_soco` function. This can be
useful for cases where you really do not care which one you get, you just need
one e.g. to query for music library information.

.. code-block::
>>> import soco
>>> device = soco.discovery.any_soco()
>>> device
SoCo("192.168.0.16")

Getting a named device
^^^^^^^^^^^^^^^^^^^^^^

.. _examples_playback_control:

Playback control
----------------
