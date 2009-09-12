The __graph__ of a [[function]] $f: X \to Y$ is a [[subset]] of the [[cartesian product]] $X \times Y$; $(a,b)$ belongs to the graph of $f$ if and only if $f(a) = b$.

It\'s easy to identify the properties of those subsets of $X \times Y$ that are the graphs of functions, and $f = g$ if they have the same graph (given $X$ and $Y$).  Consequently, it is common, especially (but not only) in material [[set theory]], to *define* a function from $X$ to $Y$ as such a subset, that is to identify a function with its graph.  On the other hand, from a more categorial foundation, it\'s common to define a [[subset]] to be a certain kind of function!

More generally, we can say that the __graph__ of a [[binary relation]] from $X$ to $Y$ is a subset of $X \times Y$; $(a,b)$ belongs to the graph if and only if $a$ is related to $b$.  The __graph__ of a [[relation]] of arbitrary arity is similarly a subset of an arbitrary [[cartesian product]]; see [[relation theory]] for more on this.  Note that *every* subset of $X \times Y$ defines a unique relation; this is the graph of a function if and only if the relation is both [[functional relation|functional]] and [[entire relation|entire]].

The graph of a binary relation from $X$ to $X$ is related to the notion of [[graph]] from [[graph theory]]; more precisely, such relations correspond to directed loop graphs (in the sense defined at [[graph]]) with vertex set $X$, and either can be defined as a subset of $X^2$.  In a similar way, [[spans]] from $X$ to $X$ correspond to [[digraph|directed pseudographs]] with vertex set $X$.

[[Bill Lawvere]] has also considered the __cograph__ of a function, which is dually a [[quotient set]] of the [[disjoint union]] $X \uplus Y$; $a$ is identified with $b$ if $f(a) = b$ (and additional identifications may follow).  This may be even more related to the sense of [[graph]] in graph theory; although the identifications are not done there, the cograph draws a picture in wich any relation (or [[multispan]]) of any arity becomes a directed loop graph (or directed pseudograph) whose vertex set is the disjoint union of the relation\'s domains.

#Discussion#

[[Eric]]: I think it might be neat to take the opportunity here to relate **graph of a function** more explicitly to other things here on the nLab. As I read this, I thought of a category with one object (monoid in Set?) and one morphism

$$\bullet\righttoleftarrow f.$$

Then a graph (or is it cograph?) is a [[category of elements]] of this category.

Then you could maybe talk about **graph of a morhism**. Or something...

[[!redirects graph of a relation]]
[[!redirects cograph]]