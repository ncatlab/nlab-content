
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

An interval is an [[under category]], [[over category]], or under-over category in a [[poset]].


## Definitions

Specifically, given a poset $P$ and an element $x$ of $P$, the __upwards unbounded interval__ $[x,\infty[$ (also $[x,\infty)$, $[x,\infty[_P$, etc) is the [[subset]]
$$ {[x, \infty[} = \{ y : P \;|\; x \leq y \} ;$$
the __downwards unbounded interval__ $]{-\infty}, x]$ (also $(-\infty,x]$, $]{-\infty},x]_P$, etc) is the subset
$$ ]{-\infty}, x] = \{ y : P \;|\; y \leq x \} ;$$
and given an element $y$ of $P$, the __bounded interval__ $[x,y]$ (also $[x,y]_P$) is the subset
$$ [x,y] = \{ z : P \;|\; x \leq z \leq y \} .$$

Thinking of $P$ as a [[category]] and subsets of $P$ as [[full subcategory|subcategories]], $[x,\infty[$ is the [[coslice category]] $(x/P)$, $]{-\infty},x]$ is the [[slice category]] $(P/x)$, and $[x,y]$ is the bislice category $(y/P/x)$.


Besides the __closed intervals__ above, we also have the __open intervals__

*  $ {]x, \infty[} = {[x,\infty[} \setminus \{x\} = \{ y : P \;|\; x \lt y \} ,$
*  $ {]{-\infty}, x[} = {]{-\infty}, x]} \setminus \{x\} = \{ y : P \;|\; y \lt x \} ,$
*  $ {]x, y[} = [x, y] \setminus \{x, y\} = \{ z : P \;|\; x \lt z \lt y \} ,$

as well as the __half-open intervals__

*  $ {[x,y[} = [x,y] \setminus \{y\} = \{ z : P \;|\; x \leq z \lt y \} ,$
*  $ ]x,y] = [x,y] \setminus \{x\} = \{ z : P \;|\; x \lt z \leq y \} .$

These are important in analysis, and more generally whenever the [[quasiorder]] $\lt$ is at least as important as the [[partial order]] $\leq$.


The entire poset $P$ is also considered an __unbounded interval__ in itself.


## Intervals in the real line

Intervals of [[real numbers]] are important in analysis and topology.  The bounded closed intervals in the real line are the original [[compact space]]s.

The __unit interval__ $[0,1]$ is primary in [[homotopy theory]]; a __[[homotopy]]__ from $f$ to $g$ (themselves continuous maps from $A$ to $B$) is a continuous map $h: A \times [0,1] \to B$ such that $h(x,0) = f(x)$ and $h(x,1) = g(x)$ always.  This generalises to the notion of [[interval object]] in an arbitrary category.

The usual [[integral]] in ordinary calculus is done over an interval in the real line, a compact interval for a 'proper' integral, or any interval for an 'improper' integral.  The theory of [[Lebesgue measure]] removes this restriction and allows integrals over any [[measurable subset]] of the real line.  Still, the Lebesgue measure on intervals (even compact intervals) generates all of the rest.

To integrate a $1$-[[differential form|form]] on the real line requires orienting an interval; the standard orientation is from $x$ to $y$ in $[x,y]$.  If $x \gt y$, then $[x,y]$ (which by the definition above would be [[empty set|empty]]) may also be interpreted as $[y,x]$ with the reverse orientation.  This also matches the traditional notation for the integral.


[[!redirects intervals]]
[[!redirects unit interval]]
[[!redirects under-over category]]