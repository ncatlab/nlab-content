
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
#### Contents
+-- {: .hide}
[[!include contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Searching the nLab

There are several methods of searching the nLab:

1. **The built-in search.**  This is via the search box at the top of every page.  The distinguishing characteristics of this search are:
   1. It uses _regular expressions_.
   1. It searches the _source_ of each page.

1. **Formula Search**:  [nLab Formula Search](https://nlabsearch.mathweb.org/) provides an instance of the [MathWebSearch](https://search.mathweb.org) engine for nLab. 
To use it enter a formula query (LaTeX with query variables of the
form `?a`, `?b`, ...) into the central input box (or just select one of the
examples), wait until the MathML has been rendered (query variables are
red), and hit search. If you click on one of the hits, you get a URL,
which puts you into nLab and highlights the formula hit (in gray).


1. **An external search engine.** 

   Most search engines allow restricting the search to a single site, such as to `ncatlab.org/nlab`.  

   The distinguishing characteristics of an external search are:
   
   1. Usually the search is for alphanumeric characters.
   
   1. It searches the _rendered version_ of each page, instead of the source code.


## Google Search

+-- {: .standout style="text-align: center"}
 *Search the nLab using Google:*
 <form  name="gsearch" method="get" action="http://www.google.com/search"><input type="text" size="30" name="as_q" style="display: inline"/><input type="hidden" name="as_sitesearch" value="http://ncatlab.org/nlab/"/></form>
=--

## Formula Search 

[MathWebSearch](https://search.mathweb.org) (MWS) is a content-based search engine for mathematical formulae.
It indexes MathML formulae, using a technique derived from automated theorem proving: Substitution Tree Indexing.

As the project is still under development, the authors would be happy to hear
your feedback. If you have some comments you can leave it
[here](https://nforum.ncatlab.org/discussion/9792/formula-search/#Item_0). If you
have a bug report or a feature request please open a issue on the github
[repository](https://github.com/MathWebSearch/mws-frontend).


## Regular Expressions

Regular expressions are a powerful way of extending search capabilities to take into account that one often wants to search for more than just a set phrase.  In a regular expression, certain characters are declared to be "special" and have a particular interpretation (somewhat like TeX with its special catcodes).  A special character can always be "escaped" to interpret it as an ordinary character.  Thus `.` means "match any single character" but `\.` means "match a period".

As Instiki is written in ruby, it uses the ruby version of regular expressions (each language has its own version; the differences are usually minor).  The following is based on the list at [ruby-doc](http://www.ruby-doc.org/docs/ProgrammingRuby/html/language.html#UJ).  It has been condensed slightly to those aspects likely to be of use here:

Special characters
: The special characters are: `.`, `|`, `(`, `)`, `[`, `\`, `^`, `{`, `+`, `$`, `*`, and `?`. To match one of these characters, precede it with a backslash.  All other characters ordinarily just match themselves unless they are made somehow special by one of the special characters.

`\b`, `\B`
: Match word boundaries and nonword boundaries respectively.  Thus `cat` matches against `category` and `cat` but `cat\b` only matches `cat` (and `scat`).

`[`...`]`
: This matches against a single character in a list.  The characters `|`, `(`, `)`, `[`, `^`, `$`, `*`, `?` are treated as regular characters in such a list.  You can specify a range using `-`: thus, `a-z`.  To include a `]` or `-` it must come at the start of the list.  A `^` at the start negates the list.

`\d`, `\s`, `\w`
: These match, respectively, digits, spaces, and word characters.

`\D`, `\S`, `\W`
: These are the negations of the lowercase versions.

`.` (period)
: Matches any character except a newline.

`(`...`)`
: Parentheses group pieces of the regular expression.  This is important for the following modifications.  In these, $x$ stands for a sub-expression which can be a single character, a `[`...`]`, or a `(`...`)`.

$x$`*`
: Matches zero or more occurrences of $x$.  Thus `ab*` matches `a`, `ab`, `abb`, and so forth.  Similarly, `(cat)*` matches `cat`, `catcat`, `catcatcat`, and so forth.  This will try to match as much as possible; use $x$`*?` to make it match as little as possible.

$x$`+`
: Matches one or more occurrences of $x$.  Thus `ab+` matches `ab`, `abb`, but not `a`.  This will try to match as much as possible; use $x$`+?` to make it match as little as possible.

$x$`{`$m$`,`$n$`}`
: Matches at least $m$ and at most $n$ occurrences of $re$.  This will try to match as much as possible; use $x$`{`$m$`,`$n$`}?` to make it match as little as possible.

$x$`?`
: Matches zero or one occurrence of $x$.

$x_1$|$x_2$
: Matches either $x_1$ or $x_2$.

[[!redirects Searching nLab]]
[[!redirects searching nLab]]
[[!redirects Searching the nLab]]
[[!redirects searching the nLab]]
[[!redirects Searching in the nLab]]
[[!redirects searching in the nLab]]

category: meta
