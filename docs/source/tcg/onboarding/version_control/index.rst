Version Control
===============

We use two versioning file systems currently, Subversion (SVN) and Git (with GitHub).

Subversion
----------

TCG Digital hosts its own Subversion repository behind a VPN. To get access to our repository(s) you will need to reach out to a TCG Digital administrator and request access. The best way to do this is to open a ticket using the `TCG Digital Service Desk <https://tcg-digital.atlassian.net/servicedesk/customer/portals>`_ and request access and/or credentials as a new user. To be able to access the service desk you must have an Atlassian account. This should be provided to you shortly after your hiring. If you have not received it yet, contact your supervisor.

Two versions of SVN are available for developers, GUI and CLI.

- Windows
  
  - `TortiseSVN <https://tortoisesvn.net/downloads.html>`_ is a GUI client for SVN that makes it easy to see the repositories and files available at a glance. If you want to use SVN via the command line, be sure to select 'command line client tools' during the installation process.

- MacOS
  
  - :code:`brew install svn`
  - :code:`port install subversion`
  
- Linux

  - :code:`sudo apt-get install subversion` or your package manager equivalent.

Connecting
++++++++++

As stated above, the Subversion repo can only be accessed over VPN. Anything involving updates to/from the remote repo will require that the VPN is connected before doing any work.

For this, we use FortiClient. Download the FortiClient VPN for your device `here <https://www.fortinet.com/support/product-downloads#vpn>`_.

How to connect:

- Create a new VPN Connection.
- Select the VPN type 'IPSec-VPN'.
- Ensure the 'Authentication Method' is set to 'Remote Gateway'.
- Fill out the VPN Connection Info.

  - Remote Gateway: :code:`202.54.73.227`
  - Pre-shared Key: :code:`ssEd9keTkey`
  
  .. NOTE::
     The default advanced settings should be adequate.

- Save and connect with the shared VPN User Credentials (they will resemble the example credentials below).
  
  - Username: :code:`FirstnameL`
  - Password: :code:`Password@000`

You should now be able to click 'connect' to get connected to the VPN (You will need to 'connect' everyt time you intend to work with the remote). Please 'disconnect' when not in use, as it will slow down the bandwidth available for everyone else.

When you are connected to the VPN you can now connect to and access the repo via the tool of your choice using the necessary repository link. This is the top-level repository SVN link available, but be aware that cloning the repository using this link will clone *all of the repositories in the TCG Digital organization* so this is not a good idea:

:code:`http://svnmcube.tcgdigital.com/svn/MCube_Implementation/`

You will almost always be working on a subset of the repositories available, and so you will be provided with the specific SVN links for those projects. Whichever SVN link you are using, with the command line you can checkout the repo with :code:`svn checkout <repo link>`. If you are familiar with Git, `here <https://backlog.com/git-tutorial/reference/commands/>`_ is a list of Git-equivalent SVN commands.

.. NOTE::

   If you get the errors below it is likely due to a timeout set in SVN server-side. To fix this you can run :code:`svn cleanup && svn up`.

   .. code:: 
         
      svn: E120106: ra_serf: The server sent a truncated HTTP response body.
    
   .. code::

      svn: E000060: Error running context: Operation timed out

   

Git / GitHub
------------

Our github is `TCG Digital US <https://github.com/tcg-digital-us>`_. There are some public-facing repositories, but the majority of the work on Github currently is private. 

To gain access to the necessary repositories, reach out to your development supervisor and they will be able to add you as a Member to the organization. This will require you to set uo a GitHub account if you haven't already.
