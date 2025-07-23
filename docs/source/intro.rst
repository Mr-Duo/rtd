.. _intro_toplevel:

==================
Overview / Install
==================

VulGuard is a unified tool for evaluating Just-In-Time Vulnerability Prediction Models.

Requirements
============

* `Python`_ 3.4 or newer
* `Git`_

.. _Python: https://www.python.org
.. _Git: https://git-scm.com/

Installing VulGuard
====================

Via Docker (RECOMMENDED)
=========================

.. code-block:: bash

   docker compose up --build -d
   docker exec -it vulguard /bin/bash

Inside docker container:

.. code-block:: bash

   python setup.py develop

If you want Docker container to access GPU(s), please download ``nvidia-container-toolkit``

**Note**: download this outside of the container

Install the ``nvidia-container-toolkit`` package as per official documentation at Github.

We also provide a `quick-run script <scripts/setup_nvidia_container_toolkit.sh>`_ for Debian-based OS.

From Scratch
============

SrcML
-----

.. code-block:: bash

   # Install libarchive13 libcurl4 libxml2
   sudo apt-get install libarchive13 libcurl4 libxml2

   # Install libssl
   wget http://archive.ubuntu.com/ubuntu/pool/main/o/openssl/libssl1.1_1.1.1f-1ubuntu2_amd64.deb && \
   dpkg -i libssl1.1_1.1.1f-1ubuntu2_amd64.deb && \
   rm -rf libssl1.1_1.1.1f-1ubuntu2_amd64.deb

   # Install SrcML
   wget http://131.123.42.38/lmcrs/v1.0.0/srcml_1.0.0-1_ubuntu20.04.deb && \
   dpkg -i srcml_1.0.0-1_ubuntu20.04.deb && \
   rm -rf srcml_1.0.0-1_ubuntu20.04.deb

Dependencies
------------

.. code-block:: bash

   pip install -r requirements.txt

Setup VulGuard
--------------

.. code-block:: bash

   python setup.py develop

How to cite VulGuard
=====================

.. sourcecode:: none

    @inbook{VulGuard,
        title = 
    }