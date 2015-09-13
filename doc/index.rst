.. Sonos Controller (SoCo) documentation master file, created by
   sphinx-quickstart on Sun Feb 24 10:28:22 2013.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Welcome to SoCo's documentation!
===================================================

SoCo (Sonos Controller) is a high level Python 2/3 library to control your
`Sonos <www.sonos.com>`_ ® speakers with::

    # Import soco and get a SoCo instance
    import soco
    device = soco.discovery.any_soco()

    # Get all albums from the music library that contains the word "Black"
    # and add them to the queue
    albums = device.music_library.get_albums(search_term='Black')
    for album in albums:
        print('Added:', album.title)
        device.add_to_queue(album)

    # Dial up the volume (just a bit) and play
    device.volume += 10
    device.play()

To get started with SoCo, start by reading the :ref:`tutorial <tutorial>` and
then optionally follow up with any of the advanced topics that interest you:
:ref:`speaker_topologies`, :ref:`events` and :ref:`upnp_services`. Finally dive
into the :ref:`the full module reference documentation <module_reference>`.

For support post a question in the `SoCo Google group
<https://groups.google.com/forum/#!forum/python-soco>`_ or `file an issue on
Github <https://github.com/SoCo/SoCo/issues>`_.

If you are interested in participating in the development, plase read :ref:`the
development documentation <development_topics>` and `file a bug
<https://github.com/SoCo/SoCo/issues>`_ or `make a pull request
<https://github.com/SoCo/SoCo/pulls>`_ on `Github
<https://github.com/SoCo/SoCo>`_.


Contents
--------

.. toctree::
   :maxdepth: 2

   tutorial
   topology
   events
   services
   plugins
   releases/index
   dev/index
   modules/index


Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`
