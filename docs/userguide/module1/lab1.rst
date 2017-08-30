.. _ug_lab_environment:

Lab Environment
---------------

This guide assumes the following devices are available in your lab environment:

- Minimum 1 x F5 BIG-IP (:ref:`Version Info <testedversions>`)
- 1 x Windows/Linux/Mac OS Host

	- Python >= 2.7
	- Web Browser (Google Chrome is recommended)

To complete the labs that demonstrate loading of resources by URL in 
:doc:`/userguide/module3/module3` you will need:

- 1 x HTTP Web Server
- :github_remote_url:`remote_url_files.tar.gz <test>` extracted to the public 
  root of the web server

Pre-built Lab Environment
^^^^^^^^^^^^^^^^^^^^^^^^^

If you are using a pre-built lab environment please assume the following:

- Base Networking is configured
- BIG-IP Device is Licensed/Activated

- All actions will be performed on BIGIP_A
- All configured virtual servers are accessible by IP from your jump host

.. list-table::
    :widths: 30 20 60
    :header-rows: 1
    :stub-columns: 1

    * - VLAN
      - VLAN Tag
      - CIDR Block
    * - Management
      - 1
      - 10.1.1.0/24
    * - Internal
      - 10 
      - 10.1.10.0/24
    * - External
      - 20
      - 10.1.20.0/24

.. list-table::
    :widths: 30 40 20
    :header-rows: 1
    :stub-columns: 1

    * - Device
      - IP's
      - Credentials
    * - BIG-IP A
      - - Management: 10.1.1.5
        - Internal: 10.1.10.8/24
        - External: 10.1.20.8/24
      - - admin/admin
    * - Windows Jump Host
      - - Management: 10.1.1.4
        - External: 10.1.20.250/24
      - - user/user
    * - Linux Webserver
      - - Management: 10.1.1.7
        - Internal: 10.1.10.100-103/24
        - Services: HTTP/HTTPS/SSH
      - - Auth: SSH Key Auth Only
