**************************
Frequently Asked Questions
**************************

Can Idris 2 compile itself?
===========================

Yes, Idris 2 is implemented in Idris 2. By default, it targets
`Chez Scheme <https://cisco.github.io/ChezScheme/>`_, so you can bootstrap
from the generated Scheme code, as described in Section :ref:`sect-starting`.

Why does Idris 2 target Scheme? Surely a dynamically typed target language is going to be slow?
===============================================================================================

You may be surprised at how fast Chez Scheme is :). `Racket <https://download.racket-lang.org/>`_,
as an alternative target, also performs well. Both perform better than the
Idris 1 back end, which is written in C but has not had the decades of
engineering effort by run time system specialists that Chez and Racket have.

Chez Scheme also allows us to turn off run time checks, which we do.

This is, nevertheless, not intended to be a long term solution, even if it
is a very convenient way to bootstrap.

Can Idris 2 generate Javascript? What about plug-in code generators?
====================================================================

Not yet, but there is a Javascript code generator in development.

Like Idris 1, Idris 2 will support plug-in code generation to allow you to
write a back end for the platform of your choice, but this is not yet
implemented.

What are the main differences between Idris 1 and Idris 2?
==========================================================

The most important difference is that Idris 2 explicitly represents *erasure*
in types, so that you can see at compile time which function and data type
arguments are erased, and which will be present at run time. You can see more
details in :ref:`sect-multiplicities`.

Idris 2 has significantly better type checking performance (perhaps even an
order of magnitude!) and generates significantly better code.

Also, being implemented in Idris, we've been able to take advantage of the
type system to remove some significant sources of bugs!

You can find more details in Section :ref:`updates-index`.

Where can I find more answers?
==============================

The `Idris 1 FAQ <http://docs.idris-lang.org/en/latest/faq/faq.html>`_ is
mostly still relevant.
