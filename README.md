RapidPro Python Client
======================

![Build Status](https://travis-ci.org/rapidpro/rapidpro-python.svg?branch=master)
[![Coverage Status](https://coveralls.io/repos/github/rapidpro/rapidpro-python/badge.svg?branch=master)](https://coveralls.io/github/rapidpro/rapidpro-python)

Official Python client library for the [RapidPro](http://rapidpro.github.io/rapidpro/). Supports latest Python 2 and 3.

Visit [here](http://rapidpro-python.readthedocs.org/) for complete documentation.

Installation
------------

```
pip install rapidpro-python
```

Example
-------

```python
from temba_client.v1 import TembaClient
client = TembaClient('rapidpro.io', 'your-api-token')
for contact in client.get_contacts():
    print(contact.name)

client.create_broadcast(text="Howdy", contacts=contacts[0:5])
client.block_contacts(contacts[1:3])
```

If you don't know your API token then visit the [API Explorer](http://rapidpro.io/api/v1/explorer)

Development
-----------

For discussions about future development, see the [RapidPro Developers Group](https://groups.google.com/forum/#!forum/rapidpro-dev).

To run the tests:

```
nosetests --with-coverage --cover-erase --cover-package=temba_client --cover-html
```
