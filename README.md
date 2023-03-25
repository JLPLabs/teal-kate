# teal-kate
Extremely rudimentary Kate 'plugin' for Teal (a typed dialect of Lua) (https://github.com/teal-language).
Also included are two pandoc themes -- one light and one dark.

The author has no business creating Kate syntax xml files, nor pandoc themes, for serious use; please set your expectations accordingly.

The author is assembling a toolchain for creating and posting Teal blog posts.

This plugin provides extremely sparse syntax highlighting for Teal. It was created as part of a toolchain for writing Teal blog posts (pandoc does a lot of heavy liftingfor the author, who really has no busines creating any kind of language tooling for vim.


I'm working on a blog series covering my experiences with Teal and Cyan.

To keep it simple I'm using these tools:

    ReStructured Text files (.rst)
    Pandoc
    Bash script to drive static web generation

To enable syntax-colored code blocks I needed to create tools that Pandoc recognizes:

    Kate style xml syntax parsing
    Pandoc style "theme" for syntax coloring

MY GOAL was an extremely sparse markup. You will see that the only coloring is:

    Declaration of variables.
    Declaration of fields/methods.
    Basic strings (as opposed to long string format, which is not handled)
    Comments

So, attached are:

    teal.xml
    mysparselight.theme
    mysparsedark.theme
    example light screenshot
    example dark screenshot

FUN TO NOTE: 'record' and 'enum' are valid identifiers in Teal. Most (all?) of the editors I looked at that can handle Teal syntax coloring CAN NOT handle 'record' or 'enum' as identifiers. And they kind of lose their minds for a little bit, before recovering.

My parser can handle these. See lines 11 and 14, below, for example.
