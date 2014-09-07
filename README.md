figgy
=====

A scalable docker cluster for LAMP apps, mainly Drupal.

Inspired by http://www.centurylinklabs.com/auto-loadbalancing-with-fig-haproxy-and-serf/?hvid=4kkCCH

This is an experiment.

Setup
=====

1. Install docker version > 1.0: https://docs.docker.com/installation/
2. Install fig: http://www.fig.sh/install.html
  The simplest way to install fig is to use Python's installer:

  ```
  $ sudo pip install -U fig
  ```
3. `$ sudo fig up`

  - The first time it will take a while as it downloads all your images.
  - This command will then output the logs from all containers.
  - The containers will run until the command closes. Use CTRL-C to stop all of containers.

4. Browse to http://127.0.0.1:8080 to view whatever is in the src folder of this repo.
5. `$ sudo fig scale web=2`

  - This will add another web server, and Serf will automatically add it to the HAProxy
    load balancer.
6. Browse to http://127.0.0.1:8080 and keep reloading. You will see the IP address change
    depending on what container HAProxy sent you to.

With the simple command `fig scale web=X` you can scale the web servers up and down in number.

All of them will have the source code mounted at src available, and be ready to go instantly.

