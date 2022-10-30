## tests for iTex accents

see: [nforum: feynman-slash-notation](https://nforum.ncatlab.org/discussion/8087/feynman-slash-notation)

Toby:
> I currently have an example sitting in the [[Sandbox]].

If you link to the sandbox for your slash example you should give a version number, i.e. [Sandbox/1328](https://ncatlab.org/nlab/revision/Sandbox/1328).

> I don't know why it doesn't work on the Forum

I decided to test all the accents listed at [https://golem.ph.utexas.edu/~distler/blog/itex2MMLcommands.html#itex2MMLAccents](https://golem.ph.utexas.edu/~distler/blog/itex2MMLcommands.html#itex2MMLAccents)

\bar, \overline ( = \closure  = \widebar), \underline, \vec, \widevec( = \overrightarrow), \overleftarrow, \dot, \ddot, \dddot, \ddddot, \tilde, \widetilde, \check, \widecheck, \hat, \widehat, \slash, \boxed 

* `a\bar{A}b\bar{BBB}c\bar{\partial}d`

*  $a\bar{A}b\bar{BBB}c\bar{\partial}d$

* `a\overline{A}b\overline{BBB}c\overline{\partial}d`

*  $a\overline{A}b\overline{BBB}c\overline{\partial}d$

* `a\underline{A}b\underline{BBB}c\underline{\partial}d`

*  $a\underline{A}b\underline{BBB}c\underline{\partial}d$

* `a\vec{A}b\vec{BBB}c\vec{\partial}d`

*  $a\vec{A}b\vec{BBB}c\vec{\partial}d$

* `a\widevec{A}b\widevec{BBB}c\widevec{\partial}d`

*  $a\widevec{A}b\widevec{BBB}c\widevec{\partial}d$

* `a\overleftarrow{A}b\overleftarrow{BBB}c\overleftarrow{\partial}d`

*  $a\overleftarrow{A}b\overleftarrow{BBB}c\overleftarrow{\partial}d$

* `a\dot{A}b\dot{BBB}c\dot{\partial}d`

*  $a\dot{A}b\dot{BBB}c\dot{\partial}d$

* `a\ddot{A}b\ddot{BBB}c\ddot{\partial}d`

*  $a\ddot{A}b\ddot{BBB}c\ddot{\partial}d$

* `a\dddot{A}b\dddot{BBB}c\dddot{\partial}d`

*  $a\dddot{A}b\dddot{BBB}c\dddot{\partial}d$

* `a\ddddot{A}b\ddddot{BBB}c\ddddot{\partial}d`

*  $a\ddddot{A}b\ddddot{BBB}c\ddddot{\partial}d$

* `a\tilde{A}b\tilde{BBB}c\tilde{\partial}d`

*  $a\tilde{A}b\tilde{BBB}c\tilde{\partial}d$

* `a\widetilde{A}b\widetilde{BBB}c\widetilde{\partial}d`

*  $a\widetilde{A}b\widetilde{BBB}c\widetilde{\partial}d$

* `a\check{A}b\check{BBB}c\check{\partial}d`

*  $a\check{A}b\check{BBB}c\check{\partial}d$

* `a\widecheck{A}b\widecheck{BBB}c\widecheck{\partial}d`

*  $a\widecheck{A}b\widecheck{BBB}c\widecheck{\partial}d$

* `a\hat{A}b\hat{BBB}c\hat{\partial}d`

*  $a\hat{A}b\hat{BBB}c\hat{\partial}d$

* `a\widehat{A}b\widehat{BBB}c\widehat{\partial}d`

*  $a\widehat{A}b\widehat{BBB}c\widehat{\partial}d$

* `a\slash{A}b\slash{BBB}c\slash{\partial}d`

*  $a\slash{A}b\slash{BBB}c\slash{\partial}d$

* `a\boxed{A}b\boxed{BBB}c\boxed{\partial}d`

*  $a\boxed{A}b\boxed{BBB}c\boxed{\partial}d$

In the nForum `\overleftarrow` is unknown while `\slash` and `boxed` silently eat their arguments.
In nLab all of these work.

NOTE however that some extra white space sometimes appears between letters.






$\,$

$\,$

$\,$

$\,$


