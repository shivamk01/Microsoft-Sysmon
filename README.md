Add licenses to the file which are important.
# Microsoft-Sysmon
Implementing Sysmon as part of Sysinternals suite within the premise on all endpoints which are part of the organization, for monitoring event logs.

Install with default settings (process images hashed with sha1 and no network monitoring)
sysmon -accepteula –i

Install with md5 and sha256 hashing of process created and monitoring network connections
sysmon -accepteula –i –h md5,sha256 –n

Install Sysmon with a configuration file (as described below)

sysmon –accepteula –i c:\windows\config.xml

Uninstall
sysmon –u

Dump the current configuration
sysmon –c

Change the configuration to use all hashes, no network monitoring and monitoring of DLLs in Lsass
sysmon –c –h * –l lsass.exe

Change the configuration of sysmon with a configuration file (as described below)

sysmon –c c:\windows\config.xml

Change the configuration to default settings
sysmon –c --

Show the configuration schema:
sysmon -s
