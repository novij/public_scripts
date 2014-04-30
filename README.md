public scripts
==============

Scripts I developed myself


backup_xen
==========

Use this script to backup your Citrx Xen virutal machines as XVA on a
backup server or file server.
It creates one file per server, e.g. 'server-name.xva'
If a backup fails, the old file won't be overwritten.
At the first run, the script saves the SSH public key and the Xen server
credentials on the Xen server. The credentials are needed to download
the XVA file through HTTP.


Usage:
./backup_xen xenhostname vm-id

or create a file with one vm-id per line and optional comment, e.g.:
a777bf48-bdce-d286-9f06-1130c6295f8a    linux otrs
2edaa605-c977-3d38-c42f-c354bdf163b8    citrix xen webservice
f53557b3-a808-afc9-e35d-9256c63cb795    windows ad

./backup_xen xenhostname /file-with-vm-ids
