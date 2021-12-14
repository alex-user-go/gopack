Athens pre-filling
=========

This example shows how to download a list of go modules to pre-fill Athens disk storage (in case it is run completely cut off from the internet)

Getting started
---------------

Download [Docker Desktop](https://www.docker.com/products/docker-desktop) for Mac or Windows. [Docker Compose](https://docs.docker.com/compose) will be automatically installed. On Linux, make sure you have the latest version of [Compose](https://docs.docker.com/compose/install/).

Usage
--------------

Fork the current GitHub project and clone it to your local machine.

Go to /list folder and fill `goget.sh` with a list of modules you need to download, for example:

```bash
#!/bin/bash
go get github.com/my/module1;
go get github.com/my/module2;
```

Run:

```bash
docker-compose up --abort-on-container-exit
```

After downloading copy ATHENS_STORAGE folder to you Athens directory storage.
