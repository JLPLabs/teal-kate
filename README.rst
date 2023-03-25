teal-kate
=========

Abstract
--------

Extremely rudimentary Kate syntax xml for Teal (a typed dialect of Lua)
`<https://github.com/teal-language`_ 

Also included are two pandoc themes -- one light and one dark.

Caution
-------

The author has no business creating Kate syntax xml files, nor pandoc themes,
for serious use.

**Please set your expectations accordingly.**

Overview
--------

The author is working on a blog series covering their experiences with Teal and
Cyan `<https://github.com/teal-language/cyan>`_, and an intentionally simple
tool chain is being used to support this effort:

* ReStructured Text files (.rst)
* Pandoc
* Bash script to drive static web generation

To enable syntax-colored code blocks we needed to create tools that Pandoc
recognizes:

* Kate style xml syntax parsing
* Pandoc style "theme" for syntax coloring

The GOAL was an extremely sparse syntax markup. You will see that the only
coloring is:

* *Declaration* of variables.
* *Declaration* of fields/methods.
* Basic strings (as opposed to long string format, which is not handled)
* Comments

record and enum as Identifiers
------------------------------

FUN TO NOTE: 'record' and 'enum' are valid identifiers in Teal. Most (all?) of
the editors the author looked at that can handle Teal syntax coloring CAN NOT
handle 'record' or 'enum' as identifiers. And they kind of lose their minds for
a little bit, before recovering.

This Kate parser **can** handle these. See lines 11 and 14 in the screenshots
below, for example.

Files
-----

teal.xml

  Syntax coloring rules in the Kate format.

mysparselight.theme

  Light coloring Pandoc theme

mysparsedark.theme

  Dark coloring Pandoc theme

Examples
--------

A light screenshot

A dark screenshot

