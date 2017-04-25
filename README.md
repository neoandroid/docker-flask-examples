Flask App with MySQL Database
=============================
[Flask](http://flask.pocoo.org/) is a web development microframework for Python.
It's efficient, easy-to-use, and easy-to-deploy! This repo shows several ways to
deploy your application using Docker.

Quick Start
-----------
 1. Change to directory "horizontal-scale"
 2. Run `docker-compose up`
 3. Visit `http://127.0.0.1` in your browser.

Requirements
------------
In order to run these examples you must have installed:
 - Docker Engine >=1.13
 - Docker Compose >=1.10

Note: Tested with Docker Engine 17.03.1 and Docker Compose 1.12

Description
-----------
You can choose different architectures to build your application depending on your needs. In each folder you'll find a reference implementation for that scenario.

 - **Simple**: Two containers linked together, one for the database and the other for the application. Application listens on port 5000 by default.
 - **Scale out**: Load-balanced design using HAProxy. Balance algorithm is round-robin by default.

Technology
----------
The main motivation to use Docker is for its simplicity. The Configuration
Management solutions all share complexity that reflects the difficulty of
configuring bare metal and virtual machines. This means not only launching them,
but also modifying the state of their configuration.

Because Docker needs to only express the configuration for a single process, the
problem becomes far easier. The Dockerfile is, thus, a bit more than a simple
bash script for configuring a process with its dependencies.

Docker also brings artifact management along with it via the public Docker Hub.
This can be thought of as a correlate to public Github repositories. When a
developer writes code and packages it with a Docker he can push this to the
Docker hub to be shared as a binary artifact. The ramifications of this are
quite extensive.  This artifact can be tested for function, performance and
security as a "black box" without needing to know what the contents of the "box"
(i.e. container) are.  

Taking this one step farther, it is possible then that one developer could write
a service based on Ubuntu and Python to manage users while another developer
could write a service that correlates these user's behaviors to their social
media handles in Scala running on CentOS. Further, the operations team need not
care since all this is packaged up. This could lead to the ops team focusing on
performance and security testing rather than worrying about application packaging.

More info:

  - [`docker-compose`](https://docs.docker.com/compose/reference/)
  - [`up`](https://docs.docker.com/compose/reference/up/)
