Usage
=====

.. _installation:

Dependencies
------------

**Note for Windows Users:** In order to deploy code, you will need to install a bash terminal
such as Git Bash, or, preferably, Windows Subsystem for Linux (Ubuntu)

Python 3.9 or newer is required to run this project.

First, install the dependencies using pip:
.. code-block:: console

   (.venv) $ pip install -R requirements.txt

Instalation
-----------

Clone the repository on both your local machine and the robot's rasberry pi, with
.. code-block:: console

   $ git clone https://github.com/FRC1076/RobotKitLib.git

On the Raspberry Pi
-------------------

Enable SSH and GPIO in the configuration menu reached with
.. code-block:: console

   $ sudo raspi-config
See the Raspberry Pi Documentation for further detail.

Setup the systemd service with
.. code-block:: console

   $ sudo ./setup_autorunner.sh


Usage
-----

The workflow of a RobotKitLib-based robot competition is as similar as possible to FRC-WPILIB.
Thus the basic equation of Code -> Deploy to Pi -> Run code with Driverstation remains.

Deploying Code
--------------

Deploy code to the Robot with
.. code-block:: console

   $ python robot.py --action deploy --ip_addr localhost
Replacing 'localhost' with the IP address of the robot.

Running the Driverstation
-------------------------

Run the driverstation with
.. code-block:: console

   $ python driverstation.py localhost
Replacing 'localhost' with the IP address of the robot.



