 steps to set up a virtual Ubuntu environment on a Windows host operating system via VirtualBox
===================================

Usage
=====

.. _installation:

Installation
------------

To use Lumache, first install it using pip:

.. code-block:: console

   (.venv) $ pip install lumache

Creating recipes
----------------

To retrieve a list of random ingredients,
you can use the ``lumache.get_random_ingredients()`` function:

.. autofunction:: lumache.get_random_ingredients

The ``kind`` parameter should be either ``"meat"``, ``"fish"``,
or ``"veggies"``. Otherwise, :py:func:`lumache.get_random_ingredients`
will raise an exception.

.. autoexception:: lumache.InvalidKindError

For example:

>>> import lumache
>>> lumache.get_random_ingredients()
['shells', 'gorgonzola', 'parsley']


**Lumache** (/lu'make/) is a Python library for cooks and food lovers
that creates recipes mixing random ingredients.
It pulls data from the `Open Food Facts database <https://world.openfoodfacts.org/>`_
and offers a *simple* and *intuitive* API.

Check out the :doc:`usage` section for further information, including
how to :ref:`installation` the project.

.. note::

   This project is under active development.

Contents
--------

.. toctree::



My change
-------------

# Step 1: Install VirtualBox
VirtualBox is a tool which allows you to run different operating systems virtually on your host operating system. This is referred to as a virtual machine.
1. In order to install VirtualBox, follow this link.
2. Under “VirtualBox 6.1.28 platform packages”, select the Windows host download link.
3. Open VirtualBox.

# Step 2: Download Ubuntu ISO file
For the purposes of this document I will be utilizing Ubuntu 20.04, although 18.04 is recommended.
Follow this link.
Under the "Download" button select "20.04 LTS".
Step 3: Set Up Ubuntu virtual machine in VirtualBox
Open VirtualBox.
Click the "New" button.
Provide the name of your new machine (I recommend the name Ubuntu 20.04).
Set Machine folder location (your choice).
Ensure the Type and version fields are correct (Type: Linux ; Version: Ubuntu (64-bit)).
Select "Next".
Select memory size (Anywhere inside the green area of the scale).
Select "Next".
Select “Create a virtual hard disk now”.
Select "Create".
Select "VDI" (Virtual Disk Image).
Select "Next".
Select "Dynamically Allocated" (Allows the OS to expand disk size if required).
Select "Next".
Choose "File Location".
Choose virtual hard disk size (I recommend around 100GB).
Click "Create".
Step 4: Configure Settings for Ubuntu virtual Machine
Select your machine.
Select "Settings".
Under "General", click "Advanced Settings". Select "Bidirectional" for both shared clipboard and drag and drop fields. This will allow you to share files between host machine and Ubuntu machine.
Under "System", click "processor". Choose the number of CPUs you wish to use (if no preference leave as default).
Under "Storage", click "Empty". Under "Attributes", by optical drive click Disk dropdown and choose a disk file. Provide location for ISO file downloaded in step 2.
Select "OK".
Step 5: Open your virtual machine
Select your machine and press start.
Select preferred language and click "Install Ubuntu".
Select "Keyboard Layout and Language", click "Continue".
Under “What apps would you like to start with?”, select "Normal installation".
Under “Other Options”, select download updates while installing Ubuntu. Then install third party software for graphics and Wi-Fi hardware, and additional media formats.
Click "Continue".
Under "Installation Type", select "Erase Disk and install Ubuntu".
Click "Install Now".
Click "Continue".
Select your location.
Enter your preferred name, "Username" and "Password".
Click "Continue".
Wait for installation to complete.
Click "Restart Now".
Log in to the user that you created.
Follow Setup Instructions provided by the OS.
Step 6: (Optional) Install VirtualBox Guest Additions
This software will allow your VirtualBox virtual machine to properly maximize on your screen.
Open Terminal.
Give command: sudo apt install build-essential dkms linux-headers-$(uname -r).
Provide your password.
Enter "y", press enter.
Close Terminal.
Select "devices" on VirtualBox window.
Select "Insert Guest additions CD Image".
Select "Run".
Provide your password, click "Authenticate".
Restart Ubuntu operating system.
