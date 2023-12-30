
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition

A [[functor]] $F: C \to B$ is a **discrete fibration** if for every object $c$ in $C$, and every morphism of the form $g : b\to F(c)$ in $B$ there is a unique morphism $h : d\to c$ in $C$ such that $F(h) = g$.  

A functor $F: C \to B$ is a **discrete opfibration** if $F^{op}:C^{op}\to B^{op}$ is a discrete fibration. 

A discrete fibration is a special case of a [[Grothendieck fibration]], namely one where each [[fiber]] is a [[set]].

Given a cartesian category $E$, [[internal categories]] $C,B$ in $E$, an internal functor $F: C \to B$ is a **discrete fibration of internal categories** if the square
$$\begin{matrix}
C_1 &\stackrel{F_1}\to& B_1\\
d_0\downarrow && \downarrow d_0\\
C_0 &\stackrel{F_0}\to& B_0
\end{matrix}$$
is cartesian.

## Discussion via category of elements

Given a discrete fibration $F: C \to B$, define a functor $F^*: B^{op} \to Set$ as follows:

*  For $x$ an object of $B$, let $F^*(x)$ be the set of objects $y$ of $C$ such that $F(y) = x$.
*  For $g: x \to y$ a morphism of $B$, let $F^*(g): F^*(y) \to F^*(x)$ be the function that maps each element of $F^*(y)$ to the unique $d$ determined by the definition of discrete fibration above.

There is a size issue here, is $F^*(x)$ in fact [[small category|small]]?  We say that the fibration has **small fibres** if so; else we must pass to a larger [[universe]] when we define [[Set]].


Conversely, give a functor $F^*: B^{op} \to Set$, define a category $C$ and a discrete fibration $F: C \to B$ as follows:

*  Let $C$ be the [[category of elements]] of the functor $F^*$; that is:
   *  an object of $C$ is a pair consisting of an object $x$ of $B$ and an element of $F^*(x)$,
   *  a morphism from $(x,a)$ to $(y,b)$ in $C$ is a morphism $g: x \to y$ in $B$ such that $F^*(g)$ maps $b$ to $a$.
*  The functor from $C$ to $B$ is the obvious [[forgetful functor]].


If you start from $F^*$, construct $C$ and $F$, and then construct a new $F^*$, it will be equal to the original $F^*$.  Conversely, if you start with $C$ and $F$, construct $F^*$, and then construct a new $C'$ and $F'$, then there will be an [[isomorphism of categories]] between $C$ and $C'$, relative to which $F$ and $F'$ are equal.

Under this equivalence, the [[representable presheaf]] on an object $X$ corresponds to the canonical functor $B/X \to B$ from the [[slice category]] over $X$.

## Invariance under equivalence

Note that the definition of fibration refers to [[equality]] of morphisms without previously assuming that the sources match, while the construction of $F^*$ from $F$ refers to equality of objects.  This is also why we get [[equality]] of [[functors]] and [[isomorphism]] of [[categories]] in the immediately preceding paragraph.  So the only thing on this page which respects the [[principle of equivalence]] is the idea of a functor to [[Set]].  That is the fundamental invariant notion; a discrete fibration is just a convenient way of talking about it.

## Further properties

* Just as general [[Grothendieck fibration|fibrations]], discrete fibrations are stable under [[pullbacks]] in [[Cat]].

* Discrete (op)fibrations are the right class of the [[comprehensive factorisation system]]. 

## Generalization for spans internal to a category

Let $E$ be a cartesian category.
A span of [[internal categories]] $A\stackrel{p}\leftarrow C\stackrel{q}\to B$ in $Cat(E)$ is called a **discrete fibration from $A$ to $B$** if in the diagram

$$\begin{matrix}
A_0 & \leftarrow & C_l && \\
\downarrow &&\downarrow i_l &&\\
A &\stackrel{p}\leftarrow & C &\stackrel{i_r}\leftarrow & C_r\\
&&q \downarrow && \downarrow \\
&& B &\leftarrow & B_0
\end{matrix}$$

in which the two squares are the cartesian satisfies the following 3 properties:

* $p\circ i_r : C_1\to A$ is a discrete fibration 

* $q\circ i_l: C_l\to B$ is a discrete opfibration

* Let $X$ be defined as the pullback
$$\begin{matrix}
X & \to & (C_r)_1 \\
\downarrow &&\downarrow \\
(C_l)_1 &\to & C_0 
\end{matrix}$$
and $j:X\hookrightarrow C_1\times_{C_0} C_1$ the canonical inclusion. Then 
the morphism $c\circ j : X\to C_1$, where $c: C_1\times_{C_0} C_1\to C_1$ is the composition morphism of internal category $C$, is invertible.

**Example.** Given internal functors $a : A\to D$ and $b : B\to D$ in $E$, the obvious span $A\leftarrow a\downarrow b\rightarrow B$ is a discrete fibration from $A$ to $B$. 

## Related concepts

* [[fibration fibered in groupoids]]

* [[Grothendieck fibration]], [[Grothendieck construction]]


## References

Review:

* [[Angelo Vistoli]], §3.4 in: *Grothendieck topologies, fibered categories and descent theory*, in: *[[Fundamental algebraic geometry -- Grothendieck's FGA explained]]*, Mathematical Surveys and Monographs **123**, Amer. Math. Soc. (2005) 1-104 &lbrack;[ISBN:978-0-8218-4245-4](https://bookstore.ams.org/surv-123-s), [math.AG/0412512](http://arxiv.org/abs/math/0412512)&rbrack;

See also:

* [[Emily Riehl]] and [[Fosco Loregian]], _Categorical notions of fibration_, Expositiones Mathematicae **38** 4 (2020) 496-514 &lbrack;[arXiv:1806.06129](https://arxiv.org/abs/1806.06129), [doi:10.1016/j.exmath.2019.02.004](https://doi.org/10.1016/j.exmath.2019.02.004)&rbrack;

A joint generalisation of the notions of discrete fibrations and [[discrete opfibrations]] are studied in the following paper under the name *unique factorization liftings*, i.e. [[discrete Conduché functors]]:

* [[Marta Bunge]], [[Susan Niefield]], _Exponentiability and single universes_, JPAA **148** (2000) 217--250


[[!redirects discrete fibration]]
[[!redirects discrete fibrations]]
[[!redirects discrete opfibration]]
[[!redirects discrete opfibrations]]

