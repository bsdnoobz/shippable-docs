Getting Started with Shippable
==============================

Introduction
------------
Shippable is a SaaS platform that lets you easily add Continuous Integration/Deployment to your Github and BitButcket (git) repositories. It is lightweight, super simple to setup, and runs your builds and tests faster than any other service. After building and teting your code, you can deploy it to any PaaS provider like Heroku & OpenShift and also to VMs, bare metal, OpenStack clusters, or any major infrastructure provider.

Shippable uses **Build Minions** which is docker based containers to run your workloads. Docker is the fastest growing Linux container solution and this will light up some cool scenarios like portability and versioning in the coming weeks.

Common use cases for Shippable include:

- Automating the packaging and deployment of web applications.
- Automated testing and continuous integration/deployment.

.. note:: Shippable is 100% free to use, even for private repositories.

Shippable supports many popular languages such as Ruby, Python, Node.js, and others. We also support services which are commonly used in your applications like MySQL, PostgreSQL, Elastic Search, and others.

About this guide
----------------
In this guide, you will learn how to use Shippable for automated testing and then deploy your web application to Heroku if the tests are passed. We will be using Ruby on Rails app in this guide, but you can easily use this guide for other frameworks/languanges as well.

This tutorial assumes that you have:

- A free `Shippable account <http://www.shippable.com>`.
- A free `Heroku account <https://signup.heroku.com/signup/dc>`.
