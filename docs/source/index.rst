Welcome to Beth's documentation!
===================================

Introduction
============
   
I'm learning how to structure and build these files. 
   
Section A
---------

Contents here.

   
Header 3
~~~~~~~~

   .. include:: tcg/welcome.rst

Header 4
^^^^^^^^

LVA Virtual Machine
-------------------

.. code:: bash

   $ ssh -v -i ~/.ssh/vmtcgdpoc-keypair.pem ubuntu@52.66.25.175 -p 22

.. note:: This project is under active development.
      
.. warning:: **Warning Message**

Contents
--------

   .. toctree::
      :name: TCG Digital US
      :caption: TCG Digital US
      :maxdepth: 5

      tcg/welcome
      tcg/onboarding/index
      tcg/onboarding/tutorials
      tcg/doc-styleguide
