atos-hsm
========

A role to manage ATOS Hardware Security Module (HSM) client software.

Role Variables
--------------

.. list-table::
   :widths: auto
   :header-rows: 1

   * - Name
     - Default Value
     - Description
   * - atos_client_working_dir
     - /tmp/atos_client_install
     - Working directory in the target host.
   * - atos_client_iso_name
     - None
     - Filename for the ATOS Client Software ISO.
   * - atos_client_iso_location
     - None
     - Full URL where a copy of ATOS Client ISO can be downloaded.
   * - atos_hsm_ip_address
     - None
     - IPv4 address for the ATOS HSM.
   * - atos_client_cert_location
     - None
     - Full URL where the client certificate can be downloaded.
   * - atos_client_key_location
     - None
     - Full URL where the client key can be downloaded.
   * - atos_server_cert_location
     - None
     - Full URL where the server certificate can be downloaded.

Requirements
------------

 - ansible >= 2.4
