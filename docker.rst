Specifying Image Tags
=====================

If you have an image ``ubuntu`` you can specify its tag with
``ubuntu:20.04``. Presumably you can use the tagged version anywhere
an image is required.

List Images
===========

.. code-block:: bash

    docker image ls

If you want to include intermediate images

.. code-block:: bash

    docker image ls -a


List Containers
===============


.. code-block:: bash

    docker container ls

If you want to include all containers, not just running ones

.. code-block:: bash

    docker container ls -a


Create a New Container in Interactive Mode
==========================================

`Source
<https://docs.docker.com/engine/reference/commandline/run/#assign-name-and-allocate-pseudo-tty---name--it/>`_

Command
-------

.. code-block:: bash

    docker run --name my-container-name -it --rm ubuntu:20.04 /bin/bash

Explanation
-----------

Creates a container from the ``ubuntu:20.04`` image. Give the container
the name ``my-container-name``. The ``-i`` option keeps stdin open
and the ``-t`` option allocates a pseudo-tty. The ``--rm`` option
removes the container when it exits.

Create a New Conatiner from an Image which has an Entrypoint and enter it
=========================================================================


.. code-block:: bash

    docker run --name <container> -it --rm --entrypoint /bin/bash <image>


Start a Stopped Container
=========================


.. code-block:: bash

    docker start <container>

Where ``<container>`` can be the container's name or id.


Delete an Image
===============

.. code-block:: bash

    docker image rm <image>


Stop a Running Container
========================


.. code-block:: bash

    docker stop <container>

Where ``<container>`` can be the container's name or id.



Enter a Running Container
=========================


Create a Container but do not run it
====================================


Launch a Container from an Image and Run It in the Background
=============================================================

.. code-block:: bash


Create an Image with a Specific Name
====================================


.. code-block:: bash

    docker build -t <image-name> .
