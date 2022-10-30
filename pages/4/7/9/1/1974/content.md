


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea 

The term _Grothendieck group_ has two closely related meanings:

* [Grothendieck group of commutative monoids](#OfCommutativeMonoids)

* [Grothendieck group of stable infinity-categories](#OfStableCategories)


In its restricted sense the Grothedieck group of a commutative monoid (i.e. of a commutative [[semi-group]] with [[unitality|unit]]) $A$ is a specific presentation of its [[group completion]], given as a certain [[group]] structure on a [[quotient]] of the [[Cartesian product]] $A \times A$. This is such that applied to the additive monoid of [[natural numbers]] $\mathbb{N}$ it produces the additive group of [[integers]] $\mathbb{Z}$ represented by pairs of natural numbers $(n_+, n_-)$ subject to an [[equivalence relation]] which identifies them with their [[difference]] $n_+ - n_-$.

A vaguely similar procedure applied to [[decategorification|isomorphism classes]] of certain [[Quillen exact category|Quillen exact categories]] happens to compute a group that is called the [[algebraic K-theory]] of these categories. See [[K-theory]] for some general abstract nonsense behind this.

Notably, the Grothendieck group completion of the [[decategorification]] of the category of [[topological vector bundles]] on some ([[compact Hausdorff space|compact Hausdorff]]) [[topological space]] $X$ produces the group known as the [[topological K-theory]] of $X$.

Given this one speaks more generally of the ([[algebraic K-theory|algebraic]]) [[K-theory]] group of a suitable category (one presenting a [[stable (∞,1)-category]] in some way) as its _Grothendieck group_ .

In that sense, the Grothendieck group of a ($\infty$-)category $C$ with a notion of [[fibration sequence|cofibration sequence]]s is the [[decategorification]] set $K(C)$ equipped with a notion of addition that is encoded in these homotopy exact sequences.


We now first state the definition of "Grothendieck group completion" -- which is really just the _free group completion of an abelian [[monoid]]_ --  and then the definition of Grothendieck group in the sense of [[algebraic K-theory]]. Notice that a priori both concepts are entirely independent constructions on different entities. But in various special case both can be applied to specific objects so as to produce the same result.


## Of commutative monoids
 {#OfCommutativeMonoids}

Every [[abelian  group]] is in particular a [[commutative monoid]]. The [[forgetful functor]] $U \colon Ab \to CMon$ from the [[category]] [[Ab]] to the category [[CMon]] has a [[left adjoint]] $F$ (the corresponding [[free functor]]), the _[[group completion]]_ functor

$$
  Ab
    \underoverset
      {\underset{U}{\longrightarrow}}
      {\overset{F}{\longleftarrow}}
      {\bot}
  CMon
$$

The _[[Grothendieck group construction on commutative monoids]]_ (def. \ref{GrothendieckGroupViaQuotientOfCartesianProduct} below) is an explict presentation of this [[group completion]] functor.

For more details see at _[[Grothendieck group of a commutative monoid]]_.

+-- {: .num_remark}
###### Remark

The idea of the free group on an abelian monoid is a very simple algebraic idea that, at least for a [[cancellative monoid]] (so that the unit is monic and one can reasonably use the term 'completion') certainly predates [[Grothendieck]]. That the [[integers]] $\mathbb{Z}$ is the group completion of the [[natural numbers]] $\mathbb{N}$ goes back at least to [[Kronecker]].

=--

+-- {: .num_defn #GrothendieckGroupViaQuotientOfCartesianProduct}
###### Definition
**([[Grothendieck group of a commutative monoid]])**

Let $(A,+)$ be a [[commutative monoid]] (i.e. a commutative [[semi-group]]).

On the [[Cartesian product]] of underlying sets $A \times A$ (the set of ordered [[pairs]] of elements in $A$), consider the [[equivalence relation]]

$$
  \big(
    (a_+, a_-) \sim_1 (b_+, b_-)
  \big) 
    \;\Leftrightarrow\; 
  \left(
    \underset{k \in A}{\exists}
    \left( 
      a_+ + b_- + k = b_+ + a_- + k
    \right)
  \right)
$$

or equivalently the equivalence relation

$$
  \big(
    (a_+, a_-) \sim_2 (b_+, b_-)
  \big) 
    \;\Leftrightarrow\; 
  \left(
    \underset{k_1, k_2 \in A}{\exists}
    \left(
      (a_+ + k_1, a_- + k_1)
      =
      (b_+ + k_2, b_- + k_2)
    \right)
  \right)
  \,.
$$

Write

$$
  G(A) \coloneqq (A \times A)/\sim
$$

for the set of [[equivalence classes]] under this equivalence relation. This inherits a binary operation

$$
  + \;\colon\; G(A) \times G(A) \longrightarrow G(A)
$$

by applying the addition in $A$ on representatives:


$$
  [a_+,a_-] + [b_+,b_-] \coloneqq [ a_+ + b_+ , a_- + b_- ]
  \,.
$$

This defines the structure of an [[abelian group]]

$$
  (G(A),+)
$$

and this is the _Grothendieck group_ of $A$. 

This comes with a canonical [[homomorphism]] of [[semigroups]]

$$
  \array{
    A &\overset{\phantom{A} \eta_A \phantom{A} }{\longrightarrow}& G(A)
    \\
    a &\overset{\phantom{AAA}}{\mapsto}& [a,0]
  }
  \,.
$$

=--



## Of stable $\infty$-categories
 {#OfStableCategories}

In this sense, a Grothendieck group is fundamentally something assigned to a [[stable (∞,1)-category]].  We start with the naive [[decategorification]] of $C$, i.e. the set of [[equivalence]] classes of objects, which inherits the structure of an abelian monoid.  Then in addition to group-completing it as above, we add additional [[generators and relations|relations]] by the rule that for every [[fibration sequence]] 

$$
  A \to X \to B
$$ 

in $C$, the equivalence classes $[A]$, $[B]$ and $[X]$ must satisfy

$$
  [X] = [A] + [B]
  \,.
$$

The result is also called the [[K-theory]] of $C$.

In particular, the additive inverse $-[A]$ of an element $[A]$ is the class of its [[loop space object]] $\Omega A$, or equivalently of its [[delooping]] $\mathbf{B} A$ called the _suspension_ $\Sigma A$, since by definition the sequences

$$
  \Omega A \to 0 \to A
$$

and

$$
  A \to 0 \to \Sigma A
$$

are [[fibration sequence]], so that

$$
  [A] + [\Omega A] = 0
$$

and

$$
 [A] + [\Sigma A] = 0
 \,.
$$

But there are many ways to _model_ a [[stable (∞,1)-category]] by an ordinary category. Essentially for each of these ways there is a seperate prescription for how to model the above general construction in terms of concrete 1-categorical constructions.

In particular from an

* [[abelian category]]

and a

* [[Quillen exact category]]

one obtains the corresponding [[category of chain complexes|categories of chain complexes]]. These are [[stable (infinity,1)-category|stable (∞,1)-categories]]. Below we list presciptions for how to compute the Grothendieck/K-theory groups of these in terms of the underlying 1-categories.

Apart from the case of abelian categories, this requires some handle on the fibration sequences. A tool developed to handle exactly this for the purpose of computing Grothendieck/K-theory groups is the notion of a [[Waldhausen category]]. That provides the sufficient extra information to get a hand on the homotopy exact sequences.


### of an abelian category ### 

Let $C$ be an [[abelian category]].  The **Grothendieck group** or [[algebraic K-theory]] group of $C$, denoted $K(C)$, is the [[abelian group]] generated by [[decategorification|isomorphism class]]es of objects of $C$, with relations of the form 

$$[X] = [A] + [B] $$

whenever there is a [[short exact sequence]] 

$$ 0 \to A \to X \to B \to 0 $$


### of a Quillen exact category ###

An exact category $C$ in the present sense is a full [[subcategory]]
of an [[abelian category]] $\hat C$ such that the collection
of all sequences $0 \to A \to X \to B \to 0$
in $C$ that are [[exact sequence]]s in $\hat C$ has the property that for every [[exact sequence]] $A \to X \to B$ in $\hat C$ with $A$ and $B \in C$ also their "sum" $X$ is in $C$.

Given an exact category $C$ with the inherited notion of exact sequences this way, the definition of its Grothendieck group is as above.


### of a Waldhausen category ###


A [[Waldhausen category]] is a [[category with weak equivalences]] with an [[initial object]] -- called $0$ -- and equipped with the notion of auxiliary morphism called _cofibrations_. These satisfy some axioms which are such that the ordinary 1-categorical [[cokernel]] of a cofibration $A \hookrightarrow X $, i.e. the ordinary [[pushout]]

$$
  \array{
    A &\hookrightarrow& X
    \\
    \downarrow && \downarrow
    \\
    0 &\to &  B 
  }
$$

computes the desired [[homotopy colimit|homotopy]] [[pushout]]. (This is exactly dual to the reasoning by which one computes [[homotopy pullback]]s in a [[category of fibrant objects]]. See there for details.)

Therefore in a Waldhausen category a [[fibration sequence|cofibration sequence]] is a [[pushout]] sequence

$$
 A \hookrightarrow X \to B
$$

where the first morphism is a cofibration.

The Grothendieck/[[K-theory]]-group of the [[Waldhausen category]] $C$ is then, as before, on the [[decategorification]] $K(C)$ the abelian group structure given by

$$
  [X] = [A] + [B]
$$

for all cofibration sequences as above.




### Examples 



* The Grothendieck group of the [[Quillen exact category]] of [[vector bundle]]s on a space $X$ is called the [[topological K-theory]] of $X$.

  Notice that vector bundles do not form an [[abelian category]].


* The Grothendieck group of the category of finite-dimensional complex-linear [[representations]] of a [[group]] is called its [[representation ring]].

These two examples illustrate a general fact: the Grothendieck group of a [[monoidal category|monoidal]] [[abelian category]] inherits a ring structure from the tensor product in this category, and thus becomes a ring, called the [[Grothendieck ring]]. See also the general discussion at [[decategorification]].

* Every [[Quillen exact category]] $C$ is canonically equipped with the structure of a [[Waldhausen category]]. The two different prescriptions for forming the Grothendieck group $K(C)$ of $C$ do coincide.



## Related concepts

* [[group completion]]

* [[K-theory]]

## References 


* [[Charles Weibel]], _The K-book: An introduction to algebraic K-theory_ ([web](http://www.math.rutgers.edu/~weibel/Kbook.html))
  
  section 2: _The Grothendieck group $K_0$_ ([pdf](http://www.math.rutgers.edu/~weibel/Kbook/Kbook.II.pdf))

See also

* [The Grothendieck Construction](http://online.itp.ucsb.edu/online/ktheory/wu/) (UCSB ITP Seminar)


* Wikipedia, _[Grothendieck group](https://en.wikipedia.org/wiki/Grothendieck_group)_


[[!redirects Grothendieck groups]]