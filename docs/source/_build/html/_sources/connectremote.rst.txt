Connect to the remote server
==================

Once everything is setup, it is time to connect to the remote server.

.. figure:: ./images/putty_1.png
    :alt: alt textt
    :align: center
    :scale: 70 %

    Select your session and Load it before clicking Open.

On PuTTY, go back to *Session* and make sure that you are on your saved one (e.g. RockstarsG6). Then click *Open*. 

If everything was configured OK, you should get a Security Alert windows, telling you that this is the first time you are connecting to the server. Click Accept.

.. figure:: ./images/putty_6.png
    :alt: alt textt
    :align: center
    :scale: 70 %

    PuTTY Security Alert.

Enter your username as prompted and hit return key

.. figure:: ./images/putty_7.png
    :alt: alt textt
    :align: center
    :scale: 70 %

    Enter your username.

You will see a message telling you that the server refused the key. This is OK as the public file has not being uploaded yet (this is going to be done in the next step).

Meanwhile we are going to use a password to connect into the remote server (note that this **is not** the passphrase you entered to protect your private file, but the password provided to you by your instructor). 

.. figure:: ./images/putty_8.png
    :alt: alt textt
    :align: center
    :scale: 70 %

After you enter your password, you will see something similar to this. **Congratulations!** you are now connected to the remote unix server!

In the next section you will configure your account to connect using SSH Key instead of password, making the connection more secure.