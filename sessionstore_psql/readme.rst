==========================
PostgreSQL Session Storage
==========================

This addons provides a class which stores the session into the PostgreSQL database.

----------------------
Installation and Usage
----------------------

You don't have to install this addon. Just place this into an addon directory. To use the module you have to add the pull request <https://github.com/odoo/odoo/pull/7937>.

-----
Usage
-----

To use this addon you have to set this line into the odoo configuration file:
::

    session_store = openerp.addons.sessionstore_psql.sessionstore.PostgresSessionStore

You can also use set the class via the commandline:
::

    ./odoo.py --session-store=openerp.addons.sessionstore_psql.sessionstore.PostgresSessionStore

Besides the session store you have to define the database in configuration file:
::

    db_name = soemdatabase

or via commandline:
::

    ./odoo.py -d somedatabase

Now the session is stored into the defined database. To test if it will be saved there then you have to activate the debug log. You should find the following line:
::

    HTTP sessions stored via: openerp.addons.sessionstore_psql.sessionstore.PostgresSessionStore

You can also look for the database table *sessionstore*.
