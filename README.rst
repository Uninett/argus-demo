==================
Argus demo helpers
==================

The directory ``incidents/`` contains json-files that describes incidents to be
faked in an argus demo, one incident per file.

The incidents can be opened and closed for instance via cron.

The argus-server code must be in PYTHONPATH. For instance by installing into
a virtualenv then either activating the virtualenv or adding the path to the
virtualenv to PYTHONPATH manually. The database must be up and running and
known to the Argus server.

To open an incident (shell):

1. Select one of the files in ``incidents/``, store the filename in ``$filename``
2. Run ``python3 manage.py create_fake_incident --files $filename``

To close an incident (shell):

1. Select one of the files in ``incidents/``, store the filename in ``$filename``
2. Run ``python3 manage.py close_incident --files $filename``
