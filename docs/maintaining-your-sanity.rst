==============================================================
Maintaining Your Sanity While Maintaining Your Open Source App
==============================================================

Mark Lavin

Packaging
=========

* Use pip
* PEP 386
* List a description and `__version__` number in `__init__.py` 

Anti-Patterns
=============

* giant README
* Docs which aren't available online
* Use Sphinx and RTD
* Create docs before you think you need them

Things to Document
==================

* Description of the project and its goals
* How to install, including requirements
* How to configure
* Release notes (not svn/git/hg logs)

Test Only Models
================

* Define models in tests.py and they're only available to the test runner (already used by Django)

Testing
=======

* Tox uses virtualenv to run a test matrix
  * different Python versions
  * different Django versions
  * different DB backends
* You can have Tox build your Sphinx docs
* sul
