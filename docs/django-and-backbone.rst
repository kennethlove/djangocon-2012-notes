=========================================================
Creating Dynamic Applications with Django and Backbone.js
=========================================================

Mjumbe Poe

Overview
========

* Backbone.js is cool, but sorry for all the JS
* Hijax: Accessibility is important
* Django REST Framework: it's cool & we're goinna make it cooler
* Templating in Django: Great but could be better.

Django Analogues
================

* Backbone has models, which are roughly like Django models
    * No defined structure
    * Also has form-like responsibilities, like validation
* Backbone has collections, which are like Django model managers or querysets
    * Use them find/destroy/iterate through instances of models
* Backbone has events, which are similar to Django signals
* Backbone has views which are managers of portions of the page
* Backbone has routers which are similar to urlpatterns in Django

RESTful API
===========

* Using a basic `views.View` view from Django REST Framework (not what I'd consider best practices -kl)

Hijax
=====

* Plan for AJAX from the start, but implement at the end.
