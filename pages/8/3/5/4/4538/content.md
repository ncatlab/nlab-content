
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Cohomology
+-- {: .hide}
[[!include cohomology - contents]]
=--
#### Homological algebra
+-- {: .hide}
[[!include homological algebra - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

For $C_\bullet$ a [[chain complex]] (of [[abelian group]]s) and $F$ a [[field]] the [[homology group]] $H_p(C,F)$ and the [[cohomology group]] $H^p(C,F)$ are related simply by dualization

$$
  H^p(C,F) \simeq Hom_F(H_p(C,F), F)
  \,.
$$

If the coefficients is not a [[field]] but an arbitrary [[abelian group]], then this relationship is more complicated and is expressed by the _universal coefficient theorem_. 


## Statement

### For ordinary cohomology

Let $C_\bullet$ be a [[chain complex]] of [[free construction|free]] [[abelian group]]s. Let $A$ be an arbitrary [[abelian group]]. 

Write 

* $C^\bullet \coloneqq Hom_{Ab}(C_\bullet, A)$ for the dual [[cochain complex]] with respect to $A$;

* $H_n(C,\mathbb{Z})$ for the [[chain homology]] of $C$

* $H^n(C,A)$ for the [[cochain cohomology]] of $C^\bullet$.

+-- {: .num_note }
###### Observation

There is a canonical morphism of [[abelian group]]s

$$
  \int_{(-)}(-) : H^n(C,A) \to Hom_{Ab}(H_n(C,\mathbb{Z}), A)
$$

given by sending a cocycle to evaluation of that cocycle 

$$
  [\omega] \mapsto 
   \left( [\sigma] \mapsto \int_{\sigma} \omega \coloneqq \omega(\sigma) \right)
$$

=--

+-- {: .num_theorem }
###### Theorem
**(universal coefficient theorem)**

The morphism $h$ is surjective and its [[kernel]] is the [[Ext group]] $Ext^1(H_{n-1}(C, \mathbb{Z}), A)$. In other words, there is 
a [[short exact sequence]]

$$
  0 \to 
   Ext^1(H_{n-1}(C, \mathbb{Z}), A)
   \to 
   H^n(C, A) 
   \to 
   Hom(H_n(C,\mathbb{Z}), A)
   \to 
   0
  \,.
$$

=--

+-- {: .num_section #sectiona }
=--


### For generalised cohomology theories
{: .num_section}

The situation for [[generalised cohomology theories]] is much more complicated than that for ordinary cohomology due to the fact that it is harder (or impossible!) to use the tools of chain complexes. Nonetheless, it is possible to say something. The general case was studied by Adams in [Ada69](#Ada69) and the initial version of the rest of this section is heavily based on that treatment.  This was also considered in the slightly later work, [Ada74, Chapter 13](#Ada74). Adams' opening paragraph in [Ada69](#Ada69) is worth quoting in its entirety as motivation for this study.

> It is an established practice to take old theorems about ordinary homology, and generalise them so as to obtain theorems about generalised homology theories. For example, this works very well for duality theorems about manifolds. We may ask the following question. Take all those theorems about ordinary homology which are standard results in every day use. Which are the ones which still lack a fully satisfactory generalisation to generalised homology theories? I want to devote this lecture to such problems.

> *J. F. Adams*{: style="text-align: right"}

The lecture concentrates on the Universal Coefficient Theorem and, as a by-product, the [[Künneth theorem]]. 

Let $E^*$ and $F^*$ be two [[generalized cohomology theories]] and $E_*$ and $F_*$ two [[generalized homology theories]].
Then the general problems that a Universal Coefficient Theorem should apply to are the following:

1. <p></p>
   +-- {: .num_enuma #enumiAa }
   =--
   Given $E_{*}(X)$, calculate $F_{*}(X)$.

2. <p></p>
   +-- {: .num_enuma #enumiAb }
   =--
   Given $E_{*}(X)$, calculate $F^{*}(X)$.

3. <p></p>
   +-- {: .num_enuma #enumiAc }
   =--
   Given $E^{*}(X)$, calculate $F_{*}(X)$.

4. <p></p>
   +-- {: .num_enuma #enumiAd }
   =--
   Given $E^{*}(X)$, calculate $F^{*}(X)$.

In [Ada69](#Ada69), Adams works in a very general setting. On this page, we shall work in a more restricted situation (as spelled out in Note 2 in Adams' lectures). We assume that $E^{*}(-)$ is the [[generalised cohomology theory]] associated to a [[commutative ring spectrum]], $E$. The cohomology theory $F^{*}(-)$ is assumed to come from a left [[module-spectrum]] over $E$, which we shall denote by $F$. We do not assume that $F$ is itself a ring spectrum. Following Adams, we shall also assume that all our cohomology and homology theories are [[reduced cohomology|reduced]].

There are two statements that one would like to hold. These are not themselves theorems, rather the theorem would say ''Under certain conditions, these statements hold''. The statements are the following.

+-- {: .num_uct #ucta .thremark }
###### UCT1
There is a [[spectral sequence]]
$$
\Tor_{p,*}^{E_{*}} (E_{*}(X), F_{*}) \xRightarrow[p]{}    F_{*}(X)
$$
with edge homomorphism
$$
E_{*}(X) \otimes _{E_{*}} F_{*} \to F_{*}(X).
$$
=--

+-- {: .num_uct #uctb .thremark }
###### UCT2
There is a spectral sequence
$$
\Ext_{E_{*}}^{p,*} (E_{*}(X), F^{*}) \xRightarrow[p]{}    F^{*}(X)
$$
with edge homomorphism
$$
F^{*}(X) \to \Hom_{E_{*}} (E_{*}(X), F^{*}).
$$
=--

For finite [[CW-complexes]] then we can derive two further statements from the above by [[S-duality]]. We use the notation $D X$ for the [[Spanier-Whitehead dual]] of $X$.

For a finite CW-complex $X$, we can apply [UCT1](#ucta) and [UCT2](#uctb) to $D X$ in place of $X$ and then use the various isomorphisms relating the cohomologies of $X$ and $D X$ to reformulate them in terms of $X$. We thus get the following statements.

+-- {: .num_uct #uctc .thremark }
###### UCT3
For $X$ a finite CW-complex, there is a spectral sequence
$$
\Tor_{p,*}^{E^{*}}(E^{*}(X), F^{*}) \xRightarrow[p]{}    F^{*}(X)
$$
with edge homomorphism
$$
E^{*}(X) \otimes _{E^{*}} F^{*} \to F^{*}(X).
$$
=--

+-- {: .num_uct #uctd .thremark }
###### UCT4
For $X$ a finite CW-complex, there is a spectral sequence
$$
\Ext^{p,*}_{E^{*}} (E^{*}(X), F_{*}) \xRightarrow[p]{}    F_{*}(X)
$$
with edge homomorphism
$$
F_{*}(X) \to \Hom^{*}_{E^{*}}(E^{*}(X), F_{*}).
$$
=--

A particularly important special case of these statements is when we have a space, say $Y$, and a cohomology theory, $E^{*}(-)$. Then we define a new homology theory $F_{*}(-)$ by $F_{*}(X) = E_{*}(X \wedge Y)$ and a new cohomology theory $G^{*}(-)$ by $G^{*}(X) = E^{*}(X \wedge Y)$. These are representable, the homology theory by $Y \wedge E$ and the cohomology theory by the function spectrum $F(Y,E)$. Putting these into the statements of the universal coefficient theorem, we obtain similar statements for the [[Künneth theorem]].

+-- {: .num_kt #kta .thremark }
###### KT1
There is a spectral sequence
$$
\Tor_{p,*}^{E_{*}} (E_{*}(X), E_{*}(Y)) \xRightarrow[p]{}    E_{*}(X \wedge Y)
$$
with edge homomorphism
$$
E_{*}(X) \otimes _{E_{*}} E_{*}(Y) \to E_{*}(X \wedge Y).
$$
=--

+-- {: .num_kt #ktb .thremark }
###### KT2
There is a spectral sequence
$$
\Ext_{E_{*}}^{p,*}(E_{*}(X), E^{*}(Y)) \xRightarrow[p]{}    E^{*}(X \wedge Y)
$$
with edge homomorphism
$$
E^{*}(X \wedge Y) \to \Hom_{E_{*}}^{*} (E_{*}(X), E^{*}(Y)).
$$
=--

+-- {: .num_kt #ktc .thremark }
###### KT3
For $X$ a finite CW-complex, there is a spectral sequence
$$
\Tor_{p,*}^{E^{*}} (E^{*}(X), E^{*}(Y)) \xRightarrow[p]{}    E^{*}(X \wedge Y)
$$
with edge homomorphism
$$
E^{*}(X) \otimes _{E^{*}} E^{*}(Y) \to E^{*}(X \wedge Y).
$$
=--

+-- {: .num_kt #ktd .thremark }
###### KT4
For $X$ a finite CW-complex, there is a spectral sequence
$$
\Ext^{p,*}_{E^{*}} (E^{*}(X), E_{*}(Y)) \xRightarrow[p]{}    E_{*}(X \wedge Y)
$$
with edge homomorphism
$$
E_{*}(X \wedge Y) \to \Hom_{E^{*}}^{*} (E^{*}(X), E_{*}(Y)).
$$
=--

The key question is, thus: when do these statements hold? Adams gives some answers in [Ada69](#Ada69).

* If $F_{*}$ is flat over $E_{*}$ then [UCT1](#ucta) holds, whence [KT1](#kta) holds if either $E_{*}(X)$ or $E_{*}(Y)$ is flat.

* If $E = S$, the [[sphere spectrum]], then all the results are true.

* If $E$ is a strict [[ring spectrum]] then [KT1](#kta) holds, if also $F$ is a strict [[module spectrum]] over $E$ then [UCT1](#ucta) holds.

* [[Atiyah]] gives a method in [Ati62](#Ati62) for [KT3](#ktc) with $E = BU$ and $X$, $Y$ finite complexes.

### A Special Case ###

In both [Ada69](#Ada69) and [Ada74](#Ada74), there is a particular focus on the universal coefficient theorem coming from its applications to the [[Adams spectral sequence]].  With that aim in mind, he studies the universal coefficient theorems with considerably strong assumptions.  These assumptions are designed to allow Atiyah's method (from [Ati62](#Ati62)) to work.

+-- {: .un_theorem #assume}
###### Assumption ######
(Condition 13.3 in [Ada74](#Ada74), see also Assumption 20 in [Ada69](#Ada69)).

   The spectrum $E$ is the direct limit of finite spectra $E_\alpha$ for which $E_*(D E_\alpha)$ is projective over $E_*$ and

   $$ 
   F^*(D E_\alpha) \to \Hom^*_{E_*}(E_*(D E_\alpha), F_*)
   $$

   is an isomorphism for all [[module-spectra]] $F$ over $E$.  Here, $D E_\alpha$ is the [[S-dual]] of $E_\alpha$.
=--

The main difference between the two treatments is that in [Ada69](#Ada69), the condition involving $F$ is stated for a *single* module-spectrum, not for *all* module-spectra, and there are alternatives for homology ($F_*(-)$) and cohomology ($F^*(-)$).

In the comments following Assumption 20 in [Ada69](#Ada69), Adams remarks that this is implied by a stronger condition (Proposition 17) on $E$ which makes no reference to $F$.  As $E$ is a ring spectrum, this reduces to:

1. The spectral sequence $H^*(E_\alpha; E^*) \Rightarrow E^*(E_\alpha)$ is trivial, and
2. For each $p$, $H^p(E_\alpha; E^*)$ is projective as an $E^*$-module.

With this assumption, Adams shows the following result:

+-- {: .num_theorem #uctholds}
###### Theorem ######
Let $E$ be a ring spectrum satisfying [the assumption above](#assume).  Let $F$ be a module-spectrum over $E$.  Then \ref{uctb} holds, and the spectral sequence is convergent.
=--

What "convergent" means here is spelled out in [Ada74, Theorem 8.2](#Ada74).

+-- {: .num_corollary #uctproj}
###### Corollary ######
Let $E$ be a ring spectrum satisfying [the assumption above](#assume).  Suppose that $E_*(X)$ is projective over $E_*$.  Then the spectral sequence from \ref{uctb} collapses at the $E^2$ term.  That is,
$$
F^*(X) \to \Hom^*_{E_*}(E_*(X),F_*)
$$
is an isomorphism.
=--

In [Ada74](#Ada74), Adams lists several cohomology theories (for $E^*(-)$) where the assumption holds.  These are: $S$, $H\mathbb{Z}_p$, $MO$, $MU$, $MSp$, $K$, $KO$.

## References

* {: #Ada69 }  **Ada69** J.&nbsp;F. Adams. Lectures on generalised cohomology. pages 1--138, Berlin, 1969. Springer.

* {: #Ada74 } **Ada74** Adams, J. F. (1974). Stable homotopy and generalised homology. Chicago, Ill.: University of Chicago Press.

* {: #Ati62 }  **Ati62** M.&nbsp;F. Atiyah. Vector bundles and the K&uuml;nneth formula. Topology, 1:245--248, 1962.


An exposition of the universal coefficient theorem for ordinary cohomology and homology is in section 3.1 of

* [[Allen Hatcher]], _Algebraic topology_ ([pdf](http://www.math.cornell.edu/~hatcher/AT/AT.pdf))

The note

* Adam Clay, _The universal coefficient theorems and K&#252;nneth formulas_ ([pdf](http://www.math.ubc.ca/~aclay/Algtopology.pdf))

surveys and spells out statement and proof of the theorem.

Universal coefficient theorems for [[generalized homology]] are discussed in 

* [[Friedrich Bauer]], _Remarks on universal coefficient theorems for generalized homology theories_ Quaestiones Mathematicae
Volume 9, Issue 1 & 4, 1986, Pages 29 - 54 


[[!redirects universal coefficient theorem]]
[[!redirects universal coefficient theorems]]
