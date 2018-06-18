python-safet
============

Python library and commandline client for communicating with the Archos Safe-T mini Hardware Wallet

This library is a mofified version of `python-trezor <https://github.com/trezor/python-trezor>`_.

See https://safe-t.io for more information

Install
-------

Linux requirements:

.. code::

  sudo apt-get install python3-dev cython3 libusb-1.0-0-dev libudev-dev git

Linux Python requirements:

.. code::

  sudo -H pip3 install setuptools
  sudo -H pip3 install -r requirements.txt


Commandline client (safetctl)
---------------------------

The included ``safetctl`` python script can perform various tasks such as changing setting in the device, signing transactions, retrieving account info and addresses. See the `docs/ <docs/>`_ sub folder for detailed examples and options.


Python Library
--------------

You can use this python library to interact with the Safe-T mini and use its capabilities in your application.
See examples here in the `tools/ <tools/>`_ sub folder.


PIN Entering
------------

When you are asked for PIN, you have to enter scrambled PIN. Follow the numbers shown on the device's display and enter the their positions using the numeric keyboard mapping:

=== === ===
 7   8   9
 4   5   6
 1   2   3
=== === ===

Example: your PIN is **1234** and the device is displaying the following:

=== === ===
 2   8   3
 5   4   6
 7   9   1
=== === ===

You have to enter: **3795**
