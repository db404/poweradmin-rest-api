PowerAdmin REST API
=================

|travis|

.. |travis|  image:: https://travis-ci.org/adfinis-sygroup/poweradmin-rest-api.png?branch=master
   :target: https://travis-ci.org/adfinis-sygroup/poweradmin-rest-api

A basic RESTful API for `PowerAdmin`_

.. _ `PowerAdmin`: http://www.poweradmin.org/

Installation
------------
1. Install dependencies

.. code:: shell

    apt-get install python3 python3-pip python3-virtualenv virtualenv python3-dev libmysqlclient-dev libsasl2-dev libldap2-dev

2. Create and activate virtualenv

.. code:: shell

    virtualenv -p `which python3` env
    source env/bin/activate

3. Install python dependencies

.. code:: shell

    make install
    # or for development
    make install_dev


Settings
--------
Use `poweradmin/settings_example.py` as basis for your configuration.

You can activate by using `DJANGO_SETTINGS_MODULE`

https://docs.djangoproject.com/en/1.11/topics/settings/#designating-the-settings

Documentation
-------------

You can browse the api with swagger_ by opening host name (e.g. http://localhost:8000).

.. _swagger: https://swagger.io/

For authentication use `api-token-auth` call and assign `username` and `password`.
You will receive a JWT token. Copy this token prepended with 'jwt' e.g. (jwt  eyjO.....)
and click on `Authorize`.

As `api_key` assign `JWT token` and login. You should now see a `v1` api tree.

License
-------

PowerAdmin REST API is licensed under GPL-3 or later following license model of PowerAdmin it is
based on.
