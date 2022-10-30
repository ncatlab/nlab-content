
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Rational homotopy theory
+--{: .hide}
[[!include differential graded objects - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A **Sullivan model** of a [[rational space]] $X$ is a particularly well-behaved commutative [[dg-algebra]] [[quasi-isomorphism|quasi-isomorphic]] to the dg-algebra of Sullivan forms on $X$.
These _Sullivan algebras_ are precisely the cofibrant objects in the standard [[model structure on dg-algebras]].

Sullivan models are a central tool in [[rational homotopy theory]].


## Definition


Sullivan models are particularly simple [[dg-algebra]]s that are equivalent to the dg-algebras of Sullivan differrential forms on topological spaces. Conversely, every rational space can be obtained from a dg-algebra and the _minimal_ Sullivan algebras provide convenient representatives that correspond bijectively to rational homtopy types under this correspondence.

We now describe this in detail. First some notation and preliminaries:

+-- {: .un_def }
###### Definition
**(finite type)**

* A [[graded vector space]] $V$ is _of finite type_ if in each degree it is finite dimensional. In this case we write $V^*$ for its degreewise dual.

* A [[Grassmann algebra]] is of finite type if it is the Grassmann algebra $\wedge^\bullet V^*$ on a graded vector space of finite type 

  (the dualization here is just convention, that will help make some of the following constructions come out nicely).

* A [[CW-complex]] is of finite type if it is built out of finitely many cells in each degree.

=--



For $V$ a $\mathbb{N}$-[[graded vector space]] write 
$\wedge^\bullet V$ for the [[Grassmann algebra]] over it. Equipped with the trivial differential $d = 0$ this is a [[semifree dga]] $(\wedge^\bullet V, d=0)$.

With $k$ our ground [[field]] we write $(k,0)$ for the corresponding [[dg-algebra]], the tensor unit for the standard [[monoidal category|monoidal structure]] on $dgAlg$. This is the [[Grassmann algebra]] on the 0-vector space
$(k,0) = (\wedge^\bullet 0, 0)$.


+-- {: .un_def }
###### Definition
**(Sullivan algebras)**

A **relatived Sullivan algebra** is a [[morphism]] of dg-algebras that is an inclusion

$$
  (A,d) \to (A \otimes_k \wedge^\bullet V, d')
$$

for $(A,d)$ some dg-algebra and for $V$ some graded vector space, such that 

* there is a [[well ordered set]] $J$

* indexing a basis $\{v_\alpha \in V| \alpha \in J\}$ of $V$;

* such that with $V_{\lt \beta} = span(v_\alpha | \alpha \lt \beta)$ for all basis elements $v_\beta$ we have that 

  $$
    d' v_\beta \in A \otimes \wedge^\bullet V_{\lt \beta}
    \,.
  $$

This is called a **minimal** relative Sullivan algebra if in addition the condition

$$
  (\alpha \lt \beta) \Rightarrow (deg v_\alpha  \leq deg v_\beta)
$$

holds. For a Sullivan algebra $(k,0) \to (\wedge^\bullet V, d)$ relative to the tensor unit we call the [[semifree dga]] $(\wedge^\bullet V,d)$ simply a **Sullivan algebra**.  And a **minimal Sullivan algebra** if $(k,0) \to (\wedge^\bullet V, d)$ is a minimal relative Sullivan algebra.

=--

See also the section [Sullivan algebras](http://ncatlab.org/nlab/show/model+structure+on+dg-algebras#SullivanAlgebras) at [[model structure on dg-algebras]].


+-- {: .un_remark }
###### Remark

The special condition on the ordering in the relative Sullivan algebra says precisely that these morphisms are composites of [[pushout]]s of the [[cofibrantly generated model category|generating cofibrations]] of the [[model structure on dg-algebras]], which are the inclusions

$$
  S(n) \hookrightarrow D(n)
  \,,
$$

where 

$$
  S(n) = (\wedge^\bullet \langle c \rangle, d= 0)
$$ 

is the dg-algebra on a single generator in degree $n$ with vanishing differential, and where

$$
  S(n) = (\wedge^\bullet (\langle b \rangle \oplus \langle c \rangle), d b = c, d c = 0)
$$ 

with $b$ an additional generator in degree $n-1$.

Therefore for $A \in dgAlg$ dg-algebra, a pushout

$$
  \array{
     S(n) &\stackrel{\phi}{\to}& A
     \\
     \downarrow && \downarrow
     \\
     D(n) &\to& (B \otimes \wedge^ \bullet \langle b \rangle, d b = \phi) 
  }
$$ 

is precisely a choice $\phi \in A$ of a $d_A$-closed element in degree $n$
and results in adjoining to $A$ the element $b$ whose differential is
$d b = \phi$. This gives the condition in the above definition: the differential of any new element has to be one of the old elements.

Notice that it follows in particular that the cofibrations in $dgAlg_{proj}$ are precisely all the [[retract]]s of relative Sullivan algebra inclusions.

=--

+-- {: .un_remark }
###### Remark
**($L_\infty$-algebras)**

Because they are [[semifree dga]]s, Sullivan dg-algebras $(\wedge^\bullet V,d)$ are (at least for degreewise finite dimensional $V$) [[Chevalley-Eilenberg algebra]]s of [[L-∞-algebra]]s.

The co-commutative differential co-algebra encoding the corresponding [[L-∞-algebra]] is the free cocommutative algebra $\vee^\bullet V^*$ on the degreewise dual of $V$ with differential $D = d^*$, i.e. the one given by the formula

$$
  \omega(D(v_1 \vee v_2 \vee \cdots v_n)) =
  - (d \omega) (v_1, v_2, \cdots,  v_n)
$$

for all $\omega \in V$ and all $v_i \in V^*$.

=--



+-- {: .un_def }
###### Definition
**(Sullivan models)**

For $X$ a [[conected|simply connected]] [[topological space]] $X$, a **Sullivan (minimal) model** for $X$ is 

* a quasi-free [[dg-algebra]] $(\wedge^\bullet V^*, d_V)$ which is a (minimal) Sullivan algebra 

* such that there exists a [[quasi-isomorphism]]

  $$
    (\wedge^\bullet V^*, d_V) \stackrel{\simeq}{\to}
    \Omega^\bullet_{Sull}(X)
    \,.
  $$

=--



## Properties


+-- {: .un_prop }
###### Proposition
**(cofibrations are relative Sullivan algebras)**

The cofibration in the standard [[model structure on dg-algebras]] $C dgAlg_{\mathbb{N}}$ are precisely the [[retract]]s of relative  Sullivan algebras $(A,d) \to (A\otimes_k \wedge^\bullet V, d')$.

Accordingly, the cofibrant objects in $C dgAlg$ are precisely the Sullivan algebras $(\wedge^\bullet V, d)$

=--


+-- {: .un_theorem }
###### Theorem

[[rational space|Rational homotopy types]] of simply connected spaces $X$ are in bijective corespondence with minimal Sullivan algebras $(\wedge^\bullet V,d)$

$$
  (\wedge^\bullet V , d) \stackrel{\simeq}{\to}
  \Omega^\bullet_{Sullivan}(X)
  \,.
$$

And homotopy classes of morphisms on both sides are in bijection.

=--

+-- {: .proof}
###### Proof

This appears for instance as corollary 1.26 in 

* [[Kathryn Hess]], _Rational homotopy theory: a brief introduction_ ([arXiv](http://arxiv.org/abs/math.AT/0604626))


=--


Write

$$
  (\Omega^\bullet_{Sul} \dashv K)
  :
  dgAlg^{op}
  \stackrel{\overset{\Omega^\bullet_{Sul}}{\leftarrow}}{\underset{K}{\to}}
  sSet
$$

for the [[Quillen adjunction]] induced by forming Sullivan differential forms, as discussed above.



+-- {: .un_theorem }
###### Theorem

Let $(\wedge^\bullet V^*, d_V)$ be a simply connected Sullivan algebra of finite type. Then

* the unit of the [[adjunction]] $(\wedge^\bullet V^*, d_V) \to \Omega^\bullet_{Sul}(K(\wedge^\bullet, d_V) \rangle)$ is a [[quasi-isomorphism]];

* The elements of the homotopy groups of the rational space modeled by $(\wedge^\bullet V^*, d_V)$ are the generators in $V$:

  there is an isomorphism of $\mathbb{N}$-[[graded vector space]]s over $\mathbb{Q}$

  $$
    \pi_\bullet(\langle (\wedge^\bullet V^*, d_V)\rangle)
    \simeq
    V.
  $$

=--

+-- {: .proof}
###### Proof

This is recalled for instance as theorem 1.24 in 

* [[Kathryn Hess]], _Rational homotopy theory: a brief introduction_ ([arXiv](http://arxiv.org/abs/math.AT/0604626))


=--












+-- {: .un_prop }
###### Proposition

Sullivan mimimal models are unique up to [[isomorphism]]. 

=--

+-- {: .proof}
###### Proof


This appears for instance as prop 1.18 in 

* [[Kathryn Hess]], _Rational homotopy theory: a brief introduction_ ([arXiv](http://arxiv.org/abs/math.AT/0604626))


=--



+-- {: .un_theorem }
###### Theorem

Rational homotopy types of simply connected spaces $X$ are in bijective corespondence with minimal [[Sullivan model]]s $(\wedge^\bullet V,d)$

$$
  (\wedge^\bullet V , d) \stackrel{\simeq}{\to}
  \Omega^\bullet_{Sullivan}(X)
  \,.
$$

And homotopy classes of morphisms on both sides are in bijection.

=--

+-- {: .proof}
###### Proof

This appears for instance as corollary 1.26 in 

* [[Kathryn Hess]], _Rational homotopy theory: a brief introduction_ ([arXiv](http://arxiv.org/abs/math.AT/0604626))


=--

+-- {: .un_corollary }
###### Corollary


It follows that if $(\wedge^^\bullet V^{*}, d)$ is a minimal Sullivan model for $X$, then the rational homotopy groups of $X$ can be read off from the generators $V$:

$$
  \pi_\bullet(X) \otimes \mathbb{Q} \simeq V
  \,.
$$

=--



## Examples 


### The $n$-sphere

...

### Complex projective space

...

### Product spaces

...

### Formal spaces

* [[formal dg-algebra]]

## References

In

* [[Kathryn Hess]], _Rational homotopy theory: a brief introduction_ ([arXiv](http://arxiv.org/abs/math.AT/0604626))

Sullivan algebras and minimal algebras appear in def 1.10

[[!redirects Sullivan models]]
[[!redirects Sullivan algebra]]
[[!redirects Sullivan algebras]]
[[!redirects Sullivan minimal algebra]]
[[!redirects Sullivan minimal algebras]]

[[!redirects minimal Sullivan model]]
[[!redirects minimal Sullivan models]]

[[!redirects minimal model]]
[[!redirects minimal models]]