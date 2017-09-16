An __endomorphism__ of an [[object]] $x$ in a [[category]] $C$ is an [[morphism]] $f : x \to x$.  An endomorphism that is also an [[isomorphism]] is called an [[automorphism]].

Given an object $x$, the endomorphisms of $x$ form a [[monoid]] under [[composition]], the __endomorphism monoid__ of $x$:

$$
  End_C(x) = Hom_C(x,x)
,$$ 

which may be written $End(x)$ if the category $C$ is understood.  

Up to equivalence, every monoid is an endomorphism monoid; see [[delooping]].

Endomorphism monoid is a special case of a monoid structure on an [[end]] construction. Let $d:D\to C$ be a diagram in $C$, where $C$ is a [[monoidal category]] (in the case above the monoidal structure is the [[cartesian product]] and $d$ is a constant diagram from the initial category). One defines $end(d)$ as an object in $C$, equipped with a natural transformation $a:\mathrm{end}(d)\otimes d\to d$ which is universal in the sense that for all objects $Z\in C$, and any natural transformation $f:Z\otimes d\to d$ there exists a unique morphism $g:Z\to\mathrm{end}(d)$ such $a\circ(g\otimes d)=f:Z\otimes d\to d$. 

+--{: .un_prop}
###### Proposition
If the universal object $(\mathrm{end}(d),a)$ exists then there is a unique structure of a monoid $\mu : \mathrm{end}(d)\otimes\mathrm{end}(d)\to\mathrm{end}(d)$, such that the map $a:\mathrm{end}(d)\otimes d\to d$ is an action. 
=--

[[!redirects endomorphisms]]
[[!redirects endomorphism monoid]]
[[!redirects endomorphism monoids]]