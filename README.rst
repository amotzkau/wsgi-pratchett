============================
GNU Terry Pratchett for WSGI
============================

Simple WSGI middleware for adding Terry Pratchett's header to your requests.


-----
Usage
-----

WSGI middleware is pretty simple.  Wrap your WSGI application in an instance of
``GNUTerryPratchett`` and you're set.

.. code-block:: python

    from pratchett import GNUTerryPratchett

    # ... your code here, create your WSGI application
    app = GNUTerryPratchett(your_app)


When using PasteDeploy configuration files you can also add the middleware there.

.. code-block:: ini

    # Your main application
    [app:main]
    filter-with = pratchett

    [filter:pratchett]
    use = egg:wsgi-pratchett
