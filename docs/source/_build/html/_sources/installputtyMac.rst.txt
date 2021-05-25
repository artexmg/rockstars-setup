SSH client (for Mac only)
====================

**Note:** *If you are using Windows, then you need to install PuTTY. Go to Windows section instead*

Creating SSH Keys
------------------

Before connecting using SSH, you need to create your private and public SSH Keys (refer to `Use SSH Public Key Authentication <https://www.linode.com/docs/guides/use-public-key-authentication-with-ssh/>`_ to understand more about SSH Keys)

Start *terminal* and enter 

.. code-block:: shell

    ssh-keygen -b 4046

this will create a RSA with the **Number of bits in a generated key** equals to 4094.

.. figure:: ./images/mackeygen_1.png
    :alt: alt textt
    :align: center
    :scale: 80 %
    
    key generation

If you don't have a previously generated key, it is recommended to accept the default file name. If you have more than one key then you can modify the name of the file, but you will need to enter the full path (e.g. /Users/amendoza/.ssh/id_rsa_rockstars6G).

Also, you can secure your key by adding a passphrase (simple put, a password). This is not required, but it is a good practice. Do not forget what the password is, as it will be used later in the process to connect to the remote server.

.. figure:: ./images/mackeygen_2.png
    :alt: alt textt
    :align: center
    :scale: 40 %

    noticed that the filename includes a full path


after the command is executed succesfully, you can verify that the files were created in the specified directory. The one with extension *pub* correspond to the public key.

.. figure:: ./images/mackeygen_3.png
    :alt: alt textt
    :align: center
    :scale: 50 %

    verify that both, public and private keys were created

Configuring SSH connection
--------------------------

Now that you have your SSH Keys in place, we can configure our connection to the remote server.

In the *Terminal* connect to the remote server by executing the ssh command entering your own username and IP address (or URL).

.. code-block:: shell

    ssh username@104.237.138.186


You may get a warning that the key was not accepted. This is expected as we have not uploaded the public key to the remote server. 
It will ask for your password instead (not the passphrase, but the password for the remote server). After the connection is successfully stablished you should see something similar to the image below

.. figure:: ./images/mackeygen_4.png
    :alt: alt textt
    :align: center
    :scale: 45 %

    it will ask for your password

Now you can upload your public key file with *ssh-copy-id* command, keyed from the *Terminal*

.. code-block:: shell

    ssh-copy-id username@104.237.138.186

It will ask for your passphrase to validate that you have the right credentials. At the end you will get a screen similar to above, but not exactly the same as it will vary depending on the keys installed previously

.. figure:: ./images/mackeygen_5.png
    :alt: alt textt
    :align: center
    :scale: 40 %

    ssh-copy-id will upload your public key to the remote server

Finally, to verify that everything worked as intended, try to connect using *ssh*, but this time you should not be asked for your password (you may be asked to enter only your passphrase)

.. figure:: ./images/mackeygen_6.png
    :alt: alt textt
    :align: center
    :scale: 40 %

    you should be able to connect to the remote server without password (only passphrase)

These are all the configurations that we would need to make our SSH connection work.
Now that you have all the files ready, the next step would be connecting to the remote server. Do not close PuTTY!