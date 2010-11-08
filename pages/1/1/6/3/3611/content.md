
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

If $V$ is a [[symmetric monoidal category]] that is also a [[monoidal model category]], then under suitable conditions there is also the structure of a [[model category]] on the category of $V$-[[operad]]s. 

This is important for the notion of _homotopy_ [[algebra over an operad]], such as $A_\infty$- and $E_\infty$-algebras.


## Definition

Recall that a $V$-operad $P$ is called _reduced_ if $P(0)$ is the tensor unit, $P(0) = I$.  

+-- {: .un_theorem }
###### Theorem


Let $V$ be a [[monoidal model category]] with unit $I$, such that

* $V$ is [[cofibrantly generated model category|cofibrantly generated]] and $I$ is cofibrant;

* the [[model structure on an over category|model structure on the overcategory]] $V/I$ has a symmetric monoidal fibrant replacement functor;

* $V$ admits a commutative Hopf [[interval object]].

Then there exists a cofibrantly generated model structure on the category of reduced $V$-operads, in which a morphism $P \to Q$ is a weak equivalence (resp. fibration) precisely if for all $n \gt 0$ the morphisms $P(n) \to Q(n)$ are weak equivalences (resp. fibrations) in $V$.

=--

+-- {: .proof}
###### Proof

This is [BerMor03, theorem 3.1](http://arxiv.org/PS_cache/math/pdf/0206/0206094v3.pdf#page=8).

=--

If $V$ is even a [[cartesian closed category]], a stronger statement is possible:

+-- {: .un_theorem }
###### Theorem

Let $V$ be a [[cartesian closed category]], such that

* $V$ is [[cofibrantly generated model category|cofibrantly generated]] and the [[terminal object]] is cofibrant;

* $V$ has a symmetric monoidal fibrant replacement functor.

Then there exists a cofibrantly generated model structure on the category of $V$-operads, in which a morphism $P \to Q$ is a weak equivalence (resp. fibration) precisely if for all $n \geq 0$ the morphisms $P(n) \to Q(n)$ are weak equivalences (resp. fibrations) in $V$.



=--


## Examples

The conditions of the above theorems are satisfied for

* $V = $ [[sSet]] with the standard [[model structure on simplicial sets]].

  The induced model structure on $sSet$-operads is [[Quillen equivalence|Quillen equivalent]] to the [[model structure on dendroidal sets]].

* $V = $ [[Top]] the equivalence model structure on compactly generated topological spaces;

  The _homotopy algebras_ over a simplicial/topological operad as defined by Boardman and Vogt (see references below), are algebras for cofibrant replacements of these operads in this moel structure. This is essentially the statement of theorem 4.1 in

  * [[Rainer Vogt]], 
    _Cofibrant operads and universal $E_\infty$-operads_ , 
    Bielefeld SB 343 (1999), to appear in Topology Appl.


* $V = Ch_\bullet$, the [[model structure on chain complexes]];

* $V = sSh(C)$ the [[model structure on simplicial sheaves]] on some [[site]] $C$.


## Homotopy algebras over an operad

With $V$ as above, say a $V$-operad $P$ is _admissible_ if the category of $P$ [[algebra over an operad|algebras]] carries a [[transferred model structure]] from the free-forgetful adjunction

$$
  F_P : V \stackrel{\leftarrow}{\to} Alg_P : U_P
  \,.
$$

Under mild assumptions on $V$, cofibrant operads are admissible.

+-- {: .un_theorem }
###### Theorem

For an arbirtrary $V$-operad $P$, [[generalized the|the]] category of **homotopy $P$-algebras** is the category of $\hat P$-algebras for some cofibrant replacement $\hat P$ of $P$.

=--

Indeed, this is well defined up to [[Quillen equivalence]]:

[BerMor03, corollary 4.5](http://arxiv.org/PS_cache/math/pdf/0206/0206094v3.pdf#page=15).

Moreover, for this it is sufficient that $\hat P$ be _$\Sigma$-cofibrant_ . 

For instance the [[associative operad]] is $\Sigma$-cofibrant, so that by the above every $A-\infty$-algebra may be rectified to an ordinary monoid.

See around [BerMor03, remark 4.6](http://arxiv.org/PS_cache/math/pdf/0206/0206094v3.pdf#page=15).


## Related concepts

* **model structure on operads**

* [[model structure on algebras over an operad]]

## References

An influential article in which many of the homotopical and $(\infty,1)$-categorical aspects of operad theory originate is

* [[Michael Boardman]] and [[Rainer Vogt]], _Homotopy invariant algebraic structures on topological spaces_ , Lect. Notes Math. 347 (1973).

A systematic study of [[model category]] structures on operads and their algebras is in

* [[Clemens Berger]], [[Ieke Moerdijk]], _Axiomatic homotopy theory for operads_ ([arXiv:math/0206094](http://arxiv.org/abs/math/0206094))
