Getting Started with Shippable
==============================

Introduction
------------
Shippable is a SaaS platform that lets you easily add Continuous Integration/Deployment to your Github and BitButcket (git) repositories. It is lightweight, super simple to setup, and runs your builds and tests faster than any other service. After building and teting your code, you can deploy it to any PaaS provider like Heroku & OpenShift and also to VMs, bare metal, OpenStack clusters, or any major infrastructure provider.

Shippable uses **Build Minions** which is docker based containers to run your workloads. Docker is the fastest growing Linux container solution and this will light up some cool scenarios like portability and versioning in the coming weeks.

Shippable supports many popular languages such as Ruby, Python, Node.js, and others. We also support services which are commonly used in your applications like MySQL, PostgreSQL, Elastic Search, and others.

Common use cases for Shippable include:

- Automating the packaging and deployment of web applications.
- Automated testing and continuous integration/deployment.

.. note:: Shippable is 100% free to use, even for private repositories.

In this guide, you will learn how to use Shippable for automated testing and then deploy your web application to Heroku if the tests are passed. We will be using Ruby on Rails app in this guide, but you can easily use this guide for other frameworks/languanges as well.

This tutorial assumes that you have:

- A free `Github account <https:/github.com>`_.
- A free `Shippable account <http://www.shippable.com>`_.
- A free `Heroku account <https://signup.heroku.com/signup/dc>`_.
- Ruby on Rails installed your system.

Prepare your app
----------------
We have created a sample `Ruby on Rails application <https://github.com/bsdnoobz/rails-sample-app>`_ on Github for this guide. First you need to `fork the sample code <https://help.github.com/articles/fork-a-repo/>`_ to your Github account and then create a clone to work locally on your computer.

::

    git clone git@github.com:YOUR-USERNAME/rails-sample-app.git

The app is a simple Ruby on Rails project which was generated using the `rails generate scaffold` command. Before doing something with the app, take a look and play around with the app on your computer first. Run the following commands from your terminal:

::

    cd rails-sample-app
    bundle install --without production
    rake db:migrate
    rails server

Access the app by opening ``http://localhost:3000`` from your browser.
