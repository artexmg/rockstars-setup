
PuTTY (for Windows only)
-------------------------

**Note:** *If you are using MacOSX as a OS, then you don't need to install PuTTY. Instead you will use the terminal*

PuTTY is an SSH and telnet client for Windows, developed originally by Simon Tatham. It is open source  developed and supported by a group of volunteers. 

Download and install PuTTY's latest version following the instructions from `here <https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html>`_ 

Setting up SSH client
----------------------------

After you finish installing PuTTY, you should have something similar to this:

.. figure:: ./images/PuttyInstalled.png
    :alt: alt textt
    :align: center
    :scale: 50 %

    Make sure you have PuTTY and PuTTYgen Installed

Make sure that both PuTTY and PuTTYgen were successfully installed. The first one is the client and the second is how we will generate the SSH Keys.

Creating SSH Keys
_________________

Before connecting using SSH, you need to create your private and public SSH Keys (refer to `Use SSH Public Key Authentication <https://www.linode.com/docs/guides/use-public-key-authentication-with-ssh/>`_ to understand more about SSH Keys)

Start PuTTYgen and select RSA and change **Number of bits in a generated key** from 2048 to 4094.

.. figure:: ./images/keygen_1.png
    :alt: alt textt
    :align: center
    :scale: 70 %

    Change 'number of bits in a generated key' to 4096

Then hit the **Generate** button and keep moving the mouse to induce randomness into the key

.. figure:: ./images/keygen_2.png
    :alt: alt textt
    :align: center
    :scale: 70 %

    Keep moving the mouse!


once the key is created, you can secure it adding a passphrase (simple put, a password). This is not required, but it is a good practice. Do not forget it as it will be used later in the process to connect to the remote server.

.. figure:: ./images/keygen_3.png
    :alt: alt textt
    :align: center
    :scale: 70 %

    Enter keypassphrase to protect your ssh key