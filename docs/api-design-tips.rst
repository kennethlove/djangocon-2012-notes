===============
API Design Tips
===============

Daniel Lindsley

What?
=====

* Not HTTP APIs
* Programmatic APIs
* Think libraries
    * especially ones you hand off to other people…

Why?
====

* Think about how many times you've started with someone else's library…
* Used it some…
* Then got really upset and frustrated

* Other people use your code all the time

* Nice APIs begets *Happiness*
* Happiness begets *Recommendations*
* Recommendations beget *Users/Community*

Philosophy
==========

* You can't make everyone happy by default
    * You should still have sane defaults
* But *more* people will be happy if they can tweak it
    * You can bet they'll need to
* And most people will be happy if it's easy to tweak
* No copy-paste should be needed
    * Boilerplate sucks
* They shouldn't have to constantly refer to the docs
    * Especially not for things they use *all* the freaking time
* Good docs matter
    * Saves you (support) & them (implementation) time. Everyone wins
* Real World use is the best sanity check
* Someone is going to something weird/insane with your code
    * It's inevitable, so design for it up front

Approaches on Design
====================

* Common Methodologies:
    * Bottom-up
        * small components over time that eventually all work together in the final product
    * Top-down
        * build the ideal code at first, then writing the underlying code to make the ideal real
* Bottom-up sucks
    * sure, you built little pieces that work
    * but do they really work well together?
        * likely not
        * how is php formed
* Top-down feels better
    * everything fits together right
    * less duplication
    * helps you to resist the urge to duct tape things together
* With some instant TDD, you get your tests started from the get-go
    * fewer massive, painful refactories down the road

Things You Should Do
====================

* Small components
    * worked for UNIX, it'll work for you
* Composition >= Inheritance
    * Why do the work yourself when you can delegate?
* Reflection
    * If data can flow one way, add the opposite
* Broad familiarity
    * If it's a similar task to something else they know, mimic that something else
* Narrow familiarity
    * Call signatures matter
* Assume the worst
    * Don't code for just the easy case

Things You Should Not Do
========================

* Stop at a low level
* Wildly different return values
* Useless "implementation" code
* If it's difficult to test...

Django-specific Topics
======================

* Pluggable backend all the things
* Internationalize all the things
* Dynamically loaded classe/code
    * 60% more error-handling, every time
* Declarative syntax
    * Metaclasses: call your doctor if headaches last more than 4 hours
* *Don't* metaclass all the things
* The ORM
    * Love it or hate it, there's some great learning opportunities there
* Decrease reliance on `self`
* Resist the urge to magic
    * Be explicit *first*, then add shortcuts (which can be a little more magical)

In Conclusion
=============

* Use the golden rule
* Consistency is key
* Plan for the worst & include sweet shortcuts
* Make something that you love and make it better
