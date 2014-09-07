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
