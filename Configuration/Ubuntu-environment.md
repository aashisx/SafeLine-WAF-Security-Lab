System Preparation
------------------
Ubuntu package lists updated.
System packages upgraded.
Installed tools:
- net-tools
- OpenSSL
- Git
- curl

Purpose:
Prepare the Ubuntu server for DVWA deployment and SafeLine WAF installation.

LAMP Stack Installation
-----------------------
Apache2: Installed and Running
PHP: Installed
MySQL Server: Installed and Running

Purpose:
The LAMP stack provides the backend infrastructure required to host the Damn Vulnerable Web Application (DVWA).

MySQL Hardening
---------------
Executed mysql_secure_installation.

Security actions:
- Removed anonymous users
- Disabled remote root login
- Removed test database
- Reloaded privilege tables