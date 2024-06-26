+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea ##

A class $W$ of [[weak equivalence]]s in a [[category]] $C$ is said to admit a **calculus of fractions** if it satisfies some axioms ensuring that its [[localization]] $C[W^{-1}]$ can be constructed in a particularly simple way using 'one-step generalized morphisms.'  These axioms are a categorical analogue of the notion of a [[multiplicative system]] at which one can localize a ring.

Since composition in a category is generally non-commutative, we distinguish 'left' and 'right' calculi of fractions, just as for localization of non-commutative rings.  In either case $C[W^{-1}]$ is referred to as a [[category of fractions]], since its morphisms are two-step zigzags (either $\overset{f}{\to} \overset{w}{\leftarrow}$ or $ \overset{w}{\leftarrow} \overset{f}{\to}$, depending on the handedness of the calculus) in which $w\in W$, which we can think of  as 'fractions' $w^{-1} f$ or $f w^{-1}$.  One sometimes also says that $(C,W)$ 'admits a category of fractions.'


## Definition ##

A pair $(C,W)$ of a [[category]] $C$ and a class of [[morphism]]s $W$ is said to admit a **calculus of right fractions** if the following properties hold.

* $W$ is a [[wide subcategory]] of $C$ (that is, $W$ contains all [[identity morphisms]] and is closed under [[composition]]).

* (right Ore condition) Given a [[morphism]] $v \colon x\to z$ in $W$ and any morphism $f \colon y\to z$, there is a morphism $v' \colon w \to y$ in $W$ and a morphism $f' \colon w \to x$ in $C$ such that the following [[commuting diagram|diagram commutes]]:

