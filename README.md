# AuditLib


This module provides abstraction layer to message broker.
Logging module to be used with Kombu Messaging library:
https://pypi.python.org/pypi/kombu/
Requires Kombu 1.5.1 to maintain compatibility with Python 2.4.


Although designed to be used with RabbitMQ and Graylog,
it will work with any message broker and log management system.


Example:
    import audit


    message = '{"short_message":"Test", "host":"example.org"}'
    Audit = audit.Audit()
    Audit.custom_exchange(exchange='logs'...) # optional
    Audit.log(message)
