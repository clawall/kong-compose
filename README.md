# Kong Compose Sample
This repository contains a docker-compose file that sets up an environment for local tests of Kong.
It's composed of 3 services:
- [Kong](https://docs.konghq.com/gateway/):  The API Gateway configured in declarative (db-less) mode.  Its configuration is present at the folder __./kong__.
- [Konga](https://github.com/pantsel/konga):  An GUI to configure Kong (it's configured as read-only by default).  Its configuration is present at the folder __./konga__.
- [Mock Server](https://www.mock-server.com/):  A powerful mock server that configures responses based on parameters received.  Its configuration is present at the folder __./mockserver__ and it has only 3 read-only GET endpoints.

## Starting up
Just run `docker-compose up`.  The services will be exposed as:

- Kong:  http://localhost:8000/
- Konga:  http://localhost:1337/
- Mock Server:  Unreacheable from the host, it must be reached via Kong at http://localhost:8000/