$$
\begin{matrix}
  w & \overset{f'}{\longrightarrow} & x 
  \\
  \mathllap{{}^{v'}} 
  \Big\downarrow
  && 
  \Big\downarrow\mathrlap{{}^{v}}
  \\
  y &\underset{f}{\longrightarrow} & z
\end{matrix}
$$


* (right cancellability) Given a morphism $v \colon y\to z$ in $W$ and a [[pair]] of [[parallel morphisms]] $f,g \colon  x\to y$ such that $v\circ f = v \circ g$, there is a morphism $v' \colon w\to x$ in $W$ such that $f\circ v' = g \circ v'$:
$$ 
  w \xrightarrow{v'} x 
    \underoverset{g}{f}{\rightrightarrows} y 
  \xrightarrow{v} z\,.
$$

One may also say that $W$ is a **right Ore system** in $C$ (although this is potentially confusing since the Ore condition is only part of the definition), or that $(C,W)$ **admits a category of right fractions**.  If $(C^{op}, W^{op})$ admits a calculus of right fractions, we say that $(C,W)$ admits a **calculus of left fractions**.  Unfortunately there is no uniformity regarding the choice of 'left' versus 'right;' some authors use 'left' where we use 'right' and vice versa.

### Additional conditions

It is common to assume additional closure conditions on $W$ which make no difference to the localization.  For example, one often assumes that $W$ contains all isomorphisms in $C$.  One can also assume the [[2-out-of-3 property]] (so that $(C,W)$ is a [[category with weak equivalences]]) or the stronger [[2-out-of-6 property]] (so that $(C,W)$ is a [[homotopical category]]).  Note that the 2-out-of-3 property includes closure under composition, and the 2-out-of-6 property together with containment of all identities implies containment of all isomorphisms.

In the presence of either sort of calculus of fractions, the 2-out-of-6 property is equivalent to _saturation_ of $W$, i.e. that any morphism in $C$ which becomes an isomorphism in $C[W^{-1}]$ is already in $W$.  Therefore, in this case we may equivalently call $(C,W)$ _saturated_.  See [[2-out-of-6 property]] for a proof, taken from 7.1.20 of [[Categories and Sheaves]] (where a pair $(C,W)$ admitting a calculus of left fractions is called a _right multiplicative system_). 


## Construction of the localization ##

Suppose that $(C,W)$ admits a calculus of right fractions.  Then the [[localization]] of $C$ at $W$ can be realized by taking the same objects as in $C$ and the [[hom-set]] $C[W^{-1}](a,b)$ to be the set of [[equivalence classes]] of [[span|spans]] whose left leg is in $W$, under the equivalence relation where $a\stackrel{v}\leftarrow a'\stackrel{f}\rightarrow b$ is equivalent to $a\stackrel{w}\leftarrow a''\stackrel{g}\rightarrow b$ iff there exists an object $\bar{a}$
and morphisms $s:\bar{a}\to a'$, $t:\bar{a}\to a''$ such that $f\circ s = g\circ t$, $v\circ s = w\circ t$, and $v\circ s = w\circ t$ is in $W$.  We denote the equivalence class of $a\stackrel{v}\leftarrow a'\stackrel{f}\rightarrow b$ by $f\circ v^{-1}$.

These equivalence classes compose as follows: take a representative $a\stackrel{v}\leftarrow a'\stackrel{f}\rightarrow b$ and a representative $b\stackrel{u}\leftarrow b'\stackrel{h}\rightarrow c$; then by the Ore condition there exist morphisms $z:d\to a'$ and $k:d\to b'$, where $z\in W$, such that $f\circ z= u\circ k$.  The composition $(h\circ u^{-1})\circ (f\circ v^{-1})$ is the equivalence class of the span $a\stackrel{v\circ z}\leftarrow d\stackrel{h\circ   k}\rightarrow c$.  One proves that this definition does not depend on the choice of representatives, and that it is associative with units $1_a\circ 1^{-1}_a$.  Obviously, the localization functor $C\to C[W^{-1}]$ sends a morphism $p : a\to b$ to $p\circ 1^{-1}_a$.

If instead $(C,W)$ admits a calculus of left fractions, the hom-sets of $C[W^{-1}]$ are equivalence classes of [[cospan]]s (spans in opposite category).  In fact, we can realize $C[W^{-1}]$ as $(C^{\mathrm{op}}[(W^{\mathrm{op}})^{-1}])^{\mathrm{op}}$.  Note that _two_ dualizations are involved, in order to get the cospans to be pointing in the correct direction.

An equivalent way to say this is that if $W$ admits a calculus of right fractions, then the hom-sets in $C[W^{-1}]$ are obtained as the colimit over maps in $C$ out of a $W$-replacement of the source object:
$$
  Hom_{C[W^{-1}]}(X,Y) = \underset{X' \stackrel{p \in W}{\to}X}{colim} Hom_C(X',Y).
$$
Dually, if $W$ admits a calculus of left fractions,  we instead take the colimit over maps into a $W$-replacement under the target object:
$$
  Hom_{C[W^{-1}]}(X,Y) = \underset{Y \stackrel{i \in W}{\to} Y'}{colim} Hom_C(X,Y').
$$
If $W$ admits both a left and a right calculus of fractions, then both prescriptions coincide and are equivalent to taking a colimit over replacements of both objects:
$$
  \begin{aligned}
    Hom_{C[W^{-1}]}(X,Y) &= 
    \underset{X' \stackrel{p \in W}{\to}X}{colim} Hom_C(X',Y)
    \\
      &= \underset{Y \stackrel{i \in W}{\to} Y'}{colim} Hom_C(X,Y')
    \\
      &= 
      \underset{X' \stackrel{p \in W}{\to}X, 
        Y \stackrel{i \in W}{\to} Y'}{colim} Hom_C(X',Y')
  \end{aligned}
  \,.
$$

## Properties of the Localization ##

One important consequence of this construction is that when $W$ admits a calculus of right fractions, the localization functor $Q:C\to C[W^{-1}]$ is left [[exact functor|exact]], and therefore preserves all finite [[limit]]s existing in $C$.  Dually, if $W$ admits a calculus of left fractions, then $Q$ is right exact and preserves finite colimits.

Another important fact is that if

* $W$ admits a calculus of right fractions,
* $C$ admits all small [[filtered colimits]], and
* for all $X \in C$ the category $W/X$, whose objects are morphisms $X'\to X$ in $W$ and whose morphisms are commutative triangles, is [[cofinally small category|cofinally small]],

then $C[W^{-1}]$ is [[locally small category|locally small]].  In this case a left [[derived functor]] of any functor $F:C\to A$, where $A$ admits small filtered colimits, can be constructed as the colimit
$$
  R_W F(X)
  =
  \underset{X \stackrel{s \in W}{\to} X'}{\colim} F(X').
$$


## Examples ##

* If $C$ is a [[category of fibrant objects]] and $\pi C$ its
category of morphisms modulo [[homotopy]], the collection of 
weak equivalences in $\pi C$ admits a calculus of right fractions.  The corresponding localization is the homotopy category $\Ho(C)$ of $C$.  Note that this example does not satisfy the 2-out-of-3 property.

* Given a [[null system]] $N$ in a [[triangulated category]] $C$,
the collection of morphisms $f : X \to Y$ in $C$ such that
there is a distinguished triangle $X \to Y \to Z$ where $Z \in N$
admits calculi of both left and right fractions. 

* For $S$ a [[site]], the collection of [[local epimorphism]]s
in $C = [S^{op},Set]$ with respect to the given [[Grothendieck topology]] on $S$ admits a calculus of right fractions.  In this case the localization is the [[category of sheaves]] on $S$.

## Related concepts

* [[localization]]

* [[colocalization]]


## References

> See also references at *[[category of fractions]]*.

The original monograph:

* [[Pierre Gabriel]], [[Michel Zisman]], _[[Calculus of fractions and homotopy theory]]_, _Ergebnisse der Mathematik und ihrer Grenzgebiete_, Band 35. Springer, New York (1967) &lbrack;[doi:10.1007/978-3-642-85844-4](https://link.springer.com/book/10.1007/978-3-642-85844-4), [pdf](https://web.math.rochester.edu/people/faculty/doug/otherpapers/GZ.pdf)&rbrack;

See also

* [[Frank Adams]], part III, section 14 of _[[Stable homotopy and generalised homology]]_, 1974

* {#Borceux94} [[Francis Borceux]], vol 1, chapter 5 of: _[[Handbook of Categorical Algebra]], Cambridge University Press (1994)

* {#Fritz11} [[Tobias Fritz]], *Categories of Fractions Revisited*, Morfismos **15**  2 (2011) 19-38 &lbrack;[arXiv:0803.2587](https://arxiv.org/abs/0803.2587), [morfismos:vol15-n2-3](https://morfismos.math.cinvestav.mx/sites/default/files/Upload/vol15-n2-3.pdf)&rbrack;


Generalization from categories to [[quasi-categories]] ("$(\infty,1)$-calculus of fractions", cf. at *[[localization of an (infinity,1)-category|localization of an $(\infty,1)$-category]]*):

* [[Daniel Carranza]], [[Chris Kapulkin]], [[Zachery Lindsey]], *Calculus of Fractions for Quasicategories* &lbrack;[arXiv:2306.02218](https://arxiv.org/abs/2306.02218)&rbrack;

Exposition:

* [[Chris Kapulkin]], *Calculus of Fractions for Quasicategories (Part I)*, [talk at](CQTS#KapulkinOct2023) [[CQTS]] (18 Oct 2023) &lbrack;video:[YT](https://youtu.be/96ViSKAuApc)&rbrack;

* [[Daniel Carranza]], *Calculus of Fractions for Quasicategories (Part II)*, [talk at](CQTS#CarranzaOct2023) [[CQTS]] (25 Oct 2023) &lbrack;video:[YT](https://youtu.be/Z41YDb99cZk)&rbrack;


[[!redirects left calculus of fractions]]
[[!redirects right calculus of fractions]]
[[!redirects calculus of left fractions]]
[[!redirects calculus of right fractions]]


