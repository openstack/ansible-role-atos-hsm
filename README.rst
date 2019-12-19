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
   * - atos_client_cert_location
     - None
     - Full URL where the client certificate can be downloaded.
   * - atos_client_key_location
     - None
     - Full URL where the client key can be downloaded.
   * - atos_hsms
     - None
     - List of one or more HSM devices.

Requirements
------------

 - ansible >= 2.4

Usage
-----

You'll need to set up a temporary HTTP server somewhere that is accessible
to the node where this role will be applied.  The HTTP server should serve
the following:

- ATOS Client Software ISO file.
- HSM Server Certificate file(s).
- HSM Client Certificate file.
- HSM Client Key file associated with the Client Certificate.

Due to the sensitive nature of the Certificate and Key files, you should
use TLS encryption and username and passwords to access the HTTP server.

Use the hostname and user/password for your HTTP server for the full URL values
that need to be set for this role.  See `vars.yaml.example`.
