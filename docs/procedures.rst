.. Currently in heavily development.  Will use shorthand until ready to refine.

Procedures
**********

A number of things are automated from the start with this project.  This
document outlines the typical procedures that a developer would typically go
through manually, and notes where automated alternatives have been supplied.


Initial Setup
=============

Assume that a project has already been started with a project template as
described in README.

Provisioning
============

I'd like to set up some simple provisioning for:

#. Heroku
#. DigitalOcean
#. Heroku with S3
#. AWS

In that order of priority. At first, Heroku will be the only option,
with others coming later.

Heroku
------

See `Heroku Article https://devcenter.heroku.com/articles/django`_.

::
    heroku create {{ project_name }}
    echo '-r requirements/production_heroku.txt' > requirements.txt

Precompiled Assets
==================

I want to reclaim my SASS and (maybe someday) HAML.  Will largely be 
implementation specific.  May have to dig into collectstatic. Need to decide
between compass or django-compressor. Needs to support automatic AWS static
hosting via S3 / cloudfront.
